# **Machine Learning - ATU Winter 2024**
**Author**: Lais Coletta Pereira  
**Lecturer**: Brian McGinley  

---

## Repository Overview

This repository contains the final project for the Machine Learning Module for the Higher Diploma in Data Science (Data Analytics) at ATU college. This project was split into Project_part1 and Project_part2. 

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

> **Note:** Due to disk capacity limitations, the analysis performed in this notebook was restricted, as the execution time of the code was significantly long.


## **Overview**

This part of the project utilizes pre-trained machine learning models to analyze an audio recording of the 2024 U.S. Presidential Debate between candidates Donald Trump and Kamala Harris. The analysis involves speaker diarization, transcription, sentiment analysis, and the analysis of the participants’ speech patterns.

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
     
3. **Large Language Model (LLM) Analysis**:  
   - Use the annotated transcript to query a large language model (LLM) for further insights such as:
     - Identifying speaker affiliations (e.g., political leanings).
     - Analyzing sentiment and identifying other contextual information related to the speech.

---

## Project 1 repository Structure

### **Audio Files Folder**
This folder contains the MP3 and WAV files used for testing. Files such as **TrumpHarrisDebate.mp3** and corresponding WAV files are included.

### **Testing Files Folder**
This folder includes the following Jupyter Notebooks:
- **diarisation_comparison.ipynb**: Compares diarization models and tests performance with **Pyannote**, **SpeechBrain**, **Kaldi**, and **Deepgram**.
- **speech_to_text.ipynb**: Compares speech-to-text models, including **Wav2Vec 2.0**, **Whisper**, and **VOSK**.

### **Project_part1.ipynb**

> Note: For detailed information about the models selected in this notebook, please refer to the **Testing Files** folder, where I compared various models and sleected the ones with the best performance.

This Jupyter Notebook outlines the steps for analyzing the Trump and Harris debate, including tasks like speaker diarization, speech-to-text conversion, and sentiment analysis through a large language model.


# Project Part 2 
## Overview: 

This project goal is to analyze a recorded dataset of seal calls and explore whether it is possible to discriminate between different types of seal calls. 

For the Machine Learning model, the dataset is built of spectrograms npz files of the seal calls extracted from wav files. 

### **Objective**
The goal is to develop a machine learning model that performs the following tasks for audio classification following the steps:

1. **Audio Pre-processing**:  
   - Load audio files and annotations from `.wav` and `.txt` files.
   - Extract audio segments based on annotations.
   - Generate spectrograms from the audio segments.
   - Pad or crop spectrograms to standardize their dimensions.
   - Create ‘No Call’ segments for silent intervals in the audio.
   - Categorize annotations into distinct classes based on their names.

2. **Model Development and Training**:  
   - Build and compile a Convolutional Neural Network (CNN) for classifying spectrograms.
   - Train the CNN model using **augmented** training data.
   - Experiment **with hyperparameters** to test different performances.
   - Utilize techniques like **EarlyStopping** to avoid overfitting and **fine tuning** to to improve performance on those underrepresented classes..

3. **Test other Transfer Learning models**:  
   - Using the pre-trained transfer learning models **EfficientNetB4** and **ResNet50** and evaluate the performance.

---

## Project 2 jupyter notebook structure

### **Spectrogram Files Folder**
This folder contains preprocessed npz 2D array spectrograms used for training. Files are categorised and sorted by name.

### **Project 2 Jupyter notebook**
This file contains data pre preprocessing for dataset creation and model training.

---
# END