# Music Recommendation System

This project is a lyrics-based music recommendation system that leverages natural language processing and machine learning to suggest similar songs. It processes a large dataset of song lyrics, cleans and vectorizes the text, and computes similarity scores to enable fast and relevant recommendations.

## Key Features
- Cleans and preprocesses song lyrics using NLTK
- Converts lyrics to TF-IDF vectors for feature extraction
- Calculates cosine similarity between songs for recommendations
- Logs all preprocessing steps for transparency and debugging
- Saves processed data and models for efficient reuse

## Preprocessing Script (`src/preprocess.py`)
- Loads and samples the dataset (`spotify_millsongdata.csv`)
- Drops unnecessary columns
- Cleans and tokenizes lyrics, removing stopwords
- Vectorizes lyrics using TF-IDF (up to 5,000 features)
- Computes pairwise cosine similarity between all songs
- Saves the cleaned DataFrame, TF-IDF matrix, and similarity matrix as `.pkl` files
- All progress and errors are logged to `preprocess.log`

## Requirements
- Python 3.8+
- See `requirements.txt` for dependencies

## Usage
1. Create and activate a virtual environment
2. Install dependencies: `pip install -r requirements.txt`
3. Run preprocessing: `python src/preprocess.py`
4. Use the generated `.pkl` files for building recommendation features in your app

---
This project is for educational purposes and demonstrates the use of NLP for music recommendations.