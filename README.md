# Machine-Learning
24-25 Machine Learning Module for the Higher Diploma in Data Science (Data Analytics) | AT
Project Instructions & Planning

Project Part 1
This sub-project is worth 50% of the overall project grade.
Task: Interview/Debate Audio Analysis
This task is to leverage some of the existing models to perform an analysis of
interviews/debates. This tool could be used to identify media bias/impartiality
The objective of this task is to develop a notebook that will accept an audio file (mp3 or wav) of
an interview/debate.
Speaker Diarisation Analysis:
Using pre-built Speaker Diarisation models, the first task is to identify who spoke when – i.e. the
model should output the times that each speaker started and stopped talking. This should
enable calculating how many seconds/minutes each speaker spoke for.
Speech to Text Analysis:
Once the separate speakers have been identified, the next task is to use a Speech to Text model
to create a transcript of the audio with the speakers identified in the transcripts:
E.g:
[Speaker 1] Hi, how are you today?
[Speaker 2] I’m good and you?
[Speaker 1] Good thanks, how about….
This should enable an analysis of how many words each person spoke and might enable a
frequency analysis of particular words (i.e. how many times a particular word was used by a
particular individual).
Large Language Model Analysis:
Once you have the transcript with speakers identified and annotated, you can input this into a
LLM to query it on sentiment etc.
E.g. ask it can it identify what the names of the speakers are/ask it whether speakers associate
with more right-wing/left-wing values etc….
Testing:
I will give you an audio file for research purposes (from the Harris V Trump 2024 US Presidential
Debate) – Note: this file is not to be hosted on a public GitHub repo.
However, you should test on another (potentially more complex) file (with more
speakers/multiple speakers of the same sex) and evaluate/annotate the performance of the
components.
Development/Documentation:
All documentation and development should be performed within a Jupyter Notebook. Regular
commits should be made to a private GitHub repository. You must add me (brianmcgatu) as a
collaborator. The audio you tested on should be also hosted on your private repo.
Your final committed notebook should be complete with all code cell outputs populated (i.e. it
doesn’t require a viewer (me)to replicate the environment and re-execute the notebook to view
the results)
Your repository should also include a README – detailing how to recreate your environment for
the notebook to execute etc.
Any submission that does not have a full and incremental git history with informative commit
messages over the course of the project timeline will be accorded a proportionate mark.
Research:
All research must be captured through the notebook and collated in a bibliography at the end of
the notebook. An academic referencing style must be used.
If doing research/comparisons between different models, include that analysis in a separate
research notebook and refer to the research in the main notebook. This is to keep the main
notebook analysis concise.
Rubric:
Note: Your final mark will not solely be based on your final results but also on your
methodology/approach.
Consistency: 20%
Research: 25%
Development: 30%
Documentation: 25%
As usual, you are bound by ATU Student Code of Conduct (Student
Code_Final_August_2022.pdf).

Planning:
Step 1: Set Up Your Environment

Install Required Libraries:

Install libraries for audio processing, speaker diarization, speech-to-text, and LLMs:

bash
Copiar código
pip install pydub librosa SpeechRecognition pyannote.audio transformers
For speaker diarization, the pyannote-audio library is commonly used.

For speech-to-text, you can use libraries such as SpeechRecognition or whisper.

For working with LLMs, you can use transformers by Hugging Face.

Step 2: Load and Process the Audio
Input Audio (MP3 or WAV):

The first step is to upload or access the audio file (either MP3 or WAV).
You’ll need to convert the audio file to a format that works with your audio analysis tools. For instance, use pydub to convert MP3 to WAV if needed:
python
Copiar código
from pydub import AudioSegment
audio = AudioSegment.from_mp3("input_audio.mp3")
audio.export("input_audio.wav", format="wav")
Load Audio for Processing:

Use librosa or pydub to load and manipulate the audio for speaker diarization and transcription.
python
Copiar código
import librosa
audio_file = "input_audio.wav"
y, sr = librosa.load(audio_file, sr=None)  # sr is the sample rate
Step 3: Speaker Diarization (Identify Who Spoke When)
Use Pyannote-Audio for Speaker Diarization:

Pyannote is a popular library for speaker diarization, which segments audio into chunks where each speaker is active.
You can use a pre-trained model available in the pyannote-audio library:
python
Copiar código
from pyannote.audio import Model
from pyannote.audio.pipelines import SpeakerDiarization

model = Model.from_pretrained("pyannote/speaker-diarization")
pipeline = SpeakerDiarization.from_pretrained(model)

diarization = pipeline({'uri': 'filename', 'audio': audio_file})
Output Speaker Segments:

After processing the audio, the diarization model will output time-stamped segments, identifying which speaker is speaking at each moment.
You can extract the time ranges where each speaker was talking:
python
Copiar código
for speech_turn, _, speaker in diarization.itertracks(yield_label=True):
    print(f"Speaker {speaker} spoke from {speech_turn.start} to {speech_turn.end}")
Calculate Speech Duration:

Sum up the duration for each speaker to know how long each speaker spoke:
python
Copiar código
speaker_duration = {}
for speech_turn, _, speaker in diarization.itertracks(yield_label=True):
    duration = speech_turn.end - speech_turn.start
    if speaker not in speaker_duration:
        speaker_duration[speaker] = 0
    speaker_duration[speaker] += duration

print(speaker_duration)
Step 4: Speech to Text (Create a Transcript)
Use SpeechRecognition or Whisper:

Use a library like SpeechRecognition to convert the audio into text. Alternatively, whisper by OpenAI is another great option for accurate speech-to-text transcription.
python
Copiar código
import speech_recognition as sr

recognizer = sr.Recognizer()
with sr.AudioFile("input_audio.wav") as source:
    audio = recognizer.record(source)

transcript = recognizer.recognize_google(audio)  # Using Google Speech Recognition API
print(transcript)
Text with Speaker Identifiers:

Combine the speech-to-text output with the speaker diarization results so that you can identify who spoke each part of the text.
You could format your output like this:
css
Copiar código
[Speaker 1] Hi, how are you today?
[Speaker 2] I’m good, and you?
[Speaker 1] Good, thanks. How about…
Step 5: Large Language Model Analysis
Text Analysis with Pre-trained LLM:

Now that you have the transcript with speaker identification, you can pass the text into a large language model (LLM) for further analysis.
For example, use Hugging Face Transformers to analyze sentiment, extract speaker associations, etc.
python
Copiar código
from transformers import pipeline

# Use a pre-trained sentiment analysis model
sentiment_analysis = pipeline("sentiment-analysis")
results = sentiment_analysis(transcript)
print(results)
Sentiment and Bias Detection:

You can ask the model for various analyses such as identifying sentiment, speaker association with specific ideologies, etc.