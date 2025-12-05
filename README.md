# SAHAY — AI-Powered Youth Mental Wellness Companion

## Overview

SAHAY is an AI-driven mental wellness companion designed to provide confidential, empathetic, and culturally relevant support to young people in India. The platform is built to address the stigma and limited access associated with traditional mental health services. It offers a safe space for students and youth to express concerns, engage in guided self-help practices, and access curated mental health resources.

This prototype demonstrates the core functionality of the system using Google Cloud’s generative AI tools, including Gemini, Vertex AI, and supporting services.

---

## Key Features

* **Confidential Chat Interface:** Allows users to communicate securely with an AI assistant trained for empathetic and safe conversations.
* **Coping Toolkit:** Includes simple exercises such as breathing prompts, grounding activities, and daily check-ins.
* **Localized Support:** Conversations tailored to English and Hinglish to improve relatability.
* **Resource Recommendations:** Provides structured guidance and links to verified educational or crisis resources.
* **Safety Layer:** Includes basic crisis-detection logic to redirect users toward professional help when needed.
* **Prototype Backend:** Minimal Flask API to simulate interaction with generative AI.

---

## Project Structure

```
sahay_prototype/
├── frontend/
│   └── App.js
├── backend/
│   ├── app.py
│   └── db/
│       └── firestore_utils.py
```

---

## Requirements

* Python 3.9+
* Node.js 16+
* Google Cloud project with Firestore enabled
* Service account key for Firestore access
* Basic React and Flask setup

---

## Setup Instructions

### 1. Frontend Setup

```
cd frontend
npm install
npm start
```

This launches the frontend on `http://localhost:3000`.

### 2. Backend Setup

```
cd backend
python -m venv venv
source venv/bin/activate     # Windows: venv\Scripts\activate
pip install flask google-cloud-firestore
python app.py
```

Backend runs on `http://127.0.0.1:5000`.

### 3. Firestore Configuration

* Enable Firestore in Google Cloud.
* Place your service account key in the backend folder.
* Set the following environment variable:

```
export GOOGLE_APPLICATION_CREDENTIALS="service-account.json"
```

---

## Deployment

### Backend (Google Cloud Run)

```
gcloud builds submit --tag gcr.io/[PROJECT-ID]/sahay-backend
gcloud run deploy sahay-backend --image gcr.io/[PROJECT-ID]/sahay-backend --platform managed
```

### Frontend (Firebase Hosting or any static host)

```
firebase init hosting
firebase deploy
```

---

## Current Prototype Capabilities

* Basic chat with placeholder AI responses
* Minimal wellness prompts
* Firestore message logging function
* Working frontend and backend integration structure

---

## Future Enhancements

* Integration with Vertex AI Gemini for full conversational capability
* Multi-language support
* Advanced safety and crisis-handling workflows
* User profile insights and mood tracking
* Expanded library of wellness exercises
* Voice and multimedia interaction

---
