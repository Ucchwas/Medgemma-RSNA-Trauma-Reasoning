# MedGemma RSNA Trauma Reasoning

This repo contains a notebook that uses **MedGemma** to generate **radiology-style clinical reasoning** from **RSNA 2023 Abdominal Trauma Detection** sample slices (e.g., YOLO ROI images such as `val_batch*_pred.jpg`).

> ⚠️ **Medical safety disclaimer:** This project is for research and educational purposes only. It is **not** a diagnostic device and must not be used for clinical decision-making.

---

## What this does
- Loads a MedGemma multimodal model (image + text prompting)
- Reads abdominal CT slice images (often pre-rendered ROI/batch images)
- Prompts the model with a structured “radiologist mode” instruction
- Generates a clinical-style report for each sample image

---

## Dataset
This notebook expects the **RSNA 2023 Abdominal Trauma Detection** dataset (Kaggle competition dataset)

---

## Expected output
For each selected sample image, the notebook prints a generated report similar to:
- Organ identification (based on ROI boxes)
- Findings (density changes, lacerations, fluid)
- A short conclusion / suspected injury grade (model-generated)
