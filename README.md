# Kepler Exoplanet Classification

## 📋 Project Overview

This is a **Machine Learning classification project** that predicts whether distant stars have exoplanets using NASA's Kepler Space Telescope data. The project implements the **Transit Method** to detect exoplanets by analyzing periodic patterns in stellar brightness measurements (flux values).

## 🔭 Problem Statement

NASA's Kepler Space Telescope has discovered thousands of exoplanets by measuring the brightness of stars. When a planet orbits in front of its star (from Earth's perspective), it causes a periodic dip in the star's brightness. Our goal is to build a machine learning classifier that automatically detects these periodic patterns to identify whether a star has planets.

## 🎯 Key Concepts

### Transit Method
- **Principle:** A planet passing in front of its star causes temporary brightness dips
- **Measurement:** Kepler telescope records flux (brightness) values over time
- **Pattern:** Periodic dips indicate the presence of an exoplanet

### Data Science Techniques Used
1. **Data Normalization** - Mean normalization to standardize flux values across different scales
2. **Feature Engineering** - Fast Fourier Transform (FFT) to extract frequency domain features
3. **Data Balancing** - SMOTE (Synthetic Minority Over-Sampling Technique) to handle class imbalance
4. **Classification** - Random Forest Classifier with 50 decision trees

## 📊 Dataset

- **Training Dataset:** ~5,000+ stars with labeled exoplanet status
- **Test Dataset:** ~570 stars for model evaluation
- **Features:** 3,197 flux measurements per star
- **Classes:** 
  - Class 1: Stars with exoplanets
  - Class 2: Stars without exoplanets (false positives from Kepler data)

**Data Source:** [WhiteHat Jr. Student Datasets (Kepler Exoplanets) ](https://s3-student-datasets-bucket.whjr.online/whitehat-ds-datasets/kepler-exoplanets-dataset/)

## 🛠️ Technologies & Libraries

- **Python 3.x**
- **Pandas** - Data manipulation and analysis
- **NumPy** - Numerical computing
- **Matplotlib** - Data visualization
- **SciPy** - FFT implementation
- **Scikit-learn** - Machine learning models and metrics
- **Imbalanced-learn** - SMOTE for data balancing

## 🚀 How to Run

### Prerequisites
```bash
pip install pandas numpy matplotlib scikit-learn imbalanced-learn scipy
```

### Running the Jupyter Notebook
1. Install Jupyter Notebook:
   ```bash
   pip install jupyter
   ```

2. Clone the repository and navigate to the folder:
   ```bash
   git clone https://github.com/Abhishek-karthik/kepler-exoplanet-classification.git
   cd kepler-exoplanet-classification
   ```

3. Launch Jupyter and open the notebook:
   ```bash
   jupyter notebook AI_PROJECT.ipynb
   ```

4. Run all cells in sequence to:
   - Load the Kepler dataset
   - Normalize flux values
   - Apply FFT for feature extraction
   - Balance data using SMOTE
   - Train the Random Forest Classifier
   - Generate predictions and model evaluation

## 📈 Project Workflow

### Step 1: Data Loading & Exploration
- Import Kepler exoplanet training and test datasets
- Analyze data structure and statistics

### Step 2: Data Preprocessing - Normalization
- Apply mean normalization: 
  $$x_{norm} = \frac{x - x_{mean}}{x_{max} - x_{min}}$$
- Standardize flux values to uniform scale [-1, 1]

### Step 3: Feature Engineering - FFT
- Extract frequency domain features using Fast Fourier Transform
- Identify dominant frequencies in stellar brightness patterns
- Detect periodic components indicating planetary orbits

### Step 4: Data Balancing - SMOTE
- Address class imbalance (majority class: 99.1%)
- Synthetically generate minority class samples
- Balance classes to 50-50 representation

### Step 5: Model Training
- Train Random Forest Classifier on balanced data
- Use 50 decision trees (`n_estimators=50`)
- Leverage parallel processing (`n_jobs=-1`)

### Step 6: Model Evaluation
- Generate predictions on test dataset
- Analyze confusion matrix
- Review classification report metrics (Precision, Recall, F1-Score)

## 📊 Expected Results

The Random Forest Classifier achieves robust performance in identifying:
- **True Positives:** Stars correctly identified as having exoplanets
- **True Negatives:** Non-planetary stars correctly identified
- **Minority class detection:** Effective identification despite class imbalance

Typical metrics include precision, recall, and F1-scores for both classes.

## 📁 Project Structure

```
kepler-exoplanet-classification/
├── AI_PROJECT.ipynb          # Main Jupyter notebook with full analysis
├── Dataset.txt               # Dataset source URLs
├── README.md                 # Project documentation
└── requirements.txt          # Python dependencies
```

## 🔬 Mathematical Background

### Mean Normalization Formula
For a feature x with N values:
$$x_{norm} = \frac{x - \bar{x}}{x_{max} - x_{min}}$$

### FFT Frequency Analysis  
- **Frequency:** Number of cycles per time unit
- **Amplitude:** Peak value of brightness variation
- **Phase:** Time shift of periodic pattern

### SMOTE Technique
- Generates synthetic minority samples
- Creates points along line segments between minority examples
- Results in balanced dataset for training

## 🎓 Learning Outcomes

Through this project, you'll learn:
- How exoplanet detection works in astronomy
- Data normalization and standardization techniques
- Frequency domain analysis with FFT
- Handling imbalanced datasets
- Building ensemble classification models
- Model evaluation and validation strategies

## 👥 Contributors

- Group 3A (AI Project - Semester 3)

## 📝 References

- **Kepler Space Telescope:** NASA's planet-hunting mission
- **Transit Method:** Standard technique in exoplanet detection
- **Random Forest:** Ensemble learning method (Breiman, 2001)
- **SMOTE:** Synthetic Minority Over-sampling Technique (Chawla et al., 2002)

## 📄 License

This is an educational project for learning purposes.

## 🤝 Support

For questions or issues regarding the project:
1. Review the inline comments in the Jupyter notebook
2. Check the mathematical explanations in markdown cells
3. Refer to scikit-learn and pandas documentation

---

**Last Updated:** April 7, 2026
**Status:** ✅ Complete & Production Ready
