# Biopharmaceutical Manufacturing Analytics

A data analytics project that uses Python and Power BI to analyse simulated biopharmaceutical manufacturing batch data.

The project evaluates production yield, process conditions and quality-control results through a reproducible workflow and an interactive Power BI dashboard.

> **Note:** The dataset used in this project is synthetic and was created exclusively for educational and portfolio purposes. It does not contain real company or patient data.

## Dashboard Preview

![Biopharmaceutical Manufacturing Yield Dashboard](images/yield-dashboard.png)

## Project Objective

A biopharmaceutical manufacturing process produces multiple batches under different operating conditions. Each batch contains process information, production results and quality-control outcomes.

The objective of this project is to analyse batch data and answer the following questions:

- What is the average production yield?
- Which batches have low yield?
- How does yield change over time?
- Do yield results differ by product or production line?
- Are temperature, pH or dissolved oxygen values outside their expected ranges?
- Are process conditions associated with production yield?
- How many batches pass or fail the quality-control checks?

## Project Workflow

1. Create a synthetic biopharmaceutical batch dataset.
2. Load and inspect the data using Python and pandas.
3. Clean and transform the dataset.
4. Calculate manufacturing and quality KPIs.
5. Identify low-yield batches and process anomalies.
6. Visualise process and quality results using Python.
7. Export a cleaned dataset for Power BI.
8. Build an interactive manufacturing analytics dashboard.

## Dataset

The synthetic dataset contains 15 manufacturing batches and includes the following categories of information:

### Batch information

- `batch_id`
- `product_name`
- `production_line`
- `start_date`
- `end_date`
- `shift`

### Process parameters

- `reactor_temperature_C`
- `reactor_pH`
- `dissolved_oxygen_pct`
- `agitation_rpm`
- `feed_rate_L_h`

### Production performance

- `biomass_concentration_g_L`
- `product_concentration_g_L`
- `yield_pct`

### Quality-control results

- `qc_purity_pct`
- `qc_potency_pct`
- `qc_contaminants_flag`
- `overall_qc_result`

## Data Analysis

Python and pandas were used to perform the following tasks:

- Load and inspect the manufacturing dataset.
- Check column types and missing values.
- Convert production dates to datetime format.
- Calculate average, minimum and maximum yield.
- Identify batches with yield below the defined threshold.
- Calculate QC pass and fail counts.
- Calculate the overall QC pass rate.
- Compare average yield by product and production line.
- Flag temperature, pH and dissolved oxygen values outside defined operating ranges.
- Create manufacturing performance visualisations.
- Export a cleaned CSV file for Power BI.

## Key Performance Indicators

The analysis produced the following main KPIs:

- **Total batches:** 15
- **Average batch yield:** 86.11%
- **QC passed batches:** 12
- **QC failed batches:** 3
- **QC pass rate:** 80%

## Power BI Dashboard

The Power BI dashboard includes:

- Average yield KPI.
- QC passed and failed batch counts.
- Batch yield over time.
- Average yield by product.
- Average yield by production line.
- Yield versus reactor temperature.
- Yield versus reactor pH.
- Product slicer.
- Production-line slicer.

The slicers allow users to investigate manufacturing performance for individual products and production lines.

## Main Insights

- The overall average production yield was approximately 86.11%.
- Twelve of the fifteen batches passed the overall QC assessment.
- Three batches failed the overall QC assessment.
- Production yield varied between batches, products and production lines.
- The process-parameter scatter plots make it possible to explore whether reactor temperature or pH is associated with yield.
- Low-yield and failed batches can be investigated individually using the dashboard filters.

## Technologies

- Python
- pandas
- matplotlib
- Jupyter Notebook
- Power BI
- Visual Studio Code
- Git and GitHub

## Repository Structure

```text
biopharma-manufacturing-analytics/
│
├── data/
│   ├── batches_raw.csv
│   └── batches_clean_for_powerbi.csv
│
├── notebooks/
│   └── biopharma_analysis.ipynb
│
├── powerbi/
│   └── biopharma_dashboard.pbix
│
├── images/
│   └── dashboard.png
│
├── README.md
├── requirements.txt
└── .gitignore
```

## How to Run the Python Analysis

### 1. Clone the repository

```bash
git clone [https://github.com/YOUR-USERNAME/biopharma-manufacturing-analytics.git](https://github.com/YOUR-USERNAME/biopharma-manufacturing-analytics.git)
```

### 2. Open the project folder

```bash
cd biopharma-manufacturing-analytics
```

### 3. Install the required libraries

```bash
pip install -r requirements.txt
```

### 4. Open the notebook

Open the following file in Jupyter Notebook or Visual Studio Code:

```text
notebooks/biopharma_analysis.ipynb
```

Run the notebook cells in order.

## Power BI Instructions

1. Open Power BI Desktop.
2. Open `powerbi/biopharma_dashboard.pbix`.
3. If the data source cannot be found, reconnect it to:

```text
data/batches_clean_for_powerbi.csv
```

4. Use the product and production-line slicers to interact with the dashboard.

## Limitations

- The dataset is synthetic and does not represent an actual pharmaceutical manufacturing process.
- The dataset contains only 15 batches.
- Operating ranges were defined for demonstration and are not validated manufacturing specifications.
- Correlations in the dataset should not be interpreted as proof of causation.
- The project is intended to demonstrate a data-analysis workflow rather than support real batch-release decisions.

## Future Improvements

- Include more batches and a longer production period.
- Add batch-duration and productivity KPIs.
- Calculate correlations between process parameters and yield.
- Add statistical process-control charts.
- Develop anomaly-detection methods.
- Add predictive models for yield and QC outcomes.
- Connect Power BI to an automatically updated data source.

## Author

**Angel HK**  
Biotechnology Engineering student interested in bioprocessing, manufacturing analytics and scientific data analysis.

## License

This project is available for educational and portfolio purposes.
