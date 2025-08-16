<p align="center">
  <img src="screenshots/kriya_banner.png" alt="Kriya Banner" width="500"/>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.10-blue.svg" />
  <img src="https://img.shields.io/badge/API-Google%20Vision-yellow" />
  <img src="https://img.shields.io/badge/LLM-Groq%20API-purple" />
</p>

# OCR-Multilingual – Voter List OCR for Hindi, Kannada, and English



## Problem
In India, voter lists are often published as scanned images or PDFs in regional languages like Hindi and Kannada. Manual data entry from these documents is tedious, error-prone, and unscalable — especially when schema consistency is required for downstream analytics or government integrations.

## Solution
OCR-Multilingual is a Python-based tool that extracts structured voter data from image-based lists in **Hindi, Kannada, and English**. It ensures output is **Excel-safe**, **schema-aligned**, and **field-preserving** — supporting digitization efforts with minimal human correction.

## Key Features
- 📄 Supports Hindi, Kannada, and English voter lists
- ✅ Aligns exactly with required CSV schema
- 🧠 Combines OCR + LLM post-processing for higher accuracy
- ⚠️ Flags malformed rows for manual traceability


## Tech Stack
- Python 3.10+
- Google Vision AI API (OCR)
- Groq API (LLM post-processing)
- Pandas, OpenCV, regex
- `openpyxl` for Excel-safe output

<p align="center">
  <img src="screenshots/tech_stack.png" alt="Tech Stack Overview" width="500"/>
</p>

## Architecture
```mermaid
flowchart LR
    A["Scanned Image"] --> B["OCR Engine (Google Vision API)"]
    B --> C["LLM Post-Processor (Groq API)"]
    C --> D["CSV Schema Aligner"]
    D --> E["Excel Output (openpyxl)"]




