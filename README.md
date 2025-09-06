# 🦷 Predicting Dental Caries Using Systemic Health Markers

**Author:** Francisco Barbosa  
**GitHub:** [@Tuminha](https://github.com/Tuminha)  
**X (Twitter):** [@cisco_research](https://x.com/cisco_research)  
**Email:** cisco@periospot.com  

## Project Overview

This project explores the potential of **Support Vector Machine (SVM)** algorithms to predict dental caries likelihood in patients using comprehensive systemic health data. The goal is to identify novel correlations between systemic health factors and dental caries risk that could revolutionize preventive dental care through early identification of high-risk patients.

*Developed as part of Francisco Barbosa's research into machine learning applications in dental medicine and preventive healthcare.*

## 🎯 Dental Research Objectives

### Primary Goals
- **Predictive Modeling**: Develop an SVM-based classifier to assess dental caries risk
- **Feature Discovery**: Identify previously unrecognized systemic health indicators of dental caries
- **Clinical Translation**: Create actionable insights for preventive dental care strategies
- **Novel Biomarker Discovery**: Explore liver function, metabolic, and cardiovascular markers as caries predictors

### Research Questions
1. **Which systemic health factors are most predictive of dental caries?**
2. **Can we identify high-caries-risk patients before clinical symptoms appear?**
3. **What novel correlations exist between metabolic health and dental caries?**
4. **How can liver function markers predict oral health outcomes?**
5. **Can cardiovascular health indicators inform dental prevention strategies?**

## 📊 Dataset Analysis

### Dataset: Korean National Health and Nutrition Examination Survey
- **Size**: 16,708 patients
- **Features**: 21 systemic health indicators + 1 target variable
- **Target**: `dental caries` (binary: 0 = no caries, 1 = caries present)
- **Prevalence**: 21.1% caries rate (3,522 patients with caries)

### Feature Categories

#### 🏃‍♂️ **Anthropometric & Physical Health**
- `age` - Patient age
- `height(cm)` - Height in centimeters
- `weight(kg)` - Weight in kilograms
- `waist(cm)` - Waist circumference

#### 👁️ **Sensory Health**
- `eyesight(left)` - Left eye visual acuity
- `eyesight(right)` - Right eye visual acuity
- `hearing(left)` - Left ear hearing ability
- `hearing(right)` - Right ear hearing ability

#### ❤️ **Cardiovascular Health**
- `systolic` - Systolic blood pressure
- `relaxation` - Diastolic blood pressure

#### 🩸 **Metabolic & Biochemical Markers**
- `fasting blood sugar` - Glucose levels
- `Cholesterol` - Total cholesterol
- `triglyceride` - Triglyceride levels
- `HDL` - High-density lipoprotein
- `LDL` - Low-density lipoprotein
- `hemoglobin` - Hemoglobin levels

#### 🧪 **Kidney & Liver Function**
- `Urine protein` - Protein in urine
- `serum creatinine` - Kidney function marker
- `AST` - Aspartate aminotransferase (liver)
- `ALT` - Alanine aminotransferase (liver)
- `Gtp` - Gamma-glutamyl transferase (liver)

#### 🦷 **Target Variable**
- `dental caries` - Presence of dental caries (0/1)

## 🔬 Clinical Significance

### Novel Research Opportunities

#### **Metabolic Syndrome Connection**
- **Hypothesis**: Metabolic markers (glucose, cholesterol, triglycerides) may predict dental caries risk
- **Clinical Impact**: Early identification of patients at risk through routine blood work
- **Prevention Strategy**: Targeted interventions for patients with metabolic syndrome

#### **Cardiovascular-Dental Link**
- **Hypothesis**: Blood pressure and cardiovascular markers correlate with dental caries risk
- **Clinical Impact**: Integration of dental risk assessment into cardiovascular care protocols
- **Research Value**: Understanding bidirectional relationships between heart and oral health

#### **Liver Function & Oral Health** ⭐ **NOVEL DISCOVERY**
- **Hypothesis**: Liver enzymes (AST, ALT, GTP) may indicate systemic inflammation affecting dental health
- **Clinical Impact**: Novel biomarker discovery for dental caries risk prediction
- **Prevention Strategy**: Monitoring liver function as part of comprehensive oral health assessment
- **Research Innovation**: First study to explore liver-oral health correlations

#### **Sensory Health Correlation**
- **Hypothesis**: Vision and hearing impairments may correlate with dental caries through shared risk factors
- **Clinical Impact**: Identifying patients with sensory impairments as high-risk groups
- **Research Value**: Understanding aging-related health deterioration patterns

## 🤖 Machine Learning Approach

### SVM Advantages for Medical Prediction
1. **High-Dimensional Data**: Excellent performance with multiple health indicators
2. **Non-linear Relationships**: Can capture complex interactions between health factors
3. **Robust to Outliers**: Medical data often contains extreme values
4. **Interpretable Results**: Feature importance analysis reveals clinical insights
5. **Small Sample Efficiency**: Works well with medical datasets

### Model Development Strategy
- **Feature Engineering**: Create composite health scores and ratios
- **Hyperparameter Tuning**: Optimize SVM parameters for medical prediction
- **Cross-Validation**: Ensure model generalizability across patient populations
- **Feature Selection**: Identify most predictive health indicators
- **Performance Metrics**: Focus on sensitivity (catching high-risk patients)

## 📈 Expected Clinical Outcomes

### Immediate Applications
1. **Risk Stratification**: Classify patients into low/medium/high dental caries risk
2. **Preventive Protocols**: Develop targeted intervention strategies for high-risk patients
3. **Resource Allocation**: Optimize dental care resources for caries prevention
4. **Novel Biomarker Integration**: Incorporate liver function markers into dental risk assessment

### Long-term Research Impact
1. **Biomarker Discovery**: Identify novel systemic indicators of dental caries
2. **Interdisciplinary Care**: Bridge gaps between medical and dental specialties
3. **Public Health**: Develop population-level screening protocols for caries prevention
4. **Clinical Guidelines**: Establish evidence-based preventive care strategies

## 🛠️ Technical Implementation

### Environment Setup
- **Python 3.11**: Clean conda environment (`periodontal`)
- **Key Libraries**: scikit-learn, pandas, numpy, matplotlib, seaborn
- **Data Source**: Kaggle Korean National Health Survey dataset

### Project Structure
```
periodontal_disease/
├── README.md                           # This file
├── predicting_dental_caries.ipynb     # Main analysis notebook
├── data/
│   └── test_dataset.csv               # Dataset
├── .env                               # Kaggle API credentials
└── kaggle.json                        # Kaggle authentication
```

### Implementation Progress

#### ✅ **Phase 1: Data Exploration** - COMPLETED
- **Dataset Analysis**: 16,708 patients, 21 features, 21.1% caries prevalence
- **Data Quality**: No missing values, clean dataset
- **Basic Statistics**: Comprehensive understanding of feature distributions

#### ✅ **Phase 2: Feature Analysis** - COMPLETED  
- **Correlation Analysis**: Identified top features correlated with dental caries
- **Novel Biomarkers**: Explored liver function markers (AST, ALT, GTP)
- **Feature Engineering**: BMI, ratios, and composite health scores

#### ✅ **Phase 3: SVM Implementation** - COMPLETED
- **Model Development**: Linear SVM (78.1%) vs RBF SVM (80.5%)
- **Hyperparameter Tuning**: Grid search across C and gamma values
- **Best Performance**: RBF SVM with C=100, gamma=100 (80.5% accuracy)
- **Key Finding**: RBF kernel significantly outperforms linear kernel

#### 🔄 **Phase 4: Model Validation** - IN PROGRESS
- **Cross-Validation**: Testing model robustness and overfitting detection
- **Feature Selection**: Identifying most important features for optimal performance
- **Model Optimization**: Building refined models with selected features

#### 📋 **Phase 5: Clinical Translation** - PLANNED
- **Risk Stratification**: High/medium/low risk patient classification
- **Clinical Guidelines**: Evidence-based prevention strategies
- **Novel Biomarker Validation**: Confirming liver-oral health correlations

## 🎓 Learning Objectives

### SVM Mastery
- Understanding SVM theory and medical applications
- Hyperparameter optimization techniques
- Feature selection and engineering strategies
- Model interpretation and clinical translation

### Dental Research Skills
- Statistical analysis of health data
- Clinical correlation identification
- Evidence-based preventive care development
- Interdisciplinary research methodology

## 🚀 Next Steps

1. ✅ **Data Exploration**: Comprehensive EDA of health indicators - COMPLETED
2. ✅ **Feature Engineering**: Create meaningful health composites - COMPLETED
3. ✅ **SVM Implementation**: Build and optimize classification model - COMPLETED
4. 🔄 **Model Validation**: Cross-validation and overfitting detection - IN PROGRESS
5. 📋 **Feature Selection**: Identify most important features for optimal performance - PLANNED
6. 📋 **Clinical Interpretation**: Translate results into actionable insights - PLANNED
7. 📋 **Final Validation**: Cross-validate findings with clinical literature - PLANNED

---

## 📞 Contact & Collaboration

**Francisco Barbosa**  
*Dental Research & Machine Learning Specialist*

- **Email:** cisco@periospot.com
- **GitHub:** [@Tuminha](https://github.com/Tuminha)
- **X (Twitter):** [@cisco_research](https://x.com/cisco_research)
- **Research Focus:** ML applications in dental medicine, preventive healthcare, and periodontal disease prediction

### 🤝 Collaboration Opportunities

Interested in collaborating on dental AI research or have questions about this project? Feel free to reach out! I'm particularly interested in:

- **Clinical Validation Studies**: Partnering with dental practices for model validation
- **Research Publications**: Collaborative papers on ML in dental medicine
- **Open Source Contributions**: Expanding the dental ML toolkit
- **Industry Applications**: Translating research into clinical practice

---

*This project represents an innovative approach to dental caries prediction using systemic health markers, combining machine learning expertise with clinical dental knowledge to advance preventive oral healthcare. Developed by Francisco Barbosa as part of ongoing research into AI applications in dental medicine and novel biomarker discovery.*
