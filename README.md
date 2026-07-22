# FAQ-chatbot
NLP-based FAQ chatbot using TF-IDF and cosine similarity to match user queries to predefined answers.
# FAQ Chatbot (NLP-Based Question Answering System)

A simple chatbot that answers Frequently Asked Questions using TF-IDF vectorization and cosine similarity, instead of hardcoded if-else matching. Built as Task 2 for the CodeAlpha Artificial Intelligence internship.

## How it works

1. A predefined FAQ dataset (questions + answers) is stored as a Python dictionary.
2. All FAQ questions are converted into TF-IDF vectors using `scikit-learn`.
3. When a user asks a question, it's converted into a TF-IDF vector using the same fitted vectorizer.
4. Cosine similarity is computed between the user's query and every FAQ question.
5. The best-matching FAQ is returned along with a confidence score.
6. If the confidence score is below a threshold (0.3), the chatbot returns a fallback message instead of guessing.

## Tools & Technologies

- **Language:** Python
- **NLP Library:** scikit-learn
- **Text Representation:** TF-IDF (Term Frequency – Inverse Document Frequency)
- **Similarity Measure:** Cosine Similarity

## Features

- Predefined, easily extendable FAQ dataset
- TF-IDF + cosine similarity matching
- Handles empty input and unmatched/irrelevant queries gracefully
- Confidence score shown with every response
- Fallback response when confidence is too low
- Runs interactively in a loop

## Getting Started

### Prerequisites

- Python 3.8+

### Installation

```bash
git clone https://github.com/<your-username>/faq-chatbot.git
cd faq-chatbot
pip install -r requirements.txt
```

### Usage

```bash
python faq_chatbot.py
```

Example:

```
FAQ Chatbot (type 'exit' to stop)

You: how do i get my money back
Chatbot: Yes, refunds are available within 30 days of purchase.
(Confidence Score: 0.62)

You: exit
Chatbot: Goodbye!
```

## Sample FAQs Covered

- What is your name?
- How do I reset my password?
- What are your working hours?
- How can I contact support?
- Do you offer refunds?
- How do I track my order?
- Is my payment information secure?
- Can I change my delivery address?

## Limitations & Future Improvements

TF-IDF relies on exact keyword overlap and does not understand synonyms or different word forms (e.g., "refund" vs. "refunds"). Planned improvements:

- Add stemming/lemmatization (e.g., with NLTK)
- Use n-grams for more context
- Replace TF-IDF with sentence embeddings (e.g., Sentence-BERT) for semantic matching
- Expand the FAQ dataset

## Author

Tayyaba 
Electronics Engineering Student
MUET, Jamshoro

## License

This project is open source and available under the [MIT License](LICENSE).
