# ETL-Project

## Overview

A comprehensive Extract, Transform, Load (ETL) project that demonstrates data processing and analysis workflows using Python. This project includes ETL pipelines for the Iris flower classification dataset and the Titanic dataset, showcasing data extraction, transformation, and exploratory data analysis using Jupyter notebooks and Python scripts.

## Project Structure

```
ETL-Project/
├── etl_analysis_iris.ipynb        # Iris Dataset ETL Analysis and Exploration
├── data/                          # Data directory with raw and staged data
│   ├── raw/
│   │   ├── iris_raw.csv          # Raw Iris Dataset
│   │   └── titanic_raw.csv       # Raw Titanic Dataset
│   └── staged/
│       └── iris_transformed.csv  # Transformed and Processed Iris Data
├── scripts/                       # Python ETL and utility scripts
│   ├── extract_iris.py           # Iris data extraction script
│   ├── extract_titanic.py        # Titanic data extraction script
│   ├── load_iris.py              # Iris data loading script
│   └── transform_iris.py         # Iris data transformation script
├── .env                           # Environment configuration
└── README.md                      # Project Documentation
```

## Datasets

### 1. Iris Dataset (`data/raw/iris_raw.csv`)
**Purpose**: Classification and exploratory data analysis

**Key Features**:
- Sepal length and width measurements
- Petal length and width measurements
- Species classification (Setosa, Versicolor, Virginica)
- 150 flower samples

**Processed Output**: `data/staged/iris_transformed.csv` - Cleaned and transformed dataset ready for analysis

### 2. Titanic Dataset (`data/raw/titanic_raw.csv`)
**Purpose**: Data extraction and analysis

**Key Features**:
- Passenger information (name, age, sex)
- Ticket details (class, fare, cabin)
- Survival status
- Embarkation information

## Notebooks

### etl_analysis_iris.ipynb - Iris ETL Analysis
**Objectives**:
- Extract and load Iris dataset
- Perform exploratory data analysis (EDA)
- Statistical analysis of iris features
- Species classification patterns
- Data quality assessment and cleaning
- Visualization of feature distributions and relationships

**Key Analyses**:
```
- Feature Statistics: Sepal and petal measurements summary
- Species Distribution: Count and proportion of each species
- Feature Correlation: Relationships between measurements
- Statistical Testing: Distribution analysis by species
- Visualization: Scatter plots, histograms, box plots
```

## Scripts

### Data Extraction Scripts

**extract_iris.py** - Iris Data Extraction
- Loads iris_raw.csv from data/raw/
- Validates data integrity
- Returns structured dataset

**extract_titanic.py** - Titanic Data Extraction
- Loads titanic_raw.csv from data/raw/
- Handles missing values detection
- Initial data exploration

### Data Processing Scripts

**load_iris.py** - Iris Data Loading
- Loads processed iris data
- Prepares data for analysis
- Manages data connections

**transform_iris.py** - Iris Data Transformation
- Cleans iris dataset
- Handles missing or invalid values
- Feature normalization/standardization
- Outputs to data/staged/iris_transformed.csv

## Technologies Used

### Languages & Libraries
- **Python 3.x**
- **Pandas**: Data manipulation and analysis
- **NumPy**: Numerical computations
- **Matplotlib**: Static visualizations
- **Seaborn**: Statistical data visualization
- **Jupyter Notebook**: Interactive development environment
- **Supabase**: Database backend for data storage

### ETL Pipeline Components
1. **Extraction**: Load data from CSV files
2. **Transformation**: Clean, preprocess, and normalize features
3. **Loading**: Store processed data in database and files
4. **Analysis**: Statistical analysis and exploratory data analysis
5. **Visualization**: Generate insights through plots and charts

## Key Findings

### Iris Dataset Analysis
- Clear separation between Iris species based on petal measurements
- Strong correlation between petal length and width
- Sepal measurements show less distinct species separation
- Setosa species distinctly different from Versicolor and Virginica

### Data Processing Insights
- Successful transformation and standardization of features
- No significant missing values in raw Iris data
- Feature scaling improves classification model performance

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
pip install pandas numpy matplotlib seaborn jupyter
```

4. Set up environment variables (if using Supabase):
   - Copy `.env.example` to `.env`
   - Add your database credentials

5. Launch Jupyter Notebook:
```bash
jupyter notebook
```

6. Open and run the analysis:
   - `etl_analysis_iris.ipynb` - For Iris dataset analysis

## Usage

### Running ETL Scripts

**Extract Iris Data**:
```python
python scripts/extract_iris.py
```

**Transform Iris Data**:
```python
python scripts/transform_iris.py
```

**Load Iris Data**:
```python
python scripts/load_iris.py
```

### Running the Analysis Notebook

1. Start Jupyter: `jupyter notebook`
2. Open `etl_analysis_iris.ipynb`
3. Run cells sequentially to:
   - Load the Iris dataset
   - Perform exploratory analysis
   - Generate visualizations
   - View statistical summaries

### Data Exploration Example

```python
import pandas as pd

