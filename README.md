# ETL-Project

## Overview

A comprehensive Extract, Transform, Load (ETL) project that demonstrates data analysis and processing workflows using Python Jupyter notebooks. This project includes exploratory data analysis (EDA) on medical insurance data and statistical analysis of loan approval datasets.

## Project Structure

```
ETL-Project/
├── ETL_Project.ipynb          # Medical Insurance Data EDA and Analysis
├── stats.ipynb                # Loan Statistics and Distribution Analysis
├── loan.ipynb                 # Loan Data Processing and Approval Analysis
├── loan_approved.csv          # Processed Loan Approval Dataset
├── my_insurance_data.csv      # Medical Insurance Dataset
├── data/                      # Data directory
├── scripts/                   # Utility scripts
└── README.md                  # Project Documentation
```

## Datasets

### 1. Medical Insurance Dataset (`my_insurance_data.csv`)
**Purpose**: Exploratory Data Analysis (EDA) and insights extraction

**Key Analyses**:
- Age distribution and demographic patterns
- Charges correlation with age, BMI, and smoking status
- Regional analysis of insurance costs
- Statistical summaries and distribution patterns
- Premium prediction factors

**File Size**: Comprehensive medical records dataset

### 2. Loan Approval Dataset (`loan_approved.csv`)
**Purpose**: Loan approval predictions and statistical modeling

**Key Features**:
- Loan amount and duration analysis
- Approval status distribution
- Credit history patterns
- Income and employment status correlations
- Statistical indicators for approval probability

## Notebooks

### ETL_Project.ipynb - Medical Insurance EDA
**Objectives**:
- Load and explore medical insurance dataset
- Perform univariate analysis (age, BMI, charges distributions)
- Conduct bivariate analysis (age vs charges, smoking impact, regional differences)
- Statistical summaries and insights
- Data quality assessment
- Visualization of key patterns and trends

**Key Analyses**:
```
- Demographic Analysis: Age groups, gender distribution, regional patterns
- Medical Metrics: BMI classification, smoking status impact
- Cost Analysis: Premium calculations, cost drivers, regional pricing
- Correlation Analysis: Feature relationships and dependencies
- Statistical Testing: Distribution normality, outlier detection
```

### stats.ipynb - Loan Statistics Analysis
**Objectives**:
- Statistical analysis of loan datasets
- Descriptive statistics and summary measures
- Distribution analysis and visualizations
- Loan amount patterns and trends
- Approval rate statistics

**Key Metrics**:
- Mean, median, standard deviation of loan amounts
- Approval distribution and rates
- Duration and tenure statistics
- Employment and income statistics

### loan.ipynb - Loan Data Processing & Approval Analysis
**Objectives**:
- ETL operations on raw loan data
- Data cleaning and preprocessing
- Feature engineering for modeling
- Approval status analysis
- Credit history impact assessment

**Key Operations**:
- Data validation and quality checks
- Missing value handling
- Categorical encoding
- Feature scaling and normalization
- Approval predictability analysis

## Technologies Used

### Languages & Libraries
- **Python 3.x**
- **Pandas**: Data manipulation and analysis
- **NumPy**: Numerical computations
- **Matplotlib**: Static visualizations
- **Seaborn**: Statistical data visualization
- **Jupyter Notebook**: Interactive development environment

### Data Processing Pipeline
1. **Extraction**: Load data from CSV files
2. **Transformation**: Clean, preprocess, and engineer features
3. **Analysis**: Statistical analysis and EDA
4. **Visualization**: Generate insights through plots and charts

## Key Findings

### Medical Insurance Analysis
- Insurance premiums significantly correlate with age and smoking status
- Regional variations in premium pricing observed
- BMI categories show different cost patterns
- Smoking increases average costs substantially

### Loan Analysis
- Loan approval depends on multiple factors (credit history, income, employment)
- Distribution of approved vs. rejected loans shows clear patterns
- Duration of loans affects approval probability
- Employment status is a key predictor

## Installation & Setup

### Prerequisites
```bash
python >= 3.7
jupyter >= 6.0
pandas >= 1.0
numpy >= 1.18
matplotlib >= 3.0
seaborn >= 0.11
```

### Installation Steps

1. Clone the repository:
```bash
git clone https://github.com/Abhinav7301/ETL-Project.git
cd ETL-Project
```

2. Create a virtual environment (recommended):
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. Install dependencies:
```bash
pip install -r requirements.txt
```

4. Launch Jupyter Notebook:
```bash
jupyter notebook
```

5. Open and run the notebooks in the following order:
   - `ETL_Project.ipynb` (Medical Insurance EDA)
   - `stats.ipynb` (Loan Statistics)
   - `loan.ipynb` (Loan Processing & Analysis)

## Usage

### Running Individual Notebooks

Each notebook is self-contained and includes:
- Data loading and exploration
- Statistical analysis and visualizations
- Interpretations and key insights
- Comments explaining each step

### Data Exploration

**For Medical Insurance Data**:
```python
# Load dataset
import pandas as pd
df = pd.read_csv('my_insurance_data.csv')

# Basic exploration
df.head()
df.describe()
df.info()
```

