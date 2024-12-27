![Voice Transcription](https://media.wired.com/photos/59266d1ff3e2356fd8009347/191:100/w_1280,c_limit/Voice_Transcription-01-f2.jpg)

# **Machine Learning | Project 1 - ATU Winter 2024**  
**Author**: Lais Coletta Pereira  
**Lecturer**: Brian McGinley  

---

## **Project Overview: Debate Audio Analysis - Donald Trump & Kamala Harris**

This project uses pre-trained machine learning models to analyze an audio recording of the 2024 U.S. Presidential Debate between candidates Donald Trump and Kamala Harris. The diarization, transcription, and analysis aim to reveal nuances in the debate, such as potential media bias or impartiality. The main goal is to analyze speech patterns, identify distinct speakers, and extract insights from the conversation.

---

### **Objective**

Develop a Jupyter Notebook that performs the following tasks on audio files (MP3 or WAV):  

1. **Speaker Diarization**:  
   - Identify distinct speakers in the audio.  
   - Output timestamps indicating when each speaker begins and ends their speech.  
   - Calculate how long each speaker spoke in total.  

2. **Speech-to-Text Analysis**:  
   - Generate a full transcript of the audio with speaker identification.  
   - Analyze word counts for each speaker and perform frequency analysis on specific words.  
     Example:  
     ```
     [Speaker 1] Hi, how are you today?  
     [Speaker 2] I’m good, and you?  
     [Speaker 1] Good thanks, how about you?  
     ```

3. **Large Language Model (LLM) Analysis**:  
   - Use the annotated transcript to query a Large Language Model (LLM) for further insights, such as:  
     - Identifying speaker affiliations (e.g., left-wing/right-wing values).  
     - Analyzing sentiment or identifying other contextual information related to the speech.  

---

## **Repository Structure**

##### **Audio Files Folder**
This folder contains the MP3 files used for testing, as well as the exported WAV files, such as the **TrumpHarrisDebate.mp3** and corresponding WAV files used in the project.

##### **Testing Files Folder**
This folder includes two Jupyter Notebooks:  
- **diarisation_comparison.ipynb**: Compares diarization models, testing performance within **Pyannote**, **SpeechBrain**, **Kaldi**, and **Deepgram**.
- **speech_to_text.ipynb**: Compares the performance of speech-to-text models including **Wav2Vec 2.0**, **Whisper**, and **VOSK**.

##### **Project_part1.ipynb**
This Jupyter Notebook follows the steps outlined for analyzing the Trump and Harris Debate. It includes processes for speaker diarization, speech-to-text conversion, and querying a large language model for sentiment analysis.

##### **requirements.txt**
Lists the Python libraries and dependencies required to run the notebooks. All necessary installations can be performed using `pip install -r requirements.txt`.

---

### **Research & Bibliography**

The bibliography used in this repository is provided at the end of each Jupyter Notebook. It includes relevant websites, research papers, reference codes from Kaggle, and discussions from various forums that have guided the development of this project.

---

### **Environment Setup and Instructions for Notebook Execution**

To set up the environment and run the notebook smoothly, follow these steps:

1. **Install Python**:
   - Ensure you have **Python 3.12** installed on your system. You can download it from [python.org](https://www.python.org/downloads/).
   - To verify the installation, open a terminal and run:
     ```bash
     python --version
     ```

2. **Clone the Repository**:
   - Clone this repository to your local machine by running the following command in your terminal:
     ```bash
     git clone https://github.com/LaisColetta/Machine-Learning
     ```
   - After cloning, navigate to the repository's root directory:
     ```bash
     cd repositoryname
     ```

3. **Create a Virtual Environment (optional)**:
   - It is recommended to create a virtual environment to manage dependencies:
     ```bash
     python -m venv venv
     ```
   - Activate the virtual environment:
     - On **Windows**:
       ```bash
       venv\Scripts\activate
       ```
     - On **macOS/Linux**:
       ```bash
       source venv/bin/activate
       ```

4. **Install Dependencies**:
   - Install the necessary dependencies listed in the `requirements.txt` file:
     ```bash
     pip install -r requirements.txt
     ```

5. **Launch Jupyter Notebook**:
   - Install Jupyter if you haven't already:
     ```bash
     pip install jupyter
     ```
   - Start Jupyter Notebook:
     ```bash
     jupyter notebook
     ```
   - This will open a new tab in your web browser where you can open and execute the `Project_part1.ipynb` notebook.

6. **Running the Notebooks**:
   - Open and run the notebooks from the **Testing Files Folder** or **Project_part1.ipynb** to conduct the analysis and testing.

---
# END