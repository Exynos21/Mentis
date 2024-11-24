# Mentis 🌐🧠  
A privacy-preserving NLP-based classification model designed to analyze mental health sentiments using **Federated Learning**. This project combines machine learning, decentralized training, and ethical AI principles to tackle sensitive mental health issues while protecting user data.

---

## 📌 Table of Contents  
1. [Introduction](#-introduction)  
2. [Features](#features)  
3. [Dataset](#dataset)  
4. [Model Architecture](#model-architecture)  
5. [Federated Learning Setup](#federated-learning-setup)  
6. [Results](#results)  
7. [Challenges](#challenges)  
8. [Future Scope](#future-scope)  
9. [How to Run](#how-to-run)  

---

## 🧠 Introduction  
This project aims to classify mental health-related text into seven categories:  
**Normal, Depression, Suicidal, Anxiety, Bipolar, Personality Disorder, Stress**.  
By using **Federated Learning**, we ensure that sensitive data remains on local client devices, significantly reducing privacy risks.

---

## ✨ Features  
- **Decentralized Training**: Employs Flower framework for Federated Learning, enabling privacy-first AI.  
- **Scalable Model**: Processes over **53,000+ text entries** with efficient handling of imbalanced classes.  
- **High Accuracy**: Achieves **71% accuracy** and an **F1-score of 0.72** for multi-class classification.  
- **Secure Data Handling**: No raw data is shared; only model updates are aggregated.  

---

## 📊 Dataset  
- **Size**: ~53,000 labeled text entries.  
- **Classes**: 7 categories representing various mental health conditions.  
- **Preprocessing**:  
  - Text tokenization using **NLTK**.  
  - Stopword removal and padding for uniform sequence lengths.  

---

## 🏗️ Model Architecture  
- **Type**: LSTM (Long Short-Term Memory).  
- **Configuration**:  
  - Embedding Size: 256  
  - Hidden Size: 256  
  - Number of Layers: 2  
  - Dropout: 0.3  
- **Optimizer**: Stochastic Gradient Descent (SGD) with momentum.  

---

## 🌐 Federated Learning Setup  
- **Framework**: Flower  
- **Clients**: 15 virtual clients simulating decentralized devices.  
- **Rounds**: 10 rounds of training with model updates aggregated on the central server.  
- **Batch Size**: 128  
- **Learning Rate**: 0.01  

---

## 📈 Results  
- **Accuracy**: 71%  
- **F1 Score**: 0.72  
- **Precision and Recall**: Achieved balanced scores across all categories despite imbalanced dataset.  

---

## ⚡ Challenges  
- Adapting Federated Learning workflows from image-based tutorials to text processing.  
- Handling imbalanced data for rare classes like "Suicidal" and "Bipolar."  
- Computational limitations due to running all clients on a single CPU.  

---

## 🔮 Future Scope  
- Deploying the model to real client devices for local training and inference.  
- Integrating real-time mental health monitoring for clinical and personal use.  
- Extending the model to incorporate additional mental health conditions or languages.  

---

## 🚀 How to Run  
### Prerequisites  
- Python 3.8+  
- Required libraries: `PyTorch`, `Flower`, `NumPy`, `NLTK`, etc.  

### Steps  
1. Clone this repository:  
   ```bash  
   git clone https://github.com/Exynos21/Mentis.git  
   ```
2. Install dependencies:
    ```bash
    pip install -r requirements.txt  
    ```
3. Prepare the dataset:  
   - Place your dataset file as `Data.csv` in the root folder.  

3. Run the project using a Jupyter Notebook (.ipynb):  
     - Open the notebook file (`notebook.ipynb`). 
     - Select the correct Python kernel for your environment.  
     - Execute the cells in order to start the server and clients.  