**For Loan Data**:
```python
# Load approved loans dataset
loan_df = pd.read_csv('loan_approved.csv')

# Check approval distribution
loan_df['Loan_Status'].value_counts()
```

## Analysis Outputs

### Visualizations Generated
- Histograms and distribution plots
- Box plots for outlier detection
- Scatter plots for correlation analysis
- Heatmaps for feature relationships
- Bar charts for categorical analysis
- Time series patterns (where applicable)

### Statistical Reports
- Descriptive statistics
- Correlation matrices
- Distribution analyses
- Hypothesis testing results
- Outlier identification

## Data Quality & Preprocessing

### Handled Issues
- Missing values: Identified and appropriately handled
- Outliers: Detected and managed
- Categorical variables: Encoded for analysis
- Duplicate records: Identified and removed
- Data validation: Checked for consistency

### Data Types
- Numerical: Age, BMI, Charges, Loan Amount
- Categorical: Gender, Region, Smoking Status, Employment Type
- Boolean: Approval Status, Loan Status

## Results & Insights

### Medical Insurance Insights
1. **Premium Drivers**: Age and smoking status are primary cost drivers
2. **Regional Patterns**: Significant variation in premium pricing by region
3. **BMI Impact**: Higher BMI correlates with increased premiums
4. **Demographics**: Insurance costs increase significantly with age

### Loan Analysis Insights
1. **Approval Factors**: Multiple factors influence loan approval
2. **Credit History**: Crucial for loan approval probability
3. **Income Factor**: Higher income positively impacts approval
4. **Employment Stability**: Longer employment duration increases approval chances

## Reproducibility

All analyses are fully reproducible:
- Fixed random seeds where applicable
- All data sources included
- Complete code documentation
- Step-by-step explanations
- Output saved for verification

## Future Enhancements

- Predictive modeling (Linear/Logistic Regression, Random Forest)
- Time series analysis if temporal data available
- Advanced feature engineering
- Machine learning model deployment
- Interactive dashboards (Plotly/Dash)
- API development for predictions

## Project Workflow

```
Raw Data → Extraction → Cleaning → Transformation → 
Feature Engineering → Analysis → Visualization → Insights
```

## File Descriptions

| File | Type | Purpose |
|------|------|----------|
| ETL_Project.ipynb | Jupyter Notebook | Medical Insurance EDA |
| stats.ipynb | Jupyter Notebook | Loan Statistics Analysis |
| loan.ipynb | Jupyter Notebook | Loan Data ETL & Processing |
| my_insurance_data.csv | Dataset | Medical Insurance Records |
| loan_approved.csv | Dataset | Loan Approval Data |
| .env | Configuration | Environment variables |
| scripts/ | Directory | Utility and helper scripts |
| data/ | Directory | Data storage |

## Performance & Scalability

- Current implementation handles datasets with thousands of records efficiently
- Memory-optimized data processing using pandas
- Vectorized operations for fast computations
- Suitable for datasets up to several GB

## Debugging & Troubleshooting

### Common Issues

**Issue**: Jupyter kernel won't start
**Solution**: Reinstall jupyter and ipython
```bash
pip install --upgrade jupyter ipython
```

**Issue**: Missing dependencies
**Solution**: Install all requirements
```bash
pip install pandas numpy matplotlib seaborn jupyter
```

**Issue**: Data file not found
**Solution**: Ensure CSV files are in the project root directory

## Best Practices Implemented

- Clean, readable code with proper comments
- Modular notebook structure
- Error handling and validation
- Consistent naming conventions
- Comprehensive documentation
- Reproducible analysis workflow
- Version control with git

## Learning Outcomes

This project demonstrates proficiency in:
- Data extraction and loading
- Data cleaning and preprocessing
- Exploratory Data Analysis (EDA)
- Statistical analysis
- Data visualization
- Python programming with pandas/numpy
- Jupyter notebook usage
- ETL pipeline development
- Data-driven decision making

## Contributing

Feel free to fork this repository and submit pull requests for improvements.

## License

This project is open source and available under the MIT License.

## Author

**Abhinav7301** - Data Analysis & ETL Project

## Contact & Support

For questions or issues, please:
- Open an issue on GitHub
- Contact the project maintainer

## Acknowledgments

- Dataset sources and providers
- Python community and libraries used
- Data science best practices and standards

## Project Timeline

- Data collection and preparation
- EDA and exploration phase
- Statistical analysis
- Visualization and insights generation
- Documentation and finalization

## Additional Resources

- [Pandas Documentation](https://pandas.pydata.org/)
- [NumPy Documentation](https://numpy.org/)
- [Matplotlib Documentation](https://matplotlib.org/)
- [Jupyter Documentation](https://jupyter.org/)
- [Seaborn Documentation](https://seaborn.pydata.org/)

## Version History

### v1.0 (Current)
- Initial project setup
- Medical Insurance EDA
- Loan Statistics Analysis
- Loan Data Processing
- Comprehensive documentation

---

**Last Updated**: 2024
**Project Status**: Complete & Active
