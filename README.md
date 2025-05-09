
---

# Chatbot for Book Recommendation using Machine Learning and NLP

## Project Overview

This project involves the creation of an AI-powered chatbot that serves two main purposes:

1. **Chatbot Interaction**: The chatbot engages users in natural language conversations, responding intelligently to user queries.
2. **Book Recommendation**: The chatbot suggests books based on user preferences, utilizing Natural Language Processing (NLP) and Machine Learning (ML) techniques.

The project combines NLP with a custom neural network to predict the most relevant responses or book recommendations, making it a dual-purpose application—both a conversational agent and a personalized book advisor.

---

## Technologies Used

* **Programming Language**: Python
* **Libraries & Frameworks**:

  * **TensorFlow / Keras**: For building and training the deep learning model.
  * **NLTK**: For text preprocessing, tokenization, and lemmatization.
  * **Scikit-learn**: For model evaluation and metrics.
  * **Flask**: For developing the web interface where users can interact with the chatbot.
* **Preprocessing Techniques**: Tokenization, Lemmatization, Bag of Words (BoW).
* **Web Interface**: Flask for building the web application.
* **Model**: Custom neural network using dense layers for intent classification and book recommendation.
* **Dataset**: A book recommendation dataset (can be obtained from Kaggle or any public resource).

---

## Project Setup

### 1. Prerequisites

To run this project, make sure you have the following installed on your system:

* Python (version 3.x)
* Pip (Python package manager)

### 2. Install Required Libraries

Clone the repository and install the required libraries using the following commands:

```bash
pip install tensorflow scikit-learn nltk flask
```

### 3. Download Required Resources

The project uses **NLTK** for text processing, so you will need to download the necessary datasets:

```python
import nltk
nltk.download('punkt')
nltk.download('wordnet')
```

---

## How It Works

### 1. **Preprocessing User Input**

The user’s input text is tokenized and lemmatized to convert it into a format suitable for machine learning models. The text is preprocessed using NLTK’s `word_tokenize()` and `WordNetLemmatizer()` functions.

### 2. **Model Building**

A custom neural network model is built using **TensorFlow** and **Keras**. The model consists of multiple dense layers for intent classification and book recommendations. It is trained on labeled data for intent classification and book suggestion.

### 3. **Flask Web Interface**

The web interface is built using **Flask**, providing a simple user experience. Users can interact with the chatbot and get responses or book recommendations via HTTP POST requests.

### 4. **Predicting Intent and Book Recommendations**

When a user inputs a query, the chatbot:

* Processes the input text.
* Classifies the intent (either general conversation or book recommendation).
* If the intent is related to books, the chatbot suggests a book with additional feedback and ratings.
* If the intent is a general query, it provides a response from predefined intents.

---

## Running the Application

1. Clone the repository and navigate to the project folder.

2. Install all dependencies using the command:

   ```bash
   pip install -r requirements.txt
   ```

3. Start the Flask application by running:

   ```bash
   python app.py
   ```

4. Open your web browser and go to `http://127.0.0.1:5000/` to interact with the chatbot.

---

## Example Interactions

1. **User:** *"Recommend a book in history."*
   **Chatbot Response:**

   ```json
   {
     "Book": "Krakatoa",
     "Feedback": "Simon Winchester, New York Times bestselling author of The Professor and the Madman, examines the legendary annihilation in 1883 of the volcano-island of Krakatoa, which was followed by an immense tsunami that killed nearly forty thousand people. The effects of the immense waves were felt as far away as France. Barometers in Bogotá and Washington, D.C., went haywire. Bodies were washed up in Zanzibar. The sound of the island's destruction was heard in Australia and India and on islands thousands of miles away. Most significant of all -- in view of today's new political climate -- the eruption helped to trigger in Java a wave of murderous anti-Western militancy among fundamentalist Muslims, one of the first outbreaks of Islamic-inspired killings anywhere. Krakatoa gives us an entirely new perspective on this fascinating and iconic event. This P.S. edition features an extra 16 pages of insights into the book, including author interviews, recommended reading, and more.",
     "Rate": 3.87
   }
   ```

2. **User:** *"I need a book on science fiction."*
   **Chatbot Response:**

   ```json
   {
     "Book": "Dune",
     "Feedback": "Dune, written by Frank Herbert, is a science fiction masterpiece. Set in a future where humanity has colonized the galaxy, it tells the story of Paul Atreides, a young nobleman whose family is given control of the desert planet Arrakis. The planet is the only known source of the spice melange, the most valuable substance in the universe. Dune combines adventure, politics, religion, and ecology in a gripping tale that explores power and destiny.",
     "Rate": 4.25
   }
   ```

---

## Future Enhancements

* **Improved Book Recommendation Algorithm**: Incorporating collaborative filtering or content-based recommendations for more accurate suggestions.
* **Expanded Intent Support**: Adding more intents to handle a wider range of user queries.
* **Natural Response Generation**: Using advanced models like GPT for more natural conversation flow and responses.
* **User Profiles**: Implementing user preferences to provide personalized and consistent book suggestions over time.

---



---

## Acknowledgements

* "Hands-On Machine Learning with Scikit-Learn, Keras, and TensorFlow" by Aurélien Géron
* HuggingFace Transformers documentation
* Flask Documentation
* NLTK Documentation
* Kaggle Datasets

---


