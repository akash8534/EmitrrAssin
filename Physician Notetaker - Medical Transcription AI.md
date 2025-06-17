# Physician Notetaker - Medical Transcription AI 
## Overview 
Physician Notetaker is an AI system that processes doctor-patient conversations to: 

1. Extract key medical details (symptoms, diagnosis, treatment) 
1. Analyze patient sentiment and intent 
1. Generate structured clinical documentation 
## Installation Guide 
1\. Google Colab:  { 

!pip install -U spacy transformers scispacy -q 

!pip install https://s3-us-west-2.amazonaws.com/ai2-s2-scispacy/releases/v0.7.0/en\_ner\_bc5cdr\_ md-0.7.0.tar.gz -q 

!python -m spacy download en\_core\_web\_sm -q 

import spacy, json, re 

from collections import defaultdict from transformers import pipeline } 

2\.Local Installation (Python 3.7+) 

2\.1Create Virtual Environment: 

{ 

python -m venv medai-env 

source medai-env/bin/activate  # Linux/Mac medai-env\Scripts\activate    # Windows 

} 

2\.2 Install Dependencies: { 

pip install spacy transformers scispacy 

Pip install[https://s3-us-west-2.amazonaws.com/ai2-s2-scispacy/releases/v0.7.0/en_ner_bc 5cdr_md-0.7.0.tar.gz](https://s3-us-west-2.amazonaws.com/ai2-s2-scispacy/releases/v0.7.0/en_ner_bc5cdr_md-0.7.0.tar.gz) 

python -m spacy download en\_core\_web\_sm 

} 

![](Aspose.Words.c1bbb2ab-ee8d-455f-9516-9b62e5d12f31.001.png)