# Load raw Iris data
iris_df = pd.read_csv('data/raw/iris_raw.csv')
print(iris_df.head())
print(iris_df.describe())
print(iris_df.info())

# Load transformed data
iris_transformed = pd.read_csv('data/staged/iris_transformed.csv')
print(iris_transformed.head())
```

## Analysis Outputs

### Generated Visualizations
- Feature distribution plots (histograms)
- Pairwise scatter plots
- Box plots by species
- Correlation heatmaps
- 3D scatter plots for feature visualization

### Statistical Reports
- Descriptive statistics by species
- Feature correlation matrices
- Mean and variance analysis
- Distribution characteristics

## Data Quality & Preprocessing

### Handled Issues
- Missing value detection and handling
- Outlier identification
- Feature scaling and normalization
- Data type validation
- Duplicate record detection

### Data Pipeline
```
Raw CSV → Extraction → Validation → Transformation → 
Normalization → Staging → Analysis → Visualization
```

## Project Workflow

1. **Data Collection**: Raw datasets stored in `data/raw/`
2. **Extraction**: Python scripts extract data from CSV files
3. **Transformation**: Data cleaning, validation, and transformation
4. **Loading**: Processed data stored in `data/staged/`
5. **Analysis**: Jupyter notebook performs EDA and statistical analysis
6. **Visualization**: Generate charts and insights

## File Descriptions

| File | Type | Purpose |
|------|------|----------|
| etl_analysis_iris.ipynb | Jupyter Notebook | Iris ETL Analysis and Exploration |
| data/raw/iris_raw.csv | CSV Dataset | Raw Iris Classification Data |
| data/raw/titanic_raw.csv | CSV Dataset | Raw Titanic Dataset |
| data/staged/iris_transformed.csv | CSV Dataset | Transformed Iris Data |
| scripts/extract_iris.py | Python Script | Iris Data Extraction |
| scripts/extract_titanic.py | Python Script | Titanic Data Extraction |
| scripts/load_iris.py | Python Script | Iris Data Loading |
| scripts/transform_iris.py | Python Script | Iris Data Transformation |
| .env | Configuration | Environment Variables |
| README.md | Documentation | Project Documentation |

## Performance & Scalability

- Current implementation efficiently handles datasets with thousands of records
- Memory-optimized data processing using pandas
- Vectorized operations for fast computations
- Suitable for datasets up to several GB

## Debugging & Troubleshooting

### Common Issues

**Issue**: Module not found error
**Solution**: Install all requirements
```bash
pip install pandas numpy matplotlib seaborn jupyter
```

**Issue**: Jupyter kernel won't start
**Solution**: Reinstall jupyter
```bash
pip install --upgrade jupyter ipython
```

**Issue**: Data file not found
**Solution**: Ensure CSV files are in the correct directories:
- `data/raw/iris_raw.csv`
- `data/raw/titanic_raw.csv`

**Issue**: Environment variables not loading
**Solution**: 
1. Create `.env` file in project root
2. Add your Supabase credentials
3. Restart Jupyter kernel

## Best Practices Implemented

- Clean, readable Python code with comments
- Modular script structure
- Proper error handling and validation
- Consistent naming conventions
- Comprehensive documentation
- Reproducible analysis workflow
- Version control with git
- Separation of raw and processed data

## Learning Outcomes

This project demonstrates proficiency in:
- Data extraction from CSV files
- Data cleaning and preprocessing
- Exploratory Data Analysis (EDA)
- Statistical analysis and visualization
- Python programming with pandas/numpy
- Jupyter notebook usage
- ETL pipeline development
- Database integration (Supabase)
- Data-driven decision making

## Contributing

Feel free to fork this repository and submit pull requests for improvements.

## License

This project is open source and available under the MIT License.

## Author

**Abhinav7301** - Data Science & ETL Project Developer

## Contact & Support

For questions or issues, please:
- Open an issue on GitHub
- Contact the project maintainer

## Acknowledgments

- Iris dataset from UCI Machine Learning Repository
- Titanic dataset from Kaggle
- Python community and libraries used
- Data science best practices and standards

## Project Timeline

- Data extraction pipeline development
- ETL script creation
- Data transformation and cleaning
- Exploratory analysis
- Visualization generation
- Documentation and finalization

## Additional Resources

- [Pandas Documentation](https://pandas.pydata.org/)
- [NumPy Documentation](https://numpy.org/)
- [Matplotlib Documentation](https://matplotlib.org/)
- [Jupyter Documentation](https://jupyter.org/)
- [Seaborn Documentation](https://seaborn.pydata.org/)
- [Supabase Documentation](https://supabase.io/docs/)

## Version History

### v1.0 (Current)
- Iris dataset ETL pipeline
- Titanic data extraction
- Exploratory data analysis
- Python ETL scripts
- Jupyter notebook analysis
- Comprehensive documentation

---

**Last Updated**: December 2024
**Project Status**: Active Development
