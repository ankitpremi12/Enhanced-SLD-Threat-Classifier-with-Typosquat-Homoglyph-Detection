# 🔐 Enhanced SLD Threat Classifier with Typosquat & Homoglyph Detection

> A Second-Level Domain (SLD) Threat Classification System that proactively detects suspicious domains and prevents phishing attacks.

---

## 🧠 Overview

Cyber attackers frequently exploit **typosquatting** and **homoglyph attacks** to impersonate trusted domains (e.g., `g00gle.com`, `arnazon.com`). This project implements an intelligent SLD Threat Classification System enhanced with:

- 🔍 **Typosquat Detection**
- 🌐 **Homoglyph Attack Detection**
- 📊 **Risk Scoring Mechanism**
- 🏦 **Verified Domain Comparison** *(10K+ bank URLs dataset)*

---

## ❗ Problem Statement

Traditional domain filtering systems often fail to detect:

- Minor character substitutions (`o → 0`)
- Unicode homoglyph attacks (`а → a`)
- Slight misspellings of trusted brands

These attacks bypass naïve string-matching systems and pose serious cybersecurity risks.

---

## 🏗️ System Architecture

```
Input Domain
     ↓
Domain Preprocessing
     ↓
SLD Extraction
     ↓
Feature Engineering
     ↓
Typosquat Detection ──── Homoglyph Detection
     ↓                          ↓
          Threat Classification Model
                    ↓
              Risk Score Output
```

---

## ✅ Core Features

### 1. 🔤 SLD Extraction
Extracts and normalizes second-level domains for accurate analysis.

### 2. 🔁 Typosquat Detection
- Levenshtein distance analysis
- Character substitution detection
- Brand similarity scoring

### 3. 🔡 Homoglyph Detection
- Unicode normalization
- Detection of visually similar characters
- Script mixing identification

### 4. 🤖 Threat Classification
- Machine learning based scoring
- Risk categorization: **Low / Medium / High**

---

## 🛠️ Tech Stack

| Technology | Purpose |
|---|---|
| Python 3.x | Core language |
| Scikit-learn | ML classification |
| Pandas | Data handling |
| Regex | Pattern matching |
| Unicode Normalization | Homoglyph detection |
| Custom Heuristics | Domain analysis |

---

## 📁 Project Structure

```
Enhanced-SLD-Threat-Classifier-with-Typosquat-Homoglyph-Detection/
├── patched_domain_extractor_app.py   # Main application
├── verified_bank_urls_10k.csv        # Trusted domain baseline dataset
├── requirements.txt                  # Dependencies
└── README.md
```

---

## 🚀 Installation

```bash
# Clone the repository
git clone https://github.com/ankitpremi12/Enhanced-SLD-Threat-Classifier-with-Typosquat-Homoglyph-Detection.git

# Navigate into the directory
cd Enhanced-SLD-Threat-Classifier-with-Typosquat-Homoglyph-Detection

# Install dependencies
pip install -r requirements.txt
```

---

## 💻 Usage

```bash
python patched_domain_extractor_app.py
```

### Example

**Input:** `g00gle-secure-login.com`

**Output:**
```
⚠️  Risk Level   : HIGH
🔁  Typosquat    : Detected
🔡  Homoglyph    : Possible usage detected
📊  Risk Score   : 0.91
```

---

## 📊 Dataset

- **10,000+** verified banking URLs
- Used as trusted baseline for comparison
- Helps detect brand impersonation attempts

---

## 🔮 Potential Improvements

- [ ] Deep Learning based domain embeddings
- [ ] Real-time API deployment
- [ ] Browser extension integration
- [ ] SIEM integration for enterprise security

---

## 🎯 Use Cases

- 🛡️ Phishing detection systems
- 🏦 Financial institution security
- 🖥️ SOC automation
- 🌐 Domain monitoring services

---

## 👤 Author

**Ankit Premi**  
AI/ML Engineer | Cybersecurity Enthusiast

[![GitHub](https://img.shields.io/badge/GitHub-ankitpremi12-181717?style=flat&logo=github)](https://github.com/ankitpremi12)
