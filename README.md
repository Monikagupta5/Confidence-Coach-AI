# Confidence Coach AI

Confidence Coach AI is an innovative tool that helps users enhance their communication skills by identifying and addressing low-confidence language in text or speech. By leveraging NLP and machine learning, it provides actionable feedback to empower users to communicate assertively and confidently.

## Features

### Text and Speech Analysis
- Detects low-confidence language patterns, such as:
  - Hedging (e.g., "I just think...")
  - Excessive apologizing (e.g., "I'm sorry, but...")
  - Passive voice usage
  - Minimizing language

### Suggestions for Improvement
- Offers specific recommendations to:
  - Replace uncertain phrases with assertive alternatives.
  - Reframe sentences in active voice.
  - Highlight areas for improvement with confidence level ratings.

### Feedback Loop
- Allows users to resubmit revised communication for iterative analysis.
- Tracks user progress over time.

### Speech Transcription
- Converts audio to text for analysis using speech recognition.

### Model Retraining
- Accepts user submissions to continually improve the classification model.

## Installation

### Prerequisites
- Python 3.8+

Install the required libraries:
```bash
pip install fastapi uvicorn nest-asyncio pyngrok spacy transformers SpeechRecognition pydub python-dotenv python-multipart
python -m spacy download en_core_web_sm
```

## Running the Application

1. Start the FastAPI server:
```bash
uvicorn main:app --reload
```

2. Expose the server to the internet using ngrok:
```bash
ngrok http 8000
```

3. Access the API documentation at:
```
http://127.0.0.1:8000/docs
```

## API Endpoints

### `/classify/`
- **POST**: Classifies text input for confidence level and provides actionable feedback.
- **Input**: JSON with a `text` field.
- **Output**: Confidence level, suggestions, and analysis results.

### `/transcribe/`
- **POST**: Transcribes uploaded audio and analyzes the text for confidence.
- **Input**: Audio file (e.g., `.wav`, `.mp3`).
- **Output**: Transcription, confidence level, and suggestions.

### `/submit/`
- **POST**: Submits revised communication for iterative feedback.
- **Input**: User ID and text.
- **Output**: Similarity with previous submission and feedback.

### `/retrain/`
- **POST**: Retrains the machine learning model using user-submitted data.
- **Output**: Success or error message.

## Demo Video

Watch the Confidence Coach AI in action by accessing the video [here](https://drive.google.com/file/d/1Ta-q0j31MmRSTwSfYzIW7aC1xm7J--uU/view?usp=drive_link)).

## Demo Pictures

1. [Picture 1](https://drive.google.com/file/d/1tJ43OsWKrCt9PHV2CfiD62vgtn_0TwQm/view?usp=drive_link)
2. [Picture 2](https://drive.google.com/file/d/1qwCtx3Ypr6BNQgHpMfkqdQposwKttIu2/view?usp=drive_link)

## Demo Recording

[View the Recording](https://drive.google.com/file/d/1Zq2s2A3W1jmWC7-R-DpGq3oWjXIbtHmZ/view?usp=drive_link)


## How It Works

1. **Text Analysis**:
   - Patterns indicating low confidence are identified using predefined rules and spaCy NLP models.
   - Passive voice detection highlights areas for improvement.
2. **Machine Learning**:
   - A logistic regression model classifies communication as "Underconfident" or "Neutral" based on text features extracted using TF-IDF.
3. **User Interaction**:
   - Users can revise and resubmit communication, track progress, and receive updated feedback.
4. **Speech Transcription**:
   - Audio files are converted to text and analyzed using the same framework.

## Contributing

1. Fork the repository.
2. Create a feature branch (`git checkout -b feature-name`).
3. Commit your changes (`git commit -m 'Add feature'`).
4. Push to the branch (`git push origin feature-name`).
5. Open a pull request.


## License

This project is licensed under the MIT License. See the LICENSE file for details.

## Acknowledgments

- Built using FastAPI, spaCy, and scikit-learn.
- Inspired by the need to empower users to communicate confidently in professional and personal settings.

---

