# **Machine Learning - ATU Winter 2024**
**Author**: Lais Coletta Pereira  
**Lecturer**: Brian McGinley  

---

## Repository Overview

This repository contains the final project for the Machine Learning Module, which was divided into two parts. Below is the structure of the repository for easy navigation and understanding.

> **Note:** Due to disk capacity limitations, the analysis performed in this notebook was restricted, as the execution time of the code was significantly long.

---

### **Research & Bibliography**

The bibliography used in this repository can be found at the end of each Jupyter Notebook. It includes relevant websites, research papers, Kaggle code references, and discussions from various forums that guided the development of this project.

---

### **Environment Setup & Instructions for Notebook Execution**

Follow these steps to set up your environment and execute the notebooks correctly:

1. **Install Python**:
   - Ensure that Python is installed on your system. You can download it from [python.org](https://www.python.org/downloads/).
   - To verify the installation, open a terminal and run:
     ```bash
     python --version
     ```

2. **Clone the Repository**:
   - Clone the repository to your local machine by running:
     ```bash
     git clone https://github.com/LaisColetta/Machine-Learning
     ```
   - After cloning, navigate to the repository's root directory:
     ```bash
     cd repositoryname
     ```

3. **Create a Virtual Environment (optional but recommended)**:
   - It's advisable to use a virtual environment to manage dependencies. Create one by running:
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
   - Install the required Python libraries from the `requirements.txt` file:
     ```bash
     pip install -r requirements.txt
     ```

5. **Launch Jupyter Notebook**:
   - If you don't have Jupyter installed, you can install it with:
     ```bash
     pip install jupyter
     ```
   - Start Jupyter Notebook by running:
     ```bash
     jupyter notebook
     ```
   - This will open a tab in your browser, where you can open and run the `Project_part1.ipynb` notebook.

6. **Running the Notebooks**:
   - To run the analysis and testing, open the notebooks located in the **Testing Files Folder** or the `Project_part1.ipynb` file.

---

# Project Part 1: Debate Audio Analysis - Donald Trump & Kamala Harris

## **Overview**

This part of the project utilizes pre-trained machine learning models to analyze an audio recording of the 2024 U.S. Presidential Debate between candidates Donald Trump and Kamala Harris. The analysis involves speaker diarization, transcription, sentiment analysis, and the analysis of the participants’ speech patterns.

The goal is to identify distinct speakers, extract insights, and perform sentiment analysis using a large language model (LLM).

---

### **Objectives**

The goal is to develop a Jupyter Notebook that performs the following tasks on audio files (MP3 or WAV):

1. **Speaker Diarization**:  
   - Identify distinct speakers in the audio.
   - Output timestamps marking when each speaker starts and finishes their speech.
   - Calculate the total speaking time for each speaker.

2. **Speech-to-Text Analysis**:  
   - Generate a complete transcript of the audio, with speaker identification.
   - Perform a word count analysis for each speaker and include frequency analysis on specific words.
     Example:
     ```
     [Speaker 1] Hi, how are you today?
     [Speaker 2] I’m good, and you?
     [Speaker 1] Good, thanks. How about you?
     ```

3. **Large Language Model (LLM) Analysis**:  
   - Use the annotated transcript to query a large language model (LLM) for further insights such as:
     - Identifying speaker affiliations (e.g., political leanings).
     - Analyzing sentiment and identifying other contextual information related to the speech.

---

## Repository Structure

### **Audio Files Folder**
This folder contains the MP3 and WAV files used for testing. Files such as **TrumpHarrisDebate.mp3** and corresponding WAV files are included.

### **Testing Files Folder**
This folder includes the following Jupyter Notebooks:
- **diarisation_comparison.ipynb**: Compares diarization models and tests performance with **Pyannote**, **SpeechBrain**, **Kaldi**, and **Deepgram**.
- **speech_to_text.ipynb**: Compares speech-to-text models, including **Wav2Vec 2.0**, **Whisper**, and **VOSK**.

### **Project_part1.ipynb**

> Note: For detailed information about the models selected in this notebook, please refer to the **Testing Files** folder, where I compare various models and choose the ones with the best performance.

This Jupyter Notebook outlines the steps for analyzing the Trump and Harris debate, including tasks like speaker diarization, speech-to-text conversion, and sentiment analysis through a large language model.


# Project Part 2 >>> TO BE FINISHED
## Overview: 
### **Objective**
## **Repository Structure**

---
# END