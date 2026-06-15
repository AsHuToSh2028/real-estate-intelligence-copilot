# Real Estate Intelligence Copilot

An end-to-end AI-powered decision support system that combines natural-language analytics, property valuation, semantic retrieval, and explainable machine learning for real-estate intelligence.

## Overview

Real Estate Intelligence Copilot enables users to interact with housing-market data using natural language. The system supports:

* Natural-language market analytics
* Automated Text-to-SQL query generation
* Property valuation from free-form descriptions
* Explainable AI using SHAP
* Comparable property retrieval through semantic search
* Counterfactual "What-If" valuation analysis

The project integrates Large Language Models (LLMs), CatBoost, SHAP, semantic retrieval, and SQL-based analytics into a unified conversational workflow.

---

## Dataset

* King County Housing Dataset
* 21,000+ property records
* Property attributes including:

  * Location
  * Bedrooms
  * Bathrooms
  * Living Area
  * Grade
  * Waterfront Status
  * Renovation History
  * Market Characteristics

---

## System Architecture

User Query
↓
Intent Classification
↓
┌─────────────────────────────────────┐
│ Analytics │ Valuation │ Simulation │
└─────────────────────────────────────┘
↓ ↓ ↓

Text-to-SQL CatBoost Feature Modification

↓ ↓ ↓

SQLite SHAP Re-Prediction

↓ ↓ ↓

Insights Explanation Impact Analysis

---

## Core Components

### 1. Housing Market Analytics

Converts natural-language questions into executable SQL queries.

Example:

Question:
"What premium do waterfront properties command?"

Generated SQL:

SELECT
AVG(CASE WHEN waterfront=1 THEN price END) -
AVG(CASE WHEN waterfront=0 THEN price END)
AS waterfront_premium
FROM properties;

Output:

* Statistical result
* Automated business insight
* Market interpretation

---

### 2. Property Valuation Engine

Predicts property prices from natural-language descriptions.

Example:

"Predict a waterfront house with 4 bedrooms, 3 bathrooms, grade 10, and 3000 sqft living area."

Pipeline:

Natural Language
→ Feature Extraction
→ Feature Engineering
→ CatBoost Prediction
→ SHAP Explanation

---

### 3. Semantic Property Intelligence

Uses embedding-based retrieval to identify semantically similar properties and provide contextual market intelligence.

Applications:

* Comparable property retrieval
* Similar neighborhood discovery
* Context-aware valuation support

---

### 4. Explainable AI

Integrated SHAP analysis provides transparent model explanations.

Outputs:

* Top contributing features
* Positive and negative valuation drivers
* Human-readable reasoning

Example Drivers:

* Waterfront
* Grade
* Total Square Footage
* Geographic Location
* Property Age

---

### 5. Counterfactual Analysis

Supports scenario-based valuation analysis.

Example Questions:

* What if the property were renovated?
* What if grade increased from 8 to 10?
* What if living area increased to 3500 sqft?

Output:

* Original Valuation
* Updated Valuation
* Estimated Impact

---

## Machine Learning Pipeline

### Feature Engineering

30+ engineered features including:

* Total Square Footage
* Grade × Area Interactions
* Bathroom-to-Bedroom Ratios
* Age-Based Features
* Location-Based Features
* Neighborhood Aggregates

### Model

CatBoost Regressor

Reasons:

* Handles heterogeneous feature types
* Strong performance on tabular data
* Robust to feature interactions
* Minimal preprocessing requirements

---

## Explainability

SHAP (SHapley Additive exPlanations)

Provides:

* Local explanations
* Feature attribution
* Model transparency
* Valuation-driver analysis

---

## Technology Stack

### LLM & NLP

* OpenRouter
* Gemini / LLM APIs
* Prompt Engineering
* Structured Output Generation

### Machine Learning

* CatBoost
* SHAP
* Scikit-Learn
* Optuna

### Analytics

* SQLite
* Pandas
* NumPy

### Retrieval & Search

* Embeddings
* Semantic Retrieval
* Similarity Search

### Visualization

* Matplotlib
* Streamlit

---

## Key Features

✓ Natural-Language Analytics

✓ Text-to-SQL Generation

✓ Property Valuation

✓ Semantic Property Retrieval

✓ SHAP Explainability

✓ Counterfactual Simulation

✓ Conversational Interface

✓ Investment Decision Support

---

## Future Improvements

* Multi-agent planning workflows
* Advanced retrieval and re-ranking
* Geographic visualization
* Real-time property feeds
* Portfolio-level investment analysis
* Reinforcement learning-based recommendation systems

---

## Project Impact

Real Estate Intelligence Copilot demonstrates how LLMs, machine learning, explainable AI, and retrieval systems can be combined to create an end-to-end decision intelligence platform for real-estate analytics and valuation.
