Overview
This project is a Python-based application that performs the following tasks:

Transcribes audio from video files using the Whisper model.
Translates the transcribed text into English using Google Translator.
Extracts metadata from the text, including the number of words and keyword frequencies.
Performs topic modeling using both LDA (Latent Dirichlet Allocation) and transformer-based clustering.
Analyzes speaker diarization in audio files to determine the number of speakers and their speaking durations.
Conducts sentiment analysis on the translated text using VADER.
The application uses several machine learning and natural language processing techniques to provide a comprehensive analysis of the audio or video input.

Requirements
Ensure you have the following Python libraries installed:

numpy
librosa
scikit-learn
gradio
whisper
deep-translator
gensim
sentence-transformers
nltk
vaderSentiment
moviepy
You can install these libraries using pip:

pip install numpy librosa scikit-learn gradio whisper deep-translator gensim sentence-transformers nltk vaderSentiment moviepy
Additionally, you need to download NLTK resources, which are handled by the script:


import nltk
nltk.download('punkt')
nltk.download('stopwords')
nltk.download('wordnet')
Usage
Run the Script: Execute the script to start the Gradio interface. You can run the script directly in your Python environment.


python your_script_name.py
Upload File: Use the Gradio interface to upload a video file (e.g., .mp4, .avi, .mkv) or an audio file. The file will be processed to extract and analyze the audio.

Output: The interface will display the following:

Original Transcribed Text
Detected Language
Translated Text (English)
Number of Words
Keyword Frequency
Number of Speakers and Speaker Durations
LDA Topics
Transformer-based Clusters
Sentiment Analysis
Clean Up: Temporary audio files created during the process will be deleted automatically.

Code Details
Audio Extraction: Extracts audio from video files using moviepy.
Text Preprocessing: Tokenizes, removes stop words, and lemmatizes text using nltk.
LDA Topic Modeling: Uses gensim to perform topic modeling.
Transformer-based Clustering: Uses sentence-transformers and scikit-learn to cluster text embeddings.
Speaker Diarization: Analyzes speaker segments using librosa and scikit-learn.
Sentiment Analysis: Uses vaderSentiment for sentiment scoring.
License
This project is licensed under the MIT License. See the LICENSE file for details.
