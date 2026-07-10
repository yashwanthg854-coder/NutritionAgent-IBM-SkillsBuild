# 🥗 AI-Powered Nutrition Agent

**Personalized Dietary Guidance System built on IBM watsonx.ai & Granite Models**

*"Exploring the Power of Agentic AI with IBM Cloud and Orchestrate"*

[![IBM SkillsBuild](https://img.shields.io/badge/IBM-SkillsBuild-052FAD?style=flat-square&logo=ibm)](https://skillsbuild.org)
[![Domain](https://img.shields.io/badge/Domain-Healthcare-blue?style=flat-square)]()
[![Tech](https://img.shields.io/badge/Tech-Agentic%20AI%20%2F%20Multi--Agent-teal?style=flat-square)]()

> IBM SkillsBuild × Edunet Foundation × AICTE — University Engagement Program 2026

---

## 📌 Overview

The **AI-Powered Nutrition Agent** is a multi-agent, agentic AI system that delivers personalized, real-time dietary guidance for individuals, families, and health professionals. It combines **Retrieval-Augmented Generation (RAG)** with **IBM watsonx Orchestrate** and **IBM Granite models** to move beyond static diet advice into an adaptive, context-aware digital nutritionist.

### The Problem

Good nutrition is the foundation of health, but people struggle with diet planning, portion control, and tracking intake — and reliable, personalized guidance is scattered and hard to find.

### The Solution

An intelligent nutrition assistant that recommends meals, retrieves verified nutrition data, tracks food logs, and gives preventive health advice — all through natural conversation.

---

## ✨ Features

- **Personalized Diet Plans** — Meal recommendations based on age, health conditions, allergies, cultural preferences, and fitness goals
- **RAG-Based Food Data Retrieval** — Fetches and summarizes accurate nutritional values (calories, macros, vitamins) from trusted USDA & WHO sources
- **Diet Tracking & Feedback** — Log meals via text, voice, or images and get instant nutritional analysis
- **Preventive Health Focus** — Disease-specific diet suggestions (e.g., diabetes-friendly, heart-healthy plans)
- **Multi-Modal Input** — Supports text, voice, and image-based meal logging
- **Real-Time Adaptation** — Continuously updates suggestions based on daily meal logs
- **Nutritional Dashboard** — Visualizes daily/weekly calorie and macro intake with AI-generated suggestions

---

## 🧠 Multi-Agent Architecture

The system uses four specialized agents orchestrated together rather than a single chatbot:

| Agent | Responsibility |
|---|---|
| **Nutrition Knowledge Agent** | Retrieves and summarizes nutritional information using RAG |
| **Diet Recommendation Agent** | Generates personalized meal plans from user inputs (age, conditions, preferences, goals) |
| **Health Advisory Agent** | Provides preventive health suggestions and disease-specific diets |
| **Food Log & Feedback Agent** | Logs meals via text/voice/image and delivers instant nutritional feedback |

### Architecture Blueprint

```
Text / Voice / Image Input
        │
        ▼
IBM watsonx Orchestrate (LangFlow)
        │
        ▼
┌───────────────────────────────────────────┐
│ Nutrition Knowledge Agent  │ Diet Recommendation Agent │
│ Health Advisory Agent      │ Food Log & Feedback Agent │
└───────────────────────────────────────────┘
        │
        ▼
Vector DB (FAISS/Chroma) + USDA/WHO  ──  IBM Granite Models
        │
        ▼
Output: Personalized Meal Plans | Nutritional Analysis |
        Health Advice | Food Log Summary

Deployed on IBM Cloud Lite
```

**Agentic AI capabilities:**
- **Context Awareness** — understands user age, health conditions, and fitness goals
- **Real-Time Adaptation** — updates suggestions based on daily meal logs
- **Inter-Agent Communication** — agents collaborate for better decisions
- **Goal-Driven Behavior** — proactive and personalized, not just reactive

---

## 🛠️ Tech Stack

| Component | Purpose |
|---|---|
| **IBM Granite Models** (`granite-3.2-8b-instruct`) | Natural language understanding, reasoning, personalization |
| **IBM watsonx.ai** | Model deployment, embeddings, AI governance |
| **IBM watsonx Orchestrate** | Agent orchestration and workflow management |
| **IBM Cloud (Lite)** | Scalable, secure infrastructure for deployment |
| **LangFlow** | Orchestration pipeline for agent workflows |
| **RAG (Retrieval-Augmented Generation)** | Fetches verified real-time nutrition data before generation |
| **Vector Database (FAISS / Chroma)** | Stores/indexes USDA Food Data Central & WHO guidelines for semantic search |
| **Streamlit / React** | Dashboard visualizing daily & weekly nutrient intake |

### watsonx Orchestrate Components Used
1. Chat Input Component — text/voice/image query entry
2. watsonx Orchestrate AI Agent — processes input via Granite models
3. Granite Model (`granite-3.2-8b-instruct`) — fast, real-time diet reasoning
4. Chat Output Component — displays diet plans, analysis, and suggestions
5. Knowledge Base / File Component — stores user data, meal logs, nutrition datasets
6. LangFlow Orchestration Pipeline — ties all agents together

---

## 🚀 Quick Start

### Prerequisites
- IBM Cloud account (Lite tier is sufficient)
- Access to IBM watsonx.ai / watsonx Orchestrate
- Python 3.9+ (if running the dashboard/RAG pipeline locally)

### Setup

1. **Clone the repository**
   ```bash
   git clone https://github.com/yashwanthg854-coder/NutritionAgent-IBM-SkillsBuild.git
   cd NutritionAgent-IBM-SkillsBuild
   ```

2. **Set up IBM watsonx Orchestrate**
   - Create a new Agent in watsonx Orchestrate
   - Set the **Agent Behavior Guidelines** (see `/docs` or presentation for the exact prompt)
   - Add a **Knowledge Source**: upload USDA/WHO nutrition datasets (PDF, DOCX, TXT, or CSV) or connect a Vector Database (FAISS/Chroma)
   - Select the Granite model: `granite-3.2-8b-instruct`
   - Save the agent

3. **(Optional) Run the dashboard locally**
   ```bash
   pip install -r requirements.txt
   streamlit run app.py
   ```

4. **Try it out**
   Ask the agent things like:
   - *"Suggest a diabetic-friendly dinner"*
   - *"Calculate calories for my meal"*
   - *"Create a 7-day weight-loss plan"*
   - *"Create a vegetarian weight-gain meal plan with calorie targets and macro splits"*

### Example Output
```
Nutrition Agent:
Here's your 7-Day Vegetarian Weight Gain Plan:

Daily Calorie Target: 2,800–3,000 kcal
Protein: 140g | Carbs: 350g | Fats: 90g

Day 1 – Sample Menu:
Breakfast: Oats + banana + peanut butter smoothie (620 kcal)
Lunch: Paneer tikka + brown rice + dal (780 kcal)
Snack: Mixed nuts + Greek yogurt (310 kcal)
Dinner: Tofu stir-fry + quinoa + avocado salad (730 kcal)

Source: USDA Food Data Central | WHO Protein Guidelines 2023
```

---

## 🌟 Novelty & Uniqueness

- **Multi-Agent Intelligence** instead of a single chatbot
- **RAG-Based Accuracy** reducing misinformation
- **Hyper-Personalization** based on health, culture, and goals
- **Real-Time Feedback Loop** from daily food logs
- **Multi-Modal Input** (text, voice, image)
- **Preventive Healthcare Focus**, not just diet planning
- **Enterprise-ready**, built on IBM watsonx.ai & Granite

---

## 🔮 Future Scope

1. **Wearables & Health Device Integration** — real-time steps, heart rate, sleep data
2. **AI Voice Assistant & Multilingual Support** — broader accessibility
3. **Predictive Health Analytics** — long-term dietary pattern analysis for disease prevention
4. **Community & Social Integration** — shared meal plans, recipes, and peer motivation

---

## 👤 Author

**Yashwanth Kumar H C**


if you found this project useful, consider giving it a ⭐ on GitHub.
- 📧 yashwanthg854@gmail.com
- 🔗 [LinkedIn](https://linkedin.com/in/yashwanth-kumar-h-c-3aabb8307)
- 💻 [GitHub](https://github.com/yashwanthg854-coder)

---

## 🏫 Program

IBM SkillsBuild × Edunet Foundation × AICTE University Engagement Program 2026

---

## 📄 License

This project was developed as part of an academic internship program. Please contact the author for reuse permissions.
