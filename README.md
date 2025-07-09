# Procurement KPI Analytics

A comprehensive data analytics and business intelligence project focused on procurement performance optimization through advanced KPI analysis, supplier performance evaluation, and predictive modeling.

## Project Objectives

This project aims to transform raw procurement data into actionable insights that drive strategic decision-making and operational excellence. Our primary goals include:

-   **Supplier Performance Optimization**: Identify top-performing suppliers and improvement opportunities
-   **Cost Reduction Analysis**: Quantify savings through negotiation and strategic sourcing
-   **Quality Assurance**: Monitor and predict quality issues across the supply chain
-   **Delivery Performance**: Optimize logistics and reduce lead times
-   **Compliance Monitoring**: Ensure regulatory and contractual compliance across all procurement activities
-   **Predictive Analytics**: Forecast future procurement trends and potential risks

## Dataset Overview

Our analysis is based on a comprehensive procurement dataset containing **777 procurement transactions** with the following key attributes:

| Column | Type | Description |
|----|----|----|
| `PO_ID` | String | Unique purchase order identifier |
| `Supplier` | String | Supplier/vendor name |
| `Order_Date` | Date | Purchase order creation date |
| `Delivery_Date` | Date | Actual delivery date |
| `Item_Category` | String | Product/service category |
| `Order_Status` | String | Current order status (Completed, Pending, Cancelled) |
| `Quantity` | Integer | Number of units ordered |
| `Unit_Price` | Float | Original unit price |
| `Negotiated_Price` | Float | Final negotiated unit price |
| `Defective_Units` | Float | Number of defective units received |
| `Compliance` | String | Compliance status (Compliant, Non-Compliant) |

## Key Performance Indicators (KPIs)

### Supplier Performance KPIs

-   **On-Time Delivery Rate** = (On-time deliveries / Total deliveries) × 100
-   **Quality Performance** = ((Total units - Defective units) / Total units) × 100
-   **Price Competitiveness** = Average negotiated price vs. market benchmarks
-   **Compliance Rate** = (Compliant orders / Total orders) × 100
-   **Supplier Reliability Score** = Composite score based on delivery, quality, and compliance

### Financial KPIs

-   **Cost Savings** = (Unit Price - Negotiated Price) × Quantity
-   **Total Procurement Spend** = Sum of all procurement values
-   **Average Order Value** = Total spend / Number of orders
-   **Price Variance** = Standard deviation of negotiated prices by category
-   **ROI on Negotiations** = Total savings / Total procurement spend

### Operational KPIs

-   **Average Lead Time** = Average days between order and delivery
-   **Order Fulfillment Rate** = (Completed orders / Total orders) × 100
-   **Category Performance** = Performance metrics segmented by item category
-   **Defect Rate** = (Defective units / Total units) × 100

### Strategic KPIs

-   **Supplier Diversification Index** = Number of active suppliers / Total suppliers
-   **Risk Exposure** = Percentage of spend with high-risk suppliers
-   **Compliance Violations** = Number and severity of compliance issues

## Project Structure

```         
procurement-kpi-analytics/
│
├── data/
│   ├── raw/                    # Original, immutable data
│   ├── interim/                # Intermediate transformed data
│   ├── processed/              # Final datasets for analysis
│   └── external/               # Third-party reference data
│
├── notebooks/               # Jupyter notebooks for analysis
│   ├── 01_data_exploration.ipynb
│   ├── 02_data_cleaning.ipynb
│   ├── 03_feature_engineering.ipynb
│   ├── 04_kpi_analysis.ipynb
│   ├── 05_supplier_performance.ipynb
│   ├── 06_predictive_modeling.ipynb
│   └── 07_final_report.ipynb
│
├── src/                     # Source code modules
│   ├── data/                   # Data processing utilities
│   ├── features/               # Feature engineering
│   ├── models/                 # Machine learning models
│   ├── visualization/          # Plotting and dashboard code
│   └── utils/                  # Helper functions
│
├── models/                  # Trained models and predictions
├── reports/                 # Generated reports and visualizations
├── docs/                    # Project documentation
├── config/                  # Configuration files
├── tests/                   # Unit tests
└── scripts/                 # Automation scripts
```

