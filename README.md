# Medical Conversation NLP Pipeline

This repository contains a Python application that:
- 🏥 Extracts medical entities (symptoms, diagnosis, treatments)  
- 📝 Analyzes patient sentiment & intent  
- 🗒️ Generates a structured SOAP note  

## 🚀 Setup & Installation

1. **Clone the repo**  
   https://colab.research.google.com/drive/1NPzMhUiIe4hNx3oaZ_HASXd2OiCgdRca?usp=sharing



Create a virtual environment (optional but recommended)

python3 -m venv venv
source venv/bin/activate


##Install dependencies

pip install -U spacy==3.7.4 transformers scispacy==0.7.0



pip install https://s3-us-west-2.amazonaws.com/ai2-s2-scispacy/releases/v0.7.0/en_ner_bc5cdr_md-0.7.0.tar.gz

python -m spacy download en_core_web_sm







##Run the application




python app.py

**This will print:**

Structured Medical Summary

Sentiment & Intent Analysis

SOAP Note


##**Output**  


**##Structured Medical Summary:**
![image](https://github.com/user-attachments/assets/b357b21a-0f31-49f2-9714-472bf496ca12)

**##Sentiment analysis completed!**

![image](https://github.com/user-attachments/assets/caba2558-e2e1-4767-b272-194ac47a9840)


**##SOAP note generated!**

![image](https://github.com/user-attachments/assets/51004736-d3fe-4074-aebf-7359a7773db5)


![image](https://github.com/user-attachments/assets/a6f7969e-f926-4c49-9e8e-f6e587158c01)  


**#Methodologies & Design Choices**
**spaCy NER:**

Models: en_ner_bc5cdr_md for medical entities, en_core_web_sm for general parsing

**Rule-Based Patterns:**

Regex-driven symptom & treatment detection to complement NER

**Transformers Pipelines:**

Summarization: BART (facebook/bart-large-cnn)

Sentiment Analysis: DistilBERT emotion model

**Custom Logic:**

Maps raw emotion scores → clinical labels ("Anxious", "Reassured", "Neutral")

Generates a standard SOAP note structure

