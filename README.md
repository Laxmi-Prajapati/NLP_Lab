# Natural Language Processing Laboratory

Installation & Setup

Follow the steps below to set up the environment and run the project.

1. Create and activate a virtual environment (recommended)
python3 -m venv venv
source venv/bin/activate        # Mac / Linux
venv\Scripts\activate           # Windows

2. Install dependencies

This will automatically install the spaCy model (en_core_web_sm) because the wheel URL is included in requirements.txt.

pip install -r requirements.txt


No additional model download command is required.

3. Verify spaCy model installation (optional)
python - << 'EOF'
import spacy
nlp = spacy.load("en_core_web_sm")
print("spaCy model loaded successfully.")
EOF


Expected output:

spaCy model loaded successfully.

Notes on Reproducibility

The correct Python version is documented inside requirements.txt as a comment:

# python==3.12.12


This ensures environment reproducibility without causing installation errors.

All dependencies, including the spaCy model, are installed during step 2.

Run the project
python your_script.py

This text can be pasted directly into README.md
