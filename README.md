# Natural Language Processing Laboratory

## Setup and Installation Guide

### 1. Create and activate a virtual environment (recommended)

#### Mac / Linux
```bash
python3 -m venv venv
source venv/bin/activate
```

#### Windows
```bash
python -m venv venv
venv\Scripts\activate
```

---

### 2. Install dependencies

The required packages are listed in `requirements.txt`.  
It also includes the spaCy model (`en_core_web_sm`) via a wheel URL, so no separate model download is required.

```bash
pip install -r requirements.txt
```

If you still want to manually download the spaCy model (not required unless the wheel URL fails), you can run:

```bash
python -m spacy download en_core_web_sm
```

---

### 3. Verify spaCy model installation (optional)

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

### 4. Notes on Reproducibility

- The intended Python version is recorded inside `requirements.txt` as a comment:
  ```
  # python==3.12.12
  ```
  This does not interfere with `pip install -r requirements.txt` but keeps the environment specification clear.

- All external dependencies, including the spaCy model, are installed automatically using step 2.

---

### 5. Run the project

- The jupyter notebook `NLP_Complete.ipynb` in `/english` directory contains the code for the complete project.
