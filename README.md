# Project Setup and Installation Guide

## 1. Create and activate a virtual environment (recommended)

### Mac / Linux
```bash
python3 -m venv venv
source venv/bin/activate
```

### Windows
```bash
python -m venv venv
venv\Scripts\activate
```

---

## 2. Install dependencies

The required packages are listed in `requirements.txt`.  
It also includes the spaCy model (`en_core_web_sm`) via a wheel URL, so no separate model download is required.

```bash
pip install -r requirements.txt
```

---

## 3. Verify spaCy model installation (optional)

```bash
python - << 'EOF'
import spacy
nlp = spacy.load("en_core_web_sm")
print("spaCy model loaded successfully.")
EOF
```

Expected output:

```
spaCy model loaded successfully.
```

---

## 4. Notes on Reproducibility

- Python version is documented inside `requirements.txt` as a comment:
  ```
  # python==3.12.12
  ```
  This does not interfere with dependency installation but ensures clarity on the intended environment.

- All external dependencies, including the spaCy model, are installed automatically using step 2.

---

## 5. Run the project

Replace `your_script.py` with your main file:

```bash
python nlp_project.py
```
