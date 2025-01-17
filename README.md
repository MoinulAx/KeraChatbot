# Kira: An AI-Powered Chatbot

Kira is a conversational AI chatbot designed to understand and respond to user inputs using natural language processing (NLP) techniques. Built with the **Kira library**, **Flask**, and **Jinja2**, Kira leverages **TensorFlow**, **Keras**, and a custom dataset to deliver intelligent and dynamic interactions.

---

## Features
- **Intent Recognition**: Accurately identifies user intents based on text inputs.
- **Dynamic Responses**: Delivers contextually relevant replies.
- **Custom Dataset**: Trained on a dataset of patterns, intents, and responses.
- **Web Interface**: Interactive and user-friendly, powered by Flask and Jinja2.
- **Extensible**: Easily adaptable to various domains and applications.

---

## Technology Stack
- **Programming Language**: Python
- **Frameworks**: Flask, Jinja2
- **Libraries**: TensorFlow, Keras, NLTK
- **Model Architecture**: Neural network with dense layers
- **Dataset**: JSON format with intents, patterns, and responses

---

## Installation

1. **Clone the Repository**:
   ```bash
   git clone <repository-url>
   cd <repository-folder>
   ```

2. **Install Dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

3. **Download NLTK Data**:
   ```python
   import nltk
   nltk.download('popular')
   ```

4. **Prepare Dataset**:
   Ensure `data.json` is placed in the project directory. This file contains the chatbot's intents, patterns, and responses.

5. **Train the Model**:
   Run `train.py` to preprocess the dataset and train the neural network:
   ```bash
   python train.py
   ```
   This will generate `model.h5`, `texts.pkl`, and `labels.pkl` files.

6. **Start the Chatbot**:
   Launch the Flask app to interact with Kira:
   ```bash
   python app.py
   ```
   The app will run locally at `http://127.0.0.1:5000`.

---

## How It Works

1. **Data Preprocessing**:
   - Tokenizes and lemmatizes text inputs using NLTK.
   - Converts patterns into a bag-of-words format for model training.

2. **Model Architecture**:
   - Input Layer: 128 neurons
   - Hidden Layer: 64 neurons
   - Output Layer: Softmax activation

3. **Response Generation**:
   - Predicts the intent using the trained model.
   - Matches the intent with predefined responses from `data.json`.

4. **Deployment**:
   - Flask serves the chatbot's web interface using Jinja2 templates.

---

## File Structure
```
├── app.py           # Main Flask app for running the chatbot
├── train.py         # Script for preprocessing data and training the model
├── data.json        # Dataset with intents, patterns, and responses
├── model.h5         # Trained neural network model
├── texts.pkl        # Tokenized words for the model
├── labels.pkl       # Intent labels for the model
├── templates/
│   └── index.html   # Frontend template for the chatbot
├── static/
    └── styles.css   # Stylesheet for the web interface
```

---

## Future Enhancements
- **Multilingual Support**: Extend Kira's capabilities to handle multiple languages.
- **Advanced NLP Models**: Upgrade to transformer-based architectures like BERT.
- **Improved Interface**: Add real-time messaging and voice integration.

---

## License
This project is licensed under the MIT License. See `LICENSE` for details.

---

## Acknowledgments
- NLTK for preprocessing
- TensorFlow and Keras for model training
- Flask and Jinja2 for deployment

Feel free to contribute or raise issues for enhancements and bug fixes!
