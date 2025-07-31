# new_AI_Project
Building AI course project

# Community Voice Insight Tool

Final project for the Building AI course

## Summary

This project uses AI to analyze social media texts (like tweets) in multiple languages to detect emotional tone and sentiment. It helps communities, researchers, and local organizations understand public mood, concerns, and engagement trends.

## Background

Social platforms like Twitter are full of public opinion, emotion, and feedback—but most of it goes unmeasured, especially across non-English languages. This project aims to give communities a tool to surface emotional patterns and sentiments over time.

This is how you make a list, if you need one:
* Emotional trends are rarely tracked across multiple languages.
* Decision-makers need better tools to understand community sentiment.
* Real-time feedback loops are useful for events, crises, or campaigns.

My motivation: I wanted to create a project that combines natural language processing with real-world social value.

## How is it used?

A user enters a list of tweets (or streams them live from the Twitter API). The system then:
- Detects language.
- Classifies sentiment (positive, neutral, negative).
- Identifies emotions like joy, anger, fear, sadness, etc.
- Visualizes this information in a clear dashboard or summary.

**Use case examples**:
- Local governments assessing reactions to a policy.
- Event organizers tracking audience sentiment in real-time.
- Researchers exploring emotional responses to global events.

<img src="https://upload.wikimedia.org/wikipedia/commons/1/1e/Emotion_classification_example.png" width="400">

## Data sources and AI methods

- **Data**:
  - Tweets gathered via the [Twitter API](https://developer.twitter.com/en/docs)
  - Pre-labeled datasets like:
    - [GoEmotions](https://github.com/google-research/goemotions)
    - [SemEval 2018 - Affect in Tweets](https://competitions.codalab.org/competitions/17751)

- **AI Methods**:
  - Multilingual sentence embeddings (e.g., LASER)
  - Multi-label neural network classifier for emotions
  - Sentiment classifier (logistic regression or neural network)
  - Optional topic modeling (LDA) for theme extraction

| Component            | Method/Tool                  |
|---------------------|------------------------------|
| Language Detection   | `langdetect` / `fasttext`    |
| Embedding            | Facebook LASER               |
| Classifier           | Feed-forward MLP             |
| Visualization        | Streamlit, Matplotlib        |

## Challenges

- May underperform for rare languages due to lack of training data.
- Subjectivity in labeling emotions and sentiments.
- Ethical concerns around analyzing user-generated content (anonymity, consent).
- Sarcasm and slang can reduce model accuracy.

## What next?

- Improve emotion detection using transformer-based models (e.g. XLM-RoBERTa).
- Extend it to aspect-based sentiment (e.g., detect if sentiment is about service, food, etc.).
- Deploy as a full web app with user-uploaded CSVs or real-time streaming.
- Translate insights into alerts or automated summaries.

To grow this further, I’d need:
- Access to larger multilingual datasets
- UI/UX support for real-time dashboards
- GPU resources for training bigger models

## Acknowledgments

* Inspired by [pbaitor/i18n-twitter-sentiment](https://github.com/pbaitor/i18n-twitter-sentiment)
* Emotion data from [Google’s GoEmotions](https://github.com/google-research/goemotions)
* Multilingual support via [Facebook LASER](https://github.com/facebookresearch/LASER)
* Project concept shaped by [Elements of AI - Building AI](https://buildingai.elementsofai.com)

[Sleeping Cat on Her Back by Umberto Salvagnin](https://commons.wikimedia.org/wiki/File:Sleeping_cat_on_her_back.jpg#filelinks) / [CC BY 2.0](https://creativecommons.org/licenses/by/2.0)
