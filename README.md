# Document-Intelligence
*Extracting desired information from various documents like Resume, Invoives, Bank Statement, Purchase Order*

1. Key Information Extraction from Resume and Job Descriptions

+ **Annotated** around 20k resumes and 10k JDs from various domains with 15 key fields like name,address,email,mobile,technical skill,soft skill,
  company name,working duration,location,college/university name,Minimum qualification,job role,designation etc
  
+ Fine-tuned **BERT-base-uncased** for **NER**
+ Indexed results into proper standard JSON format
+ Tried to improve the model performance by **Pre-training BERT** after building new corpus from 80k resumes, Tried adding
  new tokens to **BERT Vocab**.  
+ Also experimented with text chunk size to tackle the **MAX SEQ
  LENGTH issue** and context capturing, Looking into other model to overcome
  issue with BERT, like **Longformer**, **ExBert**, **ConvBERT** etc.


2. Key Information Extraction from Invoices and Bank Statements

+ **Data Annotation** and Preparation for **SDMGR** Deep Learning model
+ Trained and tested the **SDMGR** model to get key fields from invoices
+ Tried **PDFPlumber** and other **DOC-Parser** to get proper tabular data and 
  then applied **logic based approach** to get key fields from bank statements.
  
3. Deployment

+ Build **Python Flask Application**, **Dependencies Requirement file**,**Bash Script** to run the App with **Gunicorn**. 
+ Build **Dockerfile** and **Docker Container** with proper **logging**
+ Deployed the whole pipeline on **AWS EC2** instance
