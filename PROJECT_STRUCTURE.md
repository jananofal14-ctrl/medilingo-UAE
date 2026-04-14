# MediLingo UAE Project Structure

This is the organized folder flow to keep the project maintainable.

## Root
- `run.py`: backend startup entrypoint
- `README.md`: quickstart
- `PROJECT_STRUCTURE.md`: folder conventions (this file)

## Backend (`backend/`)
- `app.py`: Flask app creation and route registration
- `config.py`: global backend configuration
- `requirements.txt`: Python dependencies
- `routes/`: API endpoints
  - `auth_routes.py`
  - `translation_routes.py`
  - `diagnosis_routes.py`
- `services/`: business logic
  - auth, translation, diagnosis, summary, ASR, dataset services
- `models/`: model definitions and shared label constants
  - `xray_model.py`
  - `translation_model.py`
  - `class_labels.py`
- `utils/`: helper utilities
- `training/`: model training/evaluation scripts
  - `train_translation.py`, `evaluate_translation.py`
  - `train_xray.py`, `evaluate_xray.py`
- `trained_models/`
  - `translation/` (Marian tokenizer/config/model files)
  - `xray/` (`densenet121_xray_21.pth`)
- `data/`: runtime data (SQLite DB, temporary data)

## Mobile (`mobile/`)
- `App.js`: app shell and tab flow
- `src/screens/`: `AuthScreen`, `TranslatorScreen`, `DiagnosisScreen`
- `src/services/api.js`: API client methods
- `src/theme.js`: blue/green design tokens

## Datasets (`datasets/`)
- `translation/`
  - `medical_ar_en.csv`
  - `medical_ar_en_extended.csv`
- `xray/`
  - `chest_xray_metadata.csv`
  - `chest_xray_training_manifest.csv`
  - `chest_xray_diseases_master.csv`
- `TRAINING_DATASETS.md`: dataset documentation

## Conventions
- Keep API logic in `backend/routes/` only.
- Keep model/runtime logic in `backend/services/`.
- Keep training-only code in `backend/training/`.
- Keep dataset files as CSV only under `datasets/`.
- Keep model artifacts only under `backend/trained_models/`.