## Getting Started

### Prerequisites

-   Python 3.8 or higher
-   Git
-   Jupyter Notebook or JupyterLab
-   Recommended: Anaconda or Miniconda

### Installation

1.  **Clone the repository**

    ``` bash
    git clone https://github.com/yourusername/procurement-kpi-analytics.git
    cd procurement-kpi-analytics
    ```

2.  **Create virtual environment**

    ``` bash
    # Using conda (recommended)
    conda env create -f environment.yml
    conda activate procurement-analytics

    # Or using pip
    python -m venv venv
    source venv/bin/activate  # On Windows: venv\Scripts\activate
    pip install -r requirements.txt
    ```

3.  **Install the package in development mode**

    ``` bash
    pip install -e .
    ```

4.  **Verify installation**

    ``` bash
    python -c "import src; print('Installation successful!')"
    ```

## Usage Examples

### Quick Start Analysis

``` python
# Load and explore the data
from src.data.data_loader import load_procurement_data
from src.features.kpi_calculator import calculate_all_kpis

# Load data
df = load_procurement_data('data/raw/Procurement_KPI_Analysis_Dataset.csv')

# Calculate KPIs
kpis = calculate_all_kpis(df)
print(f"Overall supplier performance: {kpis['avg_supplier_score']:.2f}")
```

### Generate Supplier Performance Report

``` python
from src.visualization.dashboard import create_supplier_dashboard

# Create interactive dashboard
dashboard = create_supplier_dashboard(df)
dashboard.show()
```

### Run Complete Analysis Pipeline

``` bash
# Execute the full analysis pipeline
python scripts/run_pipeline.py

# Generate executive report
python scripts/generate_report.py --output-format pdf
```

## Analysis Workflows

### 1. Exploratory Data Analysis

-   Data quality assessment
-   Missing value analysis
-   Distribution analysis
-   Correlation analysis

### 2. KPI Calculation & Benchmarking

-   Calculate all procurement KPIs
-   Compare against industry benchmarks
-   Identify performance outliers

### 3. Supplier Performance Analysis

-   Rank suppliers by composite performance score
-   Identify high-risk suppliers
-   Analyze supplier diversity

### 4. Predictive Modeling

-   Delivery time prediction
-   Quality issue prediction
-   Supplier risk assessment
-   Demand forecasting

### 5. Reporting & Visualization

-   Executive dashboards
-   Detailed analytical reports
-   Interactive visualizations
-   Automated reporting

## Key Features

-   **Automated KPI Calculation**: Streamlined computation of all procurement metrics
-   **Interactive Dashboards**: Real-time visualization of key performance indicators
-   **Supplier Scorecards**: Comprehensive supplier evaluation framework
-   **Predictive Analytics**: Machine learning models for forecasting and risk assessment
-   **Automated Reporting**: Generate executive and technical reports automatically
-   **Data Quality Monitoring**: Built-in data validation and quality checks
-   **Configurable Thresholds**: Customizable performance benchmarks and alerts

## Contact & Support

-   **Project Repository**: <https://github.com/m4fu045/kaggle-procurement-kpi-analysis-dataset-insights.git>
-   **Email**: candice.chang1029\@gmail.com

## Acknowledgments

-   Data source: <https://www.kaggle.com/datasets/shahriarkabir/procurement-kpi-analysis-dataset/data>
-   Built with Python, Pandas, Scikit-learn, and Plotly

------------------------------------------------------------------------

**Last Updated**: 07/08/2025

------------------------------------------------------------------------

*This project is part of the digital transformation initiative to optimize procurement operations through data-driven insights.*
