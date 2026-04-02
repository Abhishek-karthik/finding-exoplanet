# 🚀 Installation & Setup Guide

## Quick Start

### 1. Clone the Repository
```bash
git clone https://github.com/Abhishek-karthik/kepler-exoplanet-classification.git
cd kepler-exoplanet-classification
```

### 2. Create Virtual Environment (Optional but Recommended)

**For Windows:**
```bash
python -m venv venv
venv\Scripts\activate
```

**For macOS/Linux:**
```bash
python3 -m venv venv
source venv/bin/activate
```

### 3. Install Dependencies
```bash
pip install -r requirements.txt
```

## Running the Project

### Method 1: Jupyter Notebook (Recommended for Exploration)
```bash
jupyter notebook AI_PROJECT.ipynb
```
- Open your browser (usually http://localhost:8888)
- Run all cells: Click "Cell" → "Run All"
- Or run cells individually by pressing `Shift + Enter` for each cell

### Method 2: Convert to Python Script (For Production)
```bash
jupyter nbconvert --to script AI_PROJECT.ipynb
python AI_PROJECT.py
```

## System Requirements

- **Python Version:** 3.7 or higher
- **RAM:** 4GB minimum (8GB recommended)
- **Disk Space:** 500MB for datasets and libraries
- **Internet:** Required for initial dataset download

## Troubleshooting

### Issue: "Module not found" errors
**Solution:**
```bash
pip install --upgrade pip
pip install -r requirements.txt
```

### Issue: Jupyter not starting
**Solution:**
```bash
pip install --force-reinstall jupyter
jupyter notebook --ip=127.0.0.1
```

### Issue: Memory errors during FFT
**Solution:**
- Close other applications
- Ensure you have at least 4GB RAM free
- The notebooks uses SMOTE which increases memory usage

### Issue: Dataset not loading
**Solution:**
- Check internet connection
- The datasets load from WhiteHat Jr. servers
- If links are broken, contact project maintainers

## Project Workflow

1. **Data Loading** → Load Kepler datasets from URLs
2. **Normalization** → Apply mean normalization
3. **FFT Processing** → Extract frequency features
4. **SMOTE Balancing** → Oversample minority class
5. **Model Training** → Train Random Forest
6. **Evaluation** → Generate predictions & metrics

## Expected Outputs

After running the notebook, you'll see:
- ✅ Normalized data statistics
- 📊 Flux pattern visualizations
- 📈 FFT analysis plots
- 🎯 Model accuracy scores
- 📋 Classification reports
- 🔍 Confusion matrices

## Performance Notes

- **Data Loading:** ~2-5 minutes (depends on internet)
- **Normalization:** ~30 seconds
- **FFT Processing:** ~1-2 minutes
- **SMOTE Balancing:** ~2-3 minutes
- **Model Training:** ~1-3 minutes
- **Total Runtime:** ~8-15 minutes

## Next Steps

1. ✅ Run the notebook to train the model
2. 📊 Analyze the classification metrics
3. 🔬 Experiment with different parameters
4. 🚀 Deploy as a web service (optional)

## Getting Help

- **Documentation:** See README.md for full project overview
- **Code Comments:** Jupyter notebook has detailed inline explanations
- **Scikit-learn Docs:** https://scikit-learn.org/
- **Pandas Docs:** https://pandas.pydata.org/

---

**Happy Learning! 🎓**
