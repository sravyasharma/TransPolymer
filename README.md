# TransPolymer

### Where Chemistry Clicks with Code

TransPolymer is a **deep learning–powered polymer informatics platform** designed to predict important polymer properties directly from **SMILES representations** using a **Transformer-based architecture**.

The system combines **Natural Language Processing (NLP), deep learning, and full-stack web technologies** to create an intelligent framework for **accelerating polymer discovery and material design**.

Instead of relying on slow experimental processes, TransPolymer enables **real-time prediction of polymer properties**, helping researchers evaluate materials faster and more efficiently.

---

# Project Overview

Polymers are fundamental to industries such as:

* Electronics
* Energy
* Aerospace
* Healthcare
* Packaging
* Advanced materials

Traditional polymer property analysis requires **extensive laboratory experiments**, making the process expensive and time-consuming.

TransPolymer addresses this challenge by:

* Learning **chemical patterns from SMILES sequences**
* Using **Transformer-based deep learning**
* Predicting multiple polymer properties simultaneously
* Providing predictions through a **web-based interface**

The system bridges the gap between **computational chemistry and practical material science applications**.

---

# Key Features

* Transformer-based polymer property prediction
* SMILES-based chemical language modeling
* Multi-property prediction using regression heads
* Masked Language Model (MLM) pretraining
* Interactive web interface
* Real-time prediction results
* Scalable backend architecture
* Prediction history storage

---

# Polymer Properties Predicted

TransPolymer predicts the following **six polymer properties**:

| Property | Description              |
| -------- | ------------------------ |
| **Eea**  | Electron Affinity        |
| **Egb**  | Band Gap Energy          |
| **Eps**  | Dielectric Constant      |
| **Ei**   | Ionization Energy        |
| **Nc**   | Refractive Index         |
| **Xc**   | Crystallization Tendency |

These properties are critical for understanding **electronic, optical, and thermal characteristics of polymers**.

---

# System Architecture

The TransPolymer platform follows a **full-stack AI architecture** consisting of frontend, backend, machine learning pipeline, and database.

```
User
 │
 ▼
React Frontend
 │
 ▼
FastAPI Backend
 │
 ▼
SMILES Validation
 │
 ▼
Tokenizer (RoBERTa Style)
 │
 ▼
Transformer Encoder
 │
 ▼
Regression Head (MLP)
 │
 ▼
Polymer Property Predictions
 │
 ▼
MongoDB Database
```

---

# Architecture Components

## Frontend

The frontend provides the main interface for users to interact with the system.

Features include:

* SMILES input field
* Property prediction results
* Prediction history
* Interactive dashboard

Technology:

* React.js
* CSS
* Axios
* React Router

---

## Backend

The backend handles:

* API communication
* SMILES validation
* Model inference
* Database interaction

Technology:

* FastAPI
* Python
* Pydantic

---

## Machine Learning Pipeline

The ML pipeline processes SMILES strings and predicts polymer properties.

Pipeline:

```
SMILES Input
   ↓
Tokenization
   ↓
Transformer Encoder
   ↓
Feature Embeddings
   ↓
Regression Head
   ↓
Property Prediction
```

Components:

* RoBERTa-style tokenizer
* Transformer encoder
* MLM pretraining module
* MLP regression head

---

# Transformer Model Architecture

The core prediction model is a **custom Transformer encoder architecture** trained on polymer SMILES data.

### Components

1. Tokenizer
   Converts SMILES sequences into tokenized input.

2. Embedding Layer
   Transforms tokens into vector representations.

3. Positional Encoding
   Adds sequence order information.

4. Transformer Encoder
   Uses **multi-head self-attention** to capture chemical relationships.

5. Regression Head
   Predicts polymer properties.

---

# Training Strategy

TransPolymer supports **two model training approaches**.

## 1. Scratch Model

The model is trained directly on labeled polymer datasets.

Loss Function:

Mean Squared Error (MSE)

Pipeline:

```
SMILES → Transformer → Regression Head → Property Prediction
```

---

## 2. Pretrained Model

The model is first trained using **Masked Language Modeling (MLM)**.

MLM Training:

```
C=C(C) → C=[MASK](C)
```

The model learns chemical patterns from large SMILES datasets.

After pretraining, the MLM head is replaced with the regression head for property prediction.

---

# Technology Stack

## Frontend

* React.js
* CSS
* Axios
* React Router

## Backend

* FastAPI
* Python
* Pydantic

## Machine Learning

* PyTorch
* Custom Transformer Encoder
* Masked Language Modeling (MLM)
* MLP Regression Head

## Database

* MongoDB
* MongoDB Atlas

## Development Tools

* Git
* GitHub
* Google Colab
* Visual Studio Code

---

# Implementation Pipeline

The implementation follows a modular workflow.

## 1. Data Preparation

Input:

Polymer sequences in **SMILES format**

Steps:

* SMILES preprocessing
* Tokenization
* Dataset preparation

Datasets include polymer properties such as:

* Eea
* Egb
* Eps
* Ei
* Nc
* Xc

---

## 2. Model Training

Two model versions are trained:

### Scratch Model

* Transformer encoder
* MLP regression head
* Trained on labeled datasets

### Pretrained Model

* MLM pretraining
* Fine-tuned for property prediction

---

## 3. Model Serving

Trained models are integrated into the backend using **FastAPI APIs**.

API responsibilities:

* Input validation
* Prediction inference
* Response generation

---

## 4. Data Storage

MongoDB stores:

* User queries
* Prediction results
* Session history

---

# User Interface Workflow

The user workflow is simple and efficient.

```
User enters SMILES
       ↓
System validates SMILES
       ↓
ML model processes input
       ↓
Property predictions generated
       ↓
Results displayed on dashboard
       ↓
Prediction saved in history
```

---

# Example Prediction Output

Input:

```
C1=CC=CC=C1
```

Output Properties:

* Electron Affinity (Eea)
* Band Gap Energy (Egb)
* Dielectric Constant (Eps)
* Ionization Energy (Ei)
* Refractive Index (Nc)
* Crystallization Tendency (Xc)

Results are displayed in a structured format within the interface.

---

# Model Evaluation

The model was evaluated using several performance metrics.

### Root Mean Squared Error (RMSE)

Average RMSE across properties:

```
0.4275
```

Lower RMSE indicates strong predictive accuracy.

---

### R² Score

Average R²:

```
0.979
```

This means the model explains **~98% of variance in polymer properties**.

---

### Perplexity (MLM)

Perplexity:

```
~5.3
```

This indicates strong understanding of SMILES chemical structure.

---

# Applications

TransPolymer can be used for:

* Polymer material discovery
* Polymer screening
* Optical materials design
* Electronic materials research
* Accelerated materials engineering

---

# Future Work

Potential improvements include:

* Larger polymer datasets
* Graph neural network integration
* Polymer generation models
* Property visualization dashboards
* Mobile interface
* Explainable AI for polymer prediction
* Copolymer and blend prediction
* Integration with chemical design tools

---

# References

Key resources used during development include:

* Transformer architectures for molecular modeling
* Polymer informatics research
* HuggingFace Transformers documentation
* FastAPI documentation
* React.js documentation
* MongoDB documentation

---

# Authors

* Sravya Sharma
* Samiksha Gupta
* Pardiv Reddy
* Prathik Reddy
* Bharghav Ram

Department of CSE (AI & ML)
Keshav Memorial College of Engineering

---

# License

This project is intended for **research and academic use**.
