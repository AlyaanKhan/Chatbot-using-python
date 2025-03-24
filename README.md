# Chatbot AI  

This is a simple AI-powered chatbot built using TensorFlow/Keras for intent recognition and natural language processing (NLP). The chatbot is trained on predefined intents and responds to user messages based on pattern matching and machine learning predictions.  

## Features  

- **Deep Learning Model**: Uses a neural network built with Keras and TensorFlow to classify user inputs.  
- **Natural Language Processing (NLP)**: Implements tokenization, lemmatization, and bag-of-words for better understanding.  
- **Interactive GUI**: Built with Tkinter for an easy-to-use chat interface.  
- **Customizable Intents**: Easily extend the chatbot by modifying the `intents.json` file.  

## Installation  

### Prerequisites  

Ensure you have Python installed. Then, install the required dependencies:  

```bash
pip install numpy tensorflow keras nltk pickle-mixin
```

### NLTK Setup  

Before running the chatbot, download the necessary NLTK data files:  

```python
import nltk
nltk.download('punkt')
nltk.download('wordnet')
```

## Training the Chatbot  

Before running the chatbot, train the model using:  

```bash
python train_chatbot.py
```

This script:  
- Reads and processes training data from `intents.json`.  
- Creates and trains a neural network.  
- Saves the trained model as `model_chatbot.h5`.  

## Running the Chatbot  

Once trained, you can start the chatbot GUI with:  

```bash
python gui_chatbot.py
```

This will launch a Tkinter-based GUI where you can interact with the chatbot.  

## Customization  

### Modifying Intents  

You can add new responses or change existing ones by editing `intents.json`. Example format:  

```json
{
  "intents": [
    {
      "tag": "greeting",
      "patterns": ["Hello", "Hi", "Hey"],
      "responses": ["Hello!", "Hi there!", "Hey! How can I help you?"]
    }
  ]
}
```

### Improving Accuracy  

If the chatbot struggles with accuracy, consider:  
- Expanding the dataset in `intents.json`.  
- Increasing the number of training epochs in `train_chatbot.py`.  
- Experimenting with different neural network architectures.  

## Future Enhancements  

- **Integrate with Speech Recognition**: Allow voice-based interactions.  
- **Expand to Web-based UI**: Replace Tkinter with a web framework (e.g., Flask or React).  
- **Use a More Advanced NLP Model**: Upgrade to transformers like GPT for better responses.  
