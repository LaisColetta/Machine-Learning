![Voice Transcription](https://media.wired.com/photos/59266d1ff3e2356fd8009347/191:100/w_1280,c_limit/Voice_Transcription-01-f2.jpg)

# **Machine Learning Project - ATU Winter 2024**  
**Author**: Lais Coletta Pereira  
**Lecturer**: Brian McGinley  

---

## **Project Overview: Debate Audio Analysis - Donald Trump & Kamala Harris**

This project leverages pre-trained machine learning models to analyze an audio recording of the 2024 U.S. Presidential Debate between candidates Donald Trump and Kamala Harris. The diarisation, transcription and analysis aims to show nuances in the debate, such as potential media bias or impartiality.

---

### **Objective**

Develop a Jupyter Notebook that performs the following tasks on audio files (MP3 or WAV):  

1. **Speaker Diarization**:  
   - Identify distinct speakers in the audio.  
   - Output timestamps for when each speaker starts and stops talking.  
   - Calculate how long each speaker spoke.  

2. **Speech-to-Text Analysis**:  
   - Generate a transcript of the audio with speakers clearly identified.  
   - Analyze word counts for each speaker and perform a frequency analysis of specific words.  
     Example:  
     ```
     [Speaker 1] Hi, how are you today?  
     [Speaker 2] I’m good and you?  
     [Speaker 1] Good thanks, how about….  
     ```

3. **Large Language Model (LLM) Analysis**:  
   - Use the annotated transcript to query a Large Language Model for additional insights, such as:  
     - Identifying speaker affiliations (e.g., left-wing/right-wing values).  
     - Analyzing sentiment or other contextual details.  

---

### **Testing Requirements**

- **Provided Test File**: A research audio file from the Harris v. Trump 2024 U.S. Presidential Debate (not to be hosted publicly).  
- **Custom Test File**: Analyze a more complex audio file (e.g., multiple speakers of the same gender) to evaluate model performance.  

---

### **Development & Documentation**

- All work must be conducted and documented in a **Jupyter Notebook**.  
- Regular commits must be made to a private GitHub repository, with **brianmcgatu** added as a collaborator.  
- Final submission must include:  
  - A fully executed notebook with outputs populated.  
  - A **README** detailing environment setup and instructions for notebook execution.  

---

### **Research & Bibliography**

- Capture all research within the notebook and include a properly formatted bibliography.  
- Comparisons between different models should be documented in a **separate research notebook**, with findings referenced in the main notebook.

---

### **Evaluation Rubric**

1. **Consistency**: 20%  
2. **Research**: 25%  
3. **Development**: 30%  
4. **Documentation**: 25%  

*Note: Marks will reflect both results and methodology, as per ATU’s Student Code of Conduct.*  

---

## Repository Structure
Audio Files

Testing Files
Project_part1.ipynb



--- 

## Bibliography

---

## Tools used

---

# **PyAnnote: Speaker Diarization Toolkit**

PyAnnote is a Python library designed for **speaker diarization**.

It uses state-of-the-art deep learning models to provide robust and accurate diarization pipelines, supporting tasks like:
- **Voice Activity Detection (VAD)**: Detect speech in an audio file.
- **Speaker Segmentation**: Identify changes in speakers over time.
- **Speaker Embedding**: Extract unique speaker features.
- **Clustering**: Group similar segments to label speakers.

---

## **How PyAnnote Works**
1. **Pre-trained Models**: Hosted on [Hugging Face](https://huggingface.co/models?search=pyannote).
2. **Pipeline**: Combines speech detection, speaker change detection, and clustering for full diarization.
3. **Output**: Generates **RTTM** files containing speaker labels and timestamps.

---

## **Use Cases**
- **Meetings & Interviews**: Label and transcribe multi-speaker recordings.
- **Media Indexing**: Identify speakers in podcasts or TV shows.
- **Surveillance**: Analyze audio for speaker-based events.


???
