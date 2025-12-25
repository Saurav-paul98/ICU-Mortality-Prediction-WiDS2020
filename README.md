# 🏥 ICU Patient Mortality Prediction - WiDS Datathon 2020

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/)
[![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-green.svg)](https://pandas.pydata.org/)
[![Status](https://img.shields.io/badge/Status-In%20Progress-yellow.svg)]()

## 📋 Project Overview

An end-to-end data analysis project predicting ICU patient mortality using the WiDS (Women in Data Science) Datathon 2020 dataset. This project analyzes **130,000+ ICU admissions** from **200+ hospitals** across 6 countries to identify critical factors affecting patient survival and provide actionable clinical insights.

**Data Source:**  [WiDS Datathon 2020](https://www.kaggle.com/competitions/widsdatathon2020) and MIT's GOSSIS Initiative (Global Open Source Severity of Illness Score)  
**Domain:** Healthcare Analytics - Critical Care Medicine  
**Timeline:** Dec 15, 2025 -Jan 10, 2026

---

## 🎯 Business Problem

ICU mortality prediction is critical for:
- **Resource Allocation:** Identifying high-risk patients requiring intensive monitoring
- **Early Intervention:** Triggering preventive care protocols for at-risk patients
- **Clinical Decision Support:** Assisting physicians with data-driven risk assessments
- **Cost Optimization:** Reducing unnecessary ICU stays while ensuring quality care

**Impact:** Early identification of high-risk patients can reduce ICU mortality by 15-20% through timely interventions.

---

## 📊 Dataset Description

### **Scale & Scope:**
- **Records:** 130,159 ICU hospital admissions
- **Features:** 186 clinical features across 6 categories
- **Geography:** 200+ hospitals in USA, Argentina, Brazil, Australia, New Zealand, Sri Lanka
- **Time Period:** First 24 hours of ICU admission
- **Target:** `hospital_death` (Binary: 0 = Survived, 1 = Died)

### **Feature Categories:**

#### **1. Patient Demographics (10 features)**
- Age, gender, ethnicity, BMI, height, weight

#### **2. APACHE Scores (15 features)**
- `apache_4a_hospital_death_prob` - Pre-calculated hospital death probability
- `apache_4a_icu_death_prob` - ICU-specific death probability
- APACHE component scores: cardiovascular, respiratory, renal, neurological

#### **3. Vital Signs - First 24 Hours (50+ features)**
- Heart rate, blood pressure (systolic, diastolic, mean arterial)
- Respiratory rate, temperature, oxygen saturation
- Min, max, mean values captured over 24-hour window

#### **4. Lab Results - First 24 Hours (40+ features)**
- Blood chemistry: sodium, potassium, glucose, creatinine, bilirubin
- Blood gas: pH, PaO2, PaCO2
- Hematology: WBC, hemoglobin, platelets

#### **5. Comorbidities (20+ features)**
- Chronic conditions: AIDS, cirrhosis, diabetes, hepatic failure
- Cancer indicators: leukemia, lymphoma, solid tumor
- Immunosuppression status

#### **6. ICU Admission Details (15+ features)**
- ICU type: Medical, Surgical, Cardiac, Neurological
- Admission source: Emergency Department, Operating Room, Floor
- Pre-ICU length of stay
- Ventilation status

---

## 🔍 Analysis Approach

### **Phase 1: Data Understanding & Cleaning** *(In Progress)*
- Comprehensive exploratory data analysis
- Missing value assessment and imputation strategy
- Outlier detection and handling
- Data quality validation

### **Phase 2: Feature Engineering** *(Planned)*
- Vital sign instability scores (range, variance)
- Lab abnormality flags (outside normal ranges)
- Comorbidity severity index
- APACHE score validation and enhancement
- Age-risk interaction features

### **Phase 3: Statistical Analysis** *(Planned)*
- Mortality rate analysis by demographics
- Correlation analysis: clinical features vs outcomes
- Hypothesis testing: survivors vs non-survivors
- Feature importance ranking
- Survival analysis (time-to-event)

### **Phase 4: Visualization & Insights** *(Planned)*
- 12-15 publication-quality visualizations
- Feature correlation heatmaps
- Mortality distribution by risk factors
- Clinical pathway analysis
- Interactive dashboards (if time permits)

### **Phase 5: Predictive Modeling** *(Stretch Goal)*
- Baseline logistic regression model
- Handle class imbalance (SMOTE/class weights)
- Model evaluation: ROC-AUC, precision, recall, F1-score
- Feature importance interpretation

---

## 🛠️ Technical Stack

**Programming:** Python 3.8+  
**Data Analysis:** Pandas, NumPy  
**Visualization:** Matplotlib, Seaborn  
**Statistical Analysis:** SciPy, scikit-learn  
**Notebook:** Jupyter Notebook  
**Version Control:** Git, GitHub

---

## 📂 Project Structure
```
ICU-Mortality-Prediction-WiDS2020/
│
├── data/
│   ├── raw/                          # Original WiDS dataset
│   │   ├── training_v2.csv
│   │   └── data_dictionary.csv
│   └── processed/                    # Cleaned datasets
│
├── notebooks/
│   ├── 01_exploration.ipynb          # Initial EDA
│   ├── 02_data_cleaning.ipynb        # Preprocessing
│   ├── 03_feature_engineering.ipynb  # Feature creation
│   ├── 04_statistical_analysis.ipynb # Deep analysis
│   ├── 05_visualizations.ipynb       # Final charts
│   └── 06_modeling.ipynb             # Predictive models (optional)
│
├── src/
│   ├── data_processing.py            # Cleaning functions
│   ├── feature_engineering.py        # Feature creation
│   └── visualization.py              # Plotting utilities
│
├── outputs/
│   ├── figures/                      # All charts (PNG/SVG)
│   └── reports/                      # Analysis summaries
│
├── requirements.txt                   # Python dependencies
├── .gitignore                         # Git ignore rules
├── LICENSE                            # MIT License
└── README.md                          # This file
```

---

## 🚀 Getting Started

### **Prerequisites**
```bash
Python 3.8+
pip or conda package manager
```

### **Installation**
```bash
# Clone repository
git clone https://github.com/yourusername/ICU-Mortality-Prediction-WiDS2020.git
cd ICU-Mortality-Prediction-WiDS2020

# Install dependencies
pip install -r requirements.txt

# Launch Jupyter Notebook
jupyter notebook
```

### **Data Setup**
1. Download dataset from [WiDS Datathon 2020](https://www.kaggle.com/competitions/widsdatathon2020)
2. Place `training_v2.csv` in `data/raw/`
3. Place `WiDS Datathon 2020 Dictionary.csv` in `data/raw/` as `data_dictionary.csv`

---

## 📈 Current Progress

- [x] Project setup and repository initialization
- [x] Dataset download and initial exploration
- [ ] Data cleaning and preprocessing
- [ ] Feature engineering
- [ ] Statistical analysis
- [ ] Visualization creation
- [ ] Model development
- [ ] Documentation and insights

**Last Updated:** December 23, 2025

---

## 🎓 Key Skills Demonstrated

- **Data Wrangling:** Handling 130k+ records with 186 features
- **Missing Data Strategies:** Multiple imputation techniques for clinical data
- **Feature Engineering:** Domain-driven feature creation (vital instability, lab abnormalities)
- **Statistical Analysis:** Hypothesis testing, correlation analysis, survival analysis
- **Data Visualization:** Publication-quality charts for clinical insights
- **Healthcare Domain:** Understanding ICU metrics, APACHE scores, clinical pathways
- **Class Imbalance:** Techniques for imbalanced classification (9:1 ratio)

---

## 💡 Business Value

### **Expected Deliverables:**
1. **Risk Stratification Framework:** Categorize patients into low/medium/high mortality risk
2. **Key Mortality Predictors:** Top 10 clinical factors affecting survival
3. **Early Warning System:** Identify high-risk patients within first 24 hours
4. **Resource Optimization:** Guidelines for ICU bed allocation
5. **Clinical Recommendations:** Data-driven protocols for improving outcomes

### **Projected Impact:**

---

## 📚 References

- [WiDS Datathon 2020 Competition](https://www.kaggle.com/competitions/widsdatathon2020)
- [MIT GOSSIS Initiative](https://gossis.mit.edu/)
- APACHE Scoring: Knaus WA, et al. APACHE II: A severity of disease classification system. Crit Care Med. 1985.
- [WiDS 2020 Overview Paper](https://arxiv.org/abs/2001.03765)

---

## 👤 Author

**[Saurav Paul]**  
 Data Analyst | Python | SQL | Healthcare Analytics

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue)](https://linkedin.com/in/yourprofile)
[![GitHub](https://img.shields.io/badge/GitHub-Follow-black)](https://github.com/yourusername)
[![Email](https://img.shields.io/badge/Email-Contact-red)](mailto:your.email@example.com)

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 🙏 Acknowledgments

- **WiDS (Women in Data Science)** for organising the datathon
- **MIT GOSSIS Initiative** for providing anonymized clinical data
- **Stanford University** for hosting the competition
- Healthcare professionals who contributed domain expertise

---

**⭐ If you find this project useful, please consider starring the repository!**

*This is an educational project for portfolio development. Not intended for clinical use.*
```

---

