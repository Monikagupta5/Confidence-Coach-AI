
# Confidence Coach AI

Confidence Coach AI is an innovative tool that helps users enhance their communication skills by identifying and addressing low-confidence language in text or speech. By leveraging NLP and machine learning, it provides actionable feedback to empower users to communicate assertively and confidently.

## Features

### Confidence Coach AI Features:
- **Text and Speech Analysis**:
  - Detects low-confidence language patterns, such as:
    - Hedging (e.g., "I just think...")
    - Excessive apologizing (e.g., "I'm sorry, but...")
    - Passive voice usage
    - Minimizing language
  - Provides confidence-level ratings for communication.

- **Suggestions for Improvement**:
  - Replaces uncertain phrases with assertive alternatives.
  - Reframes sentences into active voice.
  - Highlights areas for improvement.

- **Speech Transcription**:
  - Converts audio to text for analysis using speech recognition.

- **Feedback Loop**:
  - Allows users to resubmit revised communication for iterative analysis.
  - Tracks user progress over time.

- **Model Retraining**:
  - Accepts user submissions to continually improve the classification model.



### Agentic AI Coach Features:
- **Modular AI System**:
  - Built using CrewAI, enabling collaboration among AI agents.
  - Easily add new agents and tasks with YAML configuration.

- **Community-driven Contributions**:
  - Encourages users to submit their own AI agents and tasks.
  - Enables extensible tools to enhance agent capabilities.

- **Scalable Coaching**:
  - Provides solutions for entrepreneurial teams via AI collaboration.



## Installation

### Prerequisites
- **Confidence Coach AI**:
  - Python 3.8+
  - Install the required libraries:
    ```bash
    pip install fastapi uvicorn nest-asyncio pyngrok spacy transformers SpeechRecognition pydub python-dotenv python-multipart
    python -m spacy download en_core_web_sm
    ```

- **Agentic AI Coach**:
  - Clone the repository and follow the guidelines:
    ```bash
    git clone https://github.com/DigitalProductschool/Agentic_AI_Coach.git
    cd Agentic_AI_Coach
    ```



## Running the Application

### Confidence Coach AI:
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

### Agentic AI Coach:
1. Run the project by navigating to your chosen module (e.g., `responsible_ai`).
2. Follow the guidelines in the respective README file.



## Project Structure

### Confidence Coach AI:
```
Confidence_Coach_AI/
├── app/
├── models/
├── data/
├── README.md
```

### Agentic AI Coach:
```
Agentic_AI_Coach/
├── knowledgebase_learning/
├── responsible_ai/
├── docs/
└── community_submissions/
```



## API Endpoints (Confidence Coach AI)

### `/classify/`
- **POST**: Classifies text input for confidence level and provides actionable feedback.

### `/transcribe/`
- **POST**: Transcribes uploaded audio and analyzes the text for confidence.

### `/submit/`
- **POST**: Submits revised communication for iterative feedback.

### `/retrain/`
- **POST**: Retrains the machine learning model using user-submitted data.



## Contributing

- For **Confidence Coach AI**:
  1. Fork the repository.
  2. Create a feature branch (`git checkout -b feature-name`).
  3. Commit your changes (`git commit -m 'Add feature'`).
  4. Push to the branch (`git push origin feature-name`).
  5. Open a pull request.

- For **Agentic AI Coach**:
  Follow the contributing guidelines in the [docs/CONTRIBUTING.md](https://github.com/DigitalProductschool/Agentic_AI_Coach/docs/CONTRIBUTING.md).



## License

This project is licensed under the MIT License. See the LICENSE file for details.



### **Acknowledgments**
- **Confidence Coach AI**:
  - Built using FastAPI, spaCy, and scikit-learn.
  - Inspired by the need to empower users to communicate confidently.

- **Agentic AI Coach**:
  - Built on CrewAI by the Digital Product School community.
  - Special thanks to all contributors!


