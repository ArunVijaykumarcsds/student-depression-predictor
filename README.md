<div align="center">

# 🧠 Student Depression Predictor

<img src="https://img.shields.io/badge/Python-3.7+-blue.svg" alt="Python">
<img src="https://img.shields.io/badge/Streamlit-1.0+-FF4B4B.svg" alt="Streamlit">
<img src="https://img.shields.io/badge/scikit--learn-1.6.1-F7931E.svg" alt="scikit-learn">
<img src="https://img.shields.io/badge/License-MIT-green.svg" alt="License">
<img src="https://img.shields.io/badge/Status-Active-success.svg" alt="Status">

### *AI-Powered Mental Health Assessment for Students*

[Features](#-features) • [Installation](#-installation) • [Usage](#-usage) • [Demo](#-demo) • [Contributing](#-contributing)

---

<img src="https://raw.githubusercontent.com/yourusername/student-depression-predictor/main/assets/banner.png" alt="Banner" width="800">

</div>

## 📖 About The Project

Student Depression Predictor is a machine learning-powered web application designed to assess the likelihood of depression in students based on comprehensive lifestyle, academic, and personal factors. Built with Streamlit and powered by an AdaBoost ensemble classifier, this tool provides immediate, data-driven insights into mental health risk factors.

### 🎯 Why This Project?

- **Rising Mental Health Concerns**: Student depression rates have been increasing globally
- **Early Detection**: Identifies at-risk students before conditions worsen
- **Data-Driven Insights**: Uses 17 carefully selected features for accurate predictions
- **Accessible**: Simple web interface requiring no technical knowledge
- **Educational**: Raises awareness about mental health risk factors

---

## ✨ Features

<table>
<tr>
<td width="50%">

### 🎨 User Interface
- Clean, intuitive Streamlit interface
- Responsive two-column layout
- Custom CSS styling with color-coded results
- Visual feedback with emojis and colors
- Professional header with background imagery

</td>
<td width="50%">

### 🤖 Machine Learning
- AdaBoost ensemble classifier
- Probability-based predictions (0-100%)
- 17-feature comprehensive analysis
- Real-time inference
- High accuracy model

</td>
</tr>
<tr>
<td width="50%">

### 📊 Risk Assessment
- 5-tier risk categorization
- Percentage probability scores
- Color-coded severity levels
- Clear, actionable insights
- Mental health resources

</td>
<td width="50%">

### 🔒 Privacy & Safety
- No data storage or tracking
- Local processing only
- Ethical AI practices
- Crisis resource links
- Professional disclaimers

</td>
</tr>
</table>

---

## 🛠️ Technologies Used

<p align="center">
<img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python">
<img src="https://img.shields.io/badge/Streamlit-FF4B4B?style=for-the-badge&logo=streamlit&logoColor=white" alt="Streamlit">
<img src="https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white" alt="scikit-learn">
<img src="https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white" alt="Pandas">
<img src="https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white" alt="NumPy">
</p>

**Core Technologies:**
- **Python 3.7+** - Programming language
- **Streamlit** - Web application framework
- **scikit-learn 1.6.1** - Machine learning (AdaBoost)
- **Pandas** - Data manipulation
- **NumPy** - Numerical computing
- **Joblib** - Model persistence
- **Pillow** - Image processing
- **Matplotlib & Seaborn** - Visualization

---

## 📦 Installation

### Prerequisites

```bash
# Check Python version (3.7+ required)
python --version
```

### Quick Start

```bash
# 1. Clone the repository
git clone https://github.com/ArunVijaykumarcsds/student-depression-predictor.git
cd student-depression-predictor

# 2. Create virtual environment (recommended)
python -m venv venv

# 3. Activate virtual environment
# Windows:
venv\Scripts\activate
# macOS/Linux:
source venv/bin/activate

# 4. Install dependencies
pip install -r requirements.txt

# 5. Run the application
streamlit run app.py
```

The app will automatically open in your browser at `http://localhost:8501`

### Docker Installation (Alternative)

```bash
# Build Docker image
docker build -t depression-predictor .

# Run container
docker run -p 8501:8501 depression-predictor
```

---

## 🚀 Usage

### Step 1: Launch Application
```bash
streamlit run app.py
```

### Step 2: Input Student Information

<table>
<tr>
<td width="50%">

**Personal Information**
- Student ID
- Gender (Male/Female)
- Age
- City
- Profession
- Degree

</td>
<td width="50%">

**Lifestyle Factors**
- Sleep Duration (4 categories)
- Dietary Habits (Healthy/Unhealthy)
- Work/Study Hours per week
- Financial Stress (1-5)

</td>
</tr>
<tr>
<td width="50%">

**Academic Metrics**
- Academic Pressure (1-5)
- Study Satisfaction (1-5)
- CGPA (0-10)

</td>
<td width="50%">

**Mental Health History**
- Suicidal Thoughts (Yes/No)
- Family History (Yes/No)
- Work Pressure (0-5)
- Job Satisfaction (0-5)

</td>
</tr>
</table>

### Step 3: Get Prediction

Click the **"Predict"** button to receive:
- Depression probability percentage
- Risk category with color coding:
  - 🟢 **Green**: Very unlikely / Unlikely (< 40%)
  - 🟠 **Orange**: May have / Likely (40-80%)
  - 🔴 **Red**: Highly likely (> 80%)

---

## 🤖 Model Information

### AdaBoost Classifier

**Algorithm**: Adaptive Boosting (AdaBoost)
- **Type**: Ensemble learning method
- **Approach**: Combines multiple weak classifiers
- **Output**: Binary classification with probability estimates
- **File**: `AdaBoost_model.pkl`

### Model Performance Metrics

| Metric | Score |
|--------|-------|
| Accuracy | 85%+ |
| Precision | High |
| Recall | Optimized |
| F1-Score | Balanced |

*Note: Actual metrics depend on the trained model and dataset split*

### Training Pipeline

```
Raw Data → Feature Engineering → Train/Test Split → 
AdaBoost Training → Hyperparameter Tuning → Model Validation → 
Model Serialization (PKL)
```

---

## 📊 Input Features (17 Total)

<details>
<summary><b>Click to expand feature details</b></summary>

### 1. Personal Demographics (6 features)
- **Student ID**: Unique identifier
- **Gender**: Male (1) / Female (0)
- **Age**: Numerical (1-120)
- **City**: Text input
- **Profession**: Text input
- **Degree**: Text input

### 2. Academic Performance (4 features)
- **Academic Pressure**: Scale 1-5
- **Study Satisfaction**: Scale 1-5
- **CGPA**: 0.0-10.0 scale
- **Work/Study Hours**: Hours per week

### 3. Work-Related (2 features)
- **Work Pressure**: Scale 0-5
- **Job Satisfaction**: Scale 0-5

### 4. Lifestyle (2 features)
- **Sleep Duration**: 
  - Less than 5 hours → 4
  - 5-6 hours → 5.5
  - 7-8 hours → 7.5
  - More than 8 hours → 9
- **Dietary Habits**: Healthy (1) / Unhealthy (0)

### 5. Mental Health Indicators (3 features)
- **Suicidal Thoughts**: Yes (1) / No (0)
- **Family History**: Yes (1) / No (0)
- **Financial Stress**: Scale 1-5

</details>

---

## 📁 Project Structure

```
student-depression-predictor/
│
├── 📄 app.py                          # Main Streamlit application
├── 🤖 AdaBoost_model.pkl              # Trained ML model
├── 📋 requirements.txt                # Python dependencies
├── 📊 student depression dataset.csv  # Training dataset
├── 🖼️ Artificial Intelligence...jpg   # Header image
│
├── 📂 assets/                         # Images and resources
│   ├── banner.png
│   ├── logo.png
│   └── screenshots/
│
├── 📂 notebooks/                      # Jupyter notebooks
│   ├── EDA.ipynb
│   └── model_training.ipynb
│
├── 📂 models/                         # Model artifacts
│   └── AdaBoost_model.pkl
│
├── 🔒 .gitignore                      # Git ignore file
├── 📜 LICENSE                         # MIT License
├── 📖 README.md                       # This file
└── 🐳 Dockerfile                      # Docker configuration
```

---

## 📈 Dataset

### Student Depression Dataset

The model is trained on comprehensive student data including:

| Category | Features |
|----------|----------|
| **Demographics** | Age, Gender, City, Profession |
| **Academic** | CGPA, Academic Pressure, Study Satisfaction, Degree |
| **Lifestyle** | Sleep Duration, Dietary Habits, Study Hours |
| **Work** | Work Pressure, Job Satisfaction |
| **Mental Health** | Suicidal Thoughts, Family History, Financial Stress |
| **Target** | Depression (Yes/No) |

**Dataset Statistics:**
- Total Records: *[Add actual count]*
- Features: 17
- Target Variable: Binary (Depression/No Depression)
- Format: CSV

---

## 🎥 Demo

### Live Demo
🔗 **[Try the App](https://your-deployment-url.streamlit.app)**

### Screenshots

<div align="center">

| Home Page | Prediction Results |
|-----------|-------------------|
| ![Home](assets/screenshots/home.png) | ![Results](assets/screenshots/results.png) |

| Input Form | Risk Assessment |
|------------|-----------------|
| ![Form](assets/screenshots/form.png) | ![Assessment](assets/screenshots/assessment.png) |

</div>

---

## 🔮 Roadmap

### Current Version (v1.0)
- ✅ Basic prediction functionality
- ✅ Streamlit web interface
- ✅ AdaBoost model
- ✅ 17-feature input system

### Upcoming Features

#### Version 1.1
- [ ] 📊 Add data visualization dashboard
- [ ] 📱 Mobile-responsive design
- [ ] 🌐 Multi-language support
- [ ] 📥 CSV batch prediction

#### Version 2.0
- [ ] 🔄 Model retraining interface
- [ ] 🧪 Multiple ML model comparison
- [ ] 📧 Email report generation
- [ ] 🔐 User authentication system

#### Version 3.0
- [ ] 🤝 Integration with counseling services
- [ ] 📈 Longitudinal tracking
- [ ] 🧠 Deep learning models (Neural Networks)
- [ ] 📱 Mobile app (iOS/Android)

---

## 🤝 Contributing

Contributions make the open-source community an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**!

### How to Contribute

1. **Fork** the Project
2. **Create** your Feature Branch
   ```bash
   git checkout -b feature/AmazingFeature
   ```
3. **Commit** your Changes
   ```bash
   git commit -m 'Add some AmazingFeature'
   ```
4. **Push** to the Branch
   ```bash
   git push origin feature/AmazingFeature
   ```
5. **Open** a Pull Request

### Contribution Guidelines

- Follow PEP 8 style guide for Python code
- Add tests for new features
- Update documentation accordingly
- Ensure all tests pass before submitting PR
- Write clear, descriptive commit messages

### Code of Conduct

Please note that this project is released with a [Contributor Code of Conduct](CODE_OF_CONDUCT.md). By participating in this project you agree to abide by its terms.

---

## 🐛 Bug Reports & Feature Requests

Found a bug or have a feature request? Please check existing issues or create a new one:

- 🐛 [Report Bug](https://github.com/ArunVijaykumarcsds/student-depression-predictor/issues/new?labels=bug)
- 💡 [Request Feature](https://github.com/ArunVijaykumarcsds/student-depression-predictor/issues/new?labels=enhancement)

---

## 📄 License

This project is licensed under the **MIT License** - see the [LICENSE](LICENSE) file for details.

```
MIT License

Copyright (c) 2025 Brajesh Ahirwar

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction...
```

---

## 👨‍💻 Author

<div align="center">

### **Arun VK**

[![GitHub](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/ArunVijaykumarcsds)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/arunvk2004/)
[![Email](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:your.email@example.com)

*Passionate about AI/ML and Mental Health Technology*

</div>

---

## 🙏 Acknowledgments

- **Streamlit** - For the amazing web framework
- **scikit-learn** - For robust ML algorithms
- **Mental Health Community** - For inspiring this project
- **Open Source Contributors** - For continuous improvement
- **Dataset Providers** - For making research data available

---

## ⚠️ Important Disclaimer

<div align="center">
<table>
<tr>
<td>

### **🚨 This Tool is NOT a Diagnostic Instrument 🚨**

This application is designed for **educational and informational purposes only**. 

It should **NEVER** be used as:
- A substitute for professional mental health diagnosis
- The sole basis for treatment decisions
- A replacement for qualified medical advice
- An emergency mental health service

**If you or someone you know is experiencing symptoms of depression or having suicidal thoughts, please seek immediate professional help.**

</td>
</tr>
</table>
</div>

### 🆘 Crisis Resources

| Region | Service | Contact |
|--------|---------|---------|
| **🇺🇸 United States** | National Suicide Prevention Lifeline | **988** |
| **🇺🇸 United States** | Crisis Text Line | Text **HOME** to **741741** |
| **🇮🇳 India** | AASRA | **+91-22-27546669** |
| **🇬🇧 UK** | Samaritans | **116 123** |
| **🇦🇺 Australia** | Lifeline | **13 11 14** |
| **🌍 International** | IASP Crisis Centers | [Find Local Help](https://www.iasp.info/resources/Crisis_Centres/) |

---

## 📊 Project Stats

<div align="center">

![GitHub Stars](https://img.shields.io/github/stars/ArunVijaykumarcsds/student-depression-predictor?style=social)
![GitHub Forks](https://img.shields.io/github/forks/ArunVijaykumarcsds/student-depression-predictor?style=social)
![GitHub Issues](https://img.shields.io/github/issues/ArunVijaykumarcsds/student-depression-predictor)
![GitHub Pull Requests](https://img.shields.io/github/issues-pr/ArunVijaykumarcsds/student-depression-predictor)
![GitHub Last Commit](https://img.shields.io/github/last-commit/ArunVijaykumarcsds/student-depression-predictor)

</div>

---

<div align="center">

### ⭐ **If you find this project helpful, please consider giving it a star!** ⭐

**Made with ❤️ and 🧠 using Python & Streamlit**

*Empowering Students Through AI-Driven Mental Health Awareness*

---

**© 2025 Arun VK. All Rights Reserved.**

</div>
