# LM-ACTION: Task Classifier for a Large Action Model
LeWagon final data science project
Worked on by:
- [@FarisZahrani](https://github.com/FarisZahrani) | Lead Developer
- [@AlsaediAmro](https://github.com/AlsaediAmro) | Data Analyst Engineer
- [@raydbasa](https://github.com/raydbasa) | Deep Learning Engineer
- [@AbdulazizAllahw](https://github.com/AbdulazizAllahw) | Research & Development Engineer

## 📋 Contents
1. [Introduction](#introduction)
2. [Demo](#demo)
3. [Data Generation](#data-generation)
4. [Analysis](#analysis)
5. [Development](#development)
6. [Modeling](#modeling)

---

### 1. Introduction
We developed a **Task Classification Model** for the **Large Action Model (LAM)** using **BERT**.
- **BERT** is a language model that understands the context of words in natural language, ideal for classification tasks.
- **LAM** is an AI system that interprets natural language commands and converts them into executable actions on a computer.

### 2. Demo
You can access the task classifier demo here:  
[LM Task Classifier Demo](https://lam-task-classifier-demo.streamlit.app/)

### 3. Data Generation
We generated over 22,000 tasks using both local and API-based LLMs with auto-balancing for data distribution:
- **Local LLM Data Generation**:
  - LLaMA-3.1-8B-Instruct
  - Hermes-3-Llama-3.1-8B
- **API LLM Data Generation**:
  - Gemini-1.5-Pro
  - ChatGPT-4o
  - Claude-3.5-Sonnet
  - ChatGPT-4o-Mini

- **Data Cleaning**: Used LLMs to remove duplicates and developed a Database Manager for handling multi-job processing.
### 4. Project Life Cycle Diagram

Below is the project life cycle diagram that outlines the process from data generation to deployment:

![Project Life Cycle Diagram](images/Untitled_Diagram.png)


### 5. Analysis
- **Data Analysis**: Ensuring that data aligns with our schema and objectives.
- **What-If Analysis**: Exploring the potential impact of various approaches on the data.
- **Feature Analysis**: Ensuring consistency between task features and actions.
- **Data Cleaning**: Producing two files—one ready for immediate use and another requiring further processing.

### 6. Development
Here’s a quick guide through the data lifecycle, from generation to application development.
- We start by generating reliable data from multiple LLMs, merging it, and ensuring consistency.
- We maintain data integrity through manual and automated cleaning, using LLMs for complex cases.
- Once clean, we store the data in a database and apply feature engineering to gain insights.
- To balance data for model training and reduce bias, we use prompt engineering to improve data generation.
- Finally, we train the model and deploy it in the application for user interaction.

### 7. Modeling
We used **BERT** as a base model to classify tasks based on:
- **Feasibility and Legality**
- **Ethicality and Boundaries**
- **Reversibility and Risk Level**

To improve performance, we applied:
- **Text augmentation and focal loss**
- **Gradient accumulation and learning rate scheduling**
- **Early stopping** to enhance model performance

### Future Improvements:
- **Multi-lingual support** (e.g., Arabic and other languages).
- **Wider data range** to further enhance model accuracy.
