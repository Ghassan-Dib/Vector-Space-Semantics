# Vector Space Semantics for Similarity between EastEnders Characters

This project implements and refines vector-based representations of character dialogue from *EastEnders* scripts. The goal is to distinguish character-specific speech patterns for accurate classification of test and validation data using information retrieval techniques.

## Features

### 1. **Preprocessing**
   - Removed punctuation and stopwords.
   - Tokenized text, converted to lowercase, and applied stemming.
   - Improved feature representation, achieving 75% accuracy and a mean rank of 2.0.

### 2. **Linguistic Feature Extraction**
   - Incorporated unigrams, bigrams, trigrams, and part-of-speech (POS) tags.
   - Added sentiment analysis (positive, negative, neutral, and compound scores).
   - Used TF-IDF transformation and feature selection to emphasize informative terms.
   - Achieved 87.5% accuracy and a mean rank of 1.4375.

### 3. **Contextual Features**
   - Grouped lines by episode and scene, adding preceding and subsequent dialogue context.
   - Integrated context-aware tokenization and tagging.
   - Optimized feature sets using grid search, achieving 93.75% accuracy on validation data.

### 4. **Parameter Optimization**
   - Conducted grid search across preprocessing, feature extraction, and matrix transformation.
   - Evaluated combinations of tokenization, stopword removal, n-grams, POS tags, and sentiment analysis.

### 5. **Similarity Analysis**
   - Evaluated cosine similarity between character vectors.
   - Demonstrated character-specific speech distinctions while avoiding overfitting.

### 6. **Final Testing**
   - Tested on unseen data, achieving:
     - Mean rank: 1.5
     - Cosine similarity: 0.625
     - Accuracy: 81.5%

## Results
- The project demonstrates robust performance in distinguishing character dialogues.
- Focused feature sets (e.g., sentiment analysis) were more effective than overly complex configurations.

## Dependencies
- Python 3.x
- NLTK
- Sci-kit Learn
- SentimentIntensityAnalyzer

## Usage
1. Preprocess the data using `preprocess_with_context`.
2. Extract features using `extract_features`.
3. Train and test using the provided configurations and analyze results.
