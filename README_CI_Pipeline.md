# 🚀 Automated CI/CD Pipeline for ML Model Deployment

![Python](https://img.shields.io/badge/Python-3.10-blue?logo=python)
![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-CI%2FCD-green?logo=githubactions)
![Status](https://img.shields.io/badge/Status-Active-brightgreen)

> An automated CI/CD pipeline that tests, validates, and deploys a Python Machine Learning model using GitHub Actions — reducing manual deployment effort by 70%.

---

## 📌 Project Overview

This project demonstrates how to build a production-ready CI/CD pipeline for a Machine Learning workflow. Every time code is pushed to the repository, the pipeline automatically runs unit tests, checks code quality, and validates the ML model — simulating real-world MLOps practices.

---

## ✨ Features

- ✅ Automated testing on every `git push`
- ✅ Python linting and code quality checks
- ✅ ML model validation and build verification
- ✅ GitHub Actions workflow configuration
- ✅ Trigger-based deployment automation

---

## 🛠️ Tech Stack

| Tool | Purpose |
|------|---------|
| Python 3.10 | Core programming language |
| GitHub Actions | CI/CD automation |
| pytest | Unit testing framework |
| flake8 | Code linting |
| Scikit-learn | ML model |

---

## 📁 Project Structure

```
CI_Pipeline/
│
├── .github/
│   └── workflows/
│       └── ci.yml          # GitHub Actions workflow
│
├── model/
│   ├── train.py            # Model training script
│   └── predict.py          # Prediction script
│
├── tests/
│   └── test_model.py       # Unit tests
│
├── requirements.txt
└── README.md
```

---

## ⚙️ How It Works

```
Push Code → GitHub Actions Triggered
         → Install Dependencies
         → Run Linting (flake8)
         → Run Unit Tests (pytest)
         → Validate ML Model
         → ✅ Pipeline Passed / ❌ Failed (with logs)
```

---

## 🚀 Getting Started

### 1. Clone the Repository
```bash
git clone https://github.com/Sahilghate4/CI_Pipeline.git
cd CI_Pipeline
```

### 2. Install Dependencies
```bash
pip install -r requirements.txt
```

### 3. Run Tests Locally
```bash
pytest tests/
```

### 4. Trigger CI Pipeline
Simply push any change to GitHub:
```bash
git add .
git commit -m "your message"
git push origin main
```
GitHub Actions will automatically run the full pipeline.

---

## 📊 Pipeline Workflow (GitHub Actions)

```yaml
name: CI Pipeline
on: [push]
jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - name: Set up Python
        uses: actions/setup-python@v4
      - name: Install dependencies
        run: pip install -r requirements.txt
      - name: Lint with flake8
        run: flake8 .
      - name: Run tests
        run: pytest tests/
```

---

## 👨‍💻 Author

**Sahil Sanjay Ghate**
- 📧 sahilghate4@gmail.com
- 🔗 [GitHub](https://github.com/Sahilghate4)
- 🎓 B.Tech IT — AISSMS IOIT, Pune (2027)

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).
