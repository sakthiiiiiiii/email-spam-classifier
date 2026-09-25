# Email Spam Classifier

NLP-based email spam detection system using machine learning.

## Overview

This project aims to classify emails as spam or ham (non-spam) using natural language processing (NLP) and machine learning techniques. The model is trained on email text data and uses preprocessing, vectorization, and classification to detect spam messages.

## Features

- Email text preprocessing
- Tokenization and text cleaning
- TF-IDF vectorization
- Spam detection using machine learning
- Model training and evaluation
- Prediction pipeline for new email messages
- Simple API interface for inference

## Tech Stack

- Python
- Scikit-learn
- Pandas
- NumPy
- NLTK / text processing utilities
- Flask / FastAPI (if used in your project)
- Pickle for model persistence

## Project Structure

```bash
Email_Spam_Detection/
│
├── main.py
├── requirements.txt
├── models/
│   ├── spam_model.pkl
│   ├── count_vectorizer.pkl
│   └── ...
├── src/
│   ├── api/
│   │   └── app.py
│   ├── data/
│   │   ├── load_data.py
│   │   ├── preprocess.py
│   │   └── process_dataset.py
│   ├── features/
│   │   └── vectorizer.py
│   ├── models/
│   │   ├── build_model.py
│   │   ├── evaluate.py
│   │   ├── predict.py
│   │   └── train.py
│   └── quarantine/
│       └── store.py
└── README.md
```

## Installation

1. Clone the repository:
```bash
git clone https://github.com/sakthiiiiiiii/email-spam-classifier.git
cd email-spam-classifier
```

2. Create a virtual environment:
```bash
python -m venv venv
```

3. Activate the virtual environment:
- Windows:
```bash
venv\Scripts\activate
```

- macOS/Linux:
```bash
source venv/bin/activate
```

4. Install dependencies:
```bash
pip install -r requirements.txt
```

## Usage

Run the main script:

```bash
python main.py
```

If the project includes an API, start it with:

```bash
python src/api/app.py
```

To test prediction on a sample email:

```python
from src.models.predict import predict_email

email_text = "Congratulations! You have won a free prize. Click here now."
result = predict_email(email_text)

print(result)
```

## Model Details

The project uses a text classification pipeline based on:

- text preprocessing
- tokenization
- stopword removal
- TF-IDF vectorization
- classification model (for example, Naive Bayes, Logistic Regression, or SVM)

The trained model and vectorizer are saved as `.pkl` files in the `models/` directory.

## Dataset

This project is designed for spam classification tasks using email text datasets.  
If you are using a custom dataset, place it in the data folder and process it via the scripts in `src/data/`.

## Evaluation

The model can be evaluated using metrics such as:

- Accuracy
- Precision
- Recall
- F1-score
- Confusion matrix

Evaluation logic is implemented in:
- `src/models/evaluate.py`

## Future Improvements

- Add more robust preprocessing
- Experiment with different NLP models
- Improve accuracy using word embeddings
- Add a web interface
- Deploy the model using Flask/FastAPI
- Add real-time spam classification from email inbox data

## License

This project is licensed under the MIT License.

## Author

Sakthi Jayakumar

## Acknowledgements

This project was developed for email spam detection using NLP and machine learning techniques.
