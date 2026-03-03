# Enhanced-SLD-Threat-Classifier-with-Typosquat-Homoglyph-Detection
🔐 Overview
Cyber attackers frequently exploit typosquatting and homoglyph attacks to impersonate trusted domains (e.g., g00gle.com, arnazon.com).
This project implements a Second-Level Domain (SLD) Threat Classification System enhanced with:
🔎 Typosquat Detection
🌍 Homoglyph Attack Detection
📊 Risk Scoring Mechanism
🏦 Verified Domain Comparison (10K+ bank URLs dataset)
The system is designed to proactively detect suspicious domains and prevent phishing attacks.
🚨 Problem Statement
Traditional domain filtering systems often fail to detect:
Minor character substitutions (o → 0)
Unicode homoglyph attacks (a → а)
Slight misspellings of trusted brands
These attacks bypass naive string-matching systems and pose serious cybersecurity risks.
🏗️ System Architecture
Input Domain
     ↓
Domain Preprocessing
     ↓
SLD Extraction
     ↓
Feature Engineering
     ↓
Typosquat Detection
     ↓
Homoglyph Detection
     ↓
Threat Classification Model
     ↓
Risk Score Output
🧠 Core Features
✅ 1. SLD Extraction
Extracts and normalizes second-level domain for accurate analysis.
✅ 2. Typosquat Detection
Levenshtein distance analysis
Character substitution detection
Brand similarity scoring
✅ 3. Homoglyph Detection
Unicode normalization
Detection of visually similar characters
Script mixing identification
✅ 4. Threat Classification
Machine learning based scoring
Risk categorization (Low / Medium / High)
🛠️ Tech Stack
Python 3.x
Scikit-learn
Pandas
Regex
Unicode Normalization
Custom Heuristic Detection Algorithms
📂 Project Structure
.
├── patched_domain_extractor_app.py
├── verified_bank_urls_10k.csv
├── requirements.txt
└── README.md
▶️ Installation
git clone https://github.com/ankitpremi12/Enhanced-SLD-Threat-Classifier-with-Typosquat-Homoglyph-Detection.git
cd Enhanced-SLD-Threat-Classifier-with-Typosquat-Homoglyph-Detection
pip install -r requirements.txt
🚀 Usage
python patched_domain_extractor_app.py
Example:
Input:
g00gle-secure-login.com
Output:
⚠️ High Risk Domain
Typosquat detected
Possible homoglyph usage
Risk Score: 0.91
📊 Dataset
10,000+ verified banking URLs
Used as trusted baseline comparison
Helps detect brand impersonation attempts
📈 Potential Improvements
Deep Learning based domain embeddings
Real-time API deployment
Integration with browser extension
SIEM integration for enterprise security
🎯 Use Cases
Phishing detection systems
Financial institution security
SOC automation
Domain monitoring services
👨‍💻 Author
Ankit Premi
AI/ML Engineer | Cybersecurity Enthusiast
