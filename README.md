# MediLingo UAE

MediLingo UAE is an AI-powered medical web application that combines:

1. Real-time Arabic-English medical translation
2. Smart chest X-ray diagnosis

## Features
- Doctor-patient bilingual communication
- Speech-to-text using Whisper
- Medical-aware translation
- X-ray disease prediction
- Clinical summary generation

## Tech Stack
- Frontend: HTML, CSS, JavaScript
- Mobile: React Native (Expo)
- Backend: Flask
- AI/NLP: Whisper, MarianMT
- CV: DenseNet121, PyTorch

## Run Backend

    pip install -r backend/requirements.txt
    python run.py

## Run Mobile App

    cd mobile
    npm install
    npm run start

## Project Organization

- Folder guide: `PROJECT_STRUCTURE.md`
- Backend API routes: `backend/routes/`
- Backend AI/business logic: `backend/services/`
- Training scripts: `backend/training/`
- Datasets: `datasets/`

## Training Commands

    python backend/training/train_translation.py
    python backend/training/train_xray.py
    python backend/training/run_all.py

## Training Data

- Translation datasets: `datasets/translation/medical_ar_en.csv` and `datasets/translation/medical_ar_en_extended.csv`
- X-ray datasets: `datasets/xray/chest_xray_metadata.csv` and `datasets/xray/chest_xray_training_manifest.csv`
- Dataset guide: `datasets/TRAINING_DATASETS.md`