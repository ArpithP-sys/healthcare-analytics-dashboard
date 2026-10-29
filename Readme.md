# Healthcare Analytics & Executive Dashboard

**A Python-based healthcare data analysis project with an interactive HTML executive dashboard.**

## 1. Project Overview
Healthcare organizations generate large amounts of data related to patient admissions, medical conditions, insurance providers, treatment costs, and hospital stays. Analyzing this data can help identify operational patterns, monitor billing, and support data-driven decision-making.
This project explores a synthetic healthcare dataset using Python for data cleaning, exploratory data analysis (EDA), visualization, and business-focused ad-hoc analysis. An executive dashboard built using HTML, CSS, and JavaScript presents key performance indicators (KPIs), trends, comparisons, and business insights in an accessible format.

**Project objectives:**
- Cleaning and preparing healthcare admission data for analysis.
- Understanding patient demographics and medical-condition distributions.
- Analyze billing patterns, insurance-provider distribution, and admission trends.
- Answeing business questions through data analysis.
- Presenting key findings and recommendations through an executive dashboard.

## 2. Dataset Information
The project uses a synthetic healthcare dataset originally containing **55,500 records and 15 columns**.
The dataset includes information about patients, admissions, billing, and healthcare services.

| Column | Description |
|---|---|
| Name | Patient name |
| Age | Patient age at admission |
| Gender | Patient gender |
| Blood Type | Patient blood group |
| Medical Condition | Primary medical condition |
| Date of Admission | Admission date |
| Doctor | Responsible doctor |
| Hospital | Hospital name |
| Insurance Provider | Patient's insurance provider |
| Billing Amount | Amount billed for healthcare services |
| Room Number | Assigned room number |
| Admission Type | Emergency, Elective, or Urgent |
| Discharge Date | Patient discharge date |
| Medication | Medication administered or prescribed |
| Test Results | Normal, Abnormal, or Inconclusive |

**Dataset characteristics:**
- Original records: 55,500
- Original columns: 15
- Data type: Synthetic healthcare data
- Primary analysis focus: Patient demographics, admissions, billing, insurance, and test results

The dataset was generated for educational and analytical purposes and does not represent actual patient records.

## 3. Tools and Technologies
- **Python:** Data analysis and preprocessing
- **Pandas:** Data manipulation, aggregation, and analysis
- **NumPy:** Numerical operations
- **Matplotlib:** Data visualization
- **Jupyter Notebook:** Analysis and documentation
- **HTML:** Dashboard structure
- **CSS:** Dashboard styling and layout
- **JavaScript:** Dashboard interactions and filtering

## 4. Data Cleaning and Preprocessing
The original dataset was inspected and prepared before analysis.
The following steps were performed:

1. **Duplicate removal:** Identified and removed 534 duplicate records, reducing the dataset from 55,500 to 54,966 records.
2. **Text standardization:** Standardized patient-name formatting for consistency.
3. **Invalid billing values:** Handled negative billing values using mean imputation.
4. **Date conversion:** Converted admission and discharge dates into datetime format.
5. **Feature engineering:** Created a `Length_of_Stay` feature using admission and discharge dates.
6. **Missing-value checks:** Checked the cleaned dataset for missing values.
7. **Data validation:** Reviewed data types and the resulting dataset before conducting EDA.

**Final dataset size: 54,966 records.**

## 5. Exploratory Data Analysis (EDA)
EDA was performed using Python, Pandas, and Matplotlib to understand distributions, trends, and relationships in the data.

### Analyses performed
- Medical-condition distribution
- Patient age distribution
- Average billing trends over time
- Relationship between patient age and billing amount
- Insurance-provider patient distribution and share
- Emergency admissions by calendar month
- High-cost admission analysis
- Emergency admissions with abnormal test results

### Key findings
The dashboard highlights the following descriptive findings from the cleaned dataset:

- **Patient admissions:** 54,966 records were analyzed.
- **Total billing:** Approximately $1.41 billion.
- **Average billing:** Approximately $25,595 per admission.
- **Average length of stay:** Approximately 15.5 days.
- **Emergency admissions:** 18,102, representing approximately 32.9% of records.
- **High-cost admissions:** 5,497 records, based on the 90th-percentile billing threshold.
- **Emergency admissions with abnormal test results:** 6,038 records.
- **Patient demographics:** Average patient age is approximately 51.5 years, with patients aged 60 or older accounting for approximately 38.1% of admissions.

These figures describe the synthetic dataset and are not evidence of actual hospital performance.

## 6. Ad-Hoc Business Questions
Ad-hoc analysis involves answering specific business questions using data, calculations, filtering, grouping, and visualization.

The following questions were explored in the project.

### Q1. Which medical conditions account for the most admissions?
**Analysis:** Examined the distribution of records across the six medical conditions using grouping and visualization.

**Business value:** Helps understand the distribution of recorded conditions and identify areas for further resource-planning analysis.

### Q2. What is the relationship between patient age and treatment cost?
**Analysis:** Used a scatter plot to visualize patient age against billing amount.

**Business value:** Helps explore whether billing patterns vary with patient age and whether further statistical analysis is warranted.

### Q3. How does average billing change over time?
**Analysis:** Examined monthly average billing trends using admission dates and aggregated billing amounts.

**Business value:** Helps identify periods with higher or lower average billing and determine whether further investigation is needed.

### Q4. Which insurance providers account for the largest share of admissions?
**Analysis:** Calculated patient-record counts and shares by insurance provider.

**Business value:** Helps summarize the distribution of admissions across insurance providers and supports further analysis of payer mix.

### Q5. How many emergency admissions occur in each calendar month?
**Analysis:** Filtered emergency admissions and grouped records by month.

**Business value:** Helps identify monthly admission patterns that could be examined further for staffing and capacity planning.

### Q6. Which admissions have unusually high billing amounts?
**Analysis:** Used the 90th percentile of billing amounts as a threshold to identify high-cost admissions.

**Business value:** Supports billing review, cost monitoring, and further investigation of unusually expensive cases.

### Q7. How many emergency admissions have abnormal test results?
**Analysis:** Filtered records where the admission type is Emergency and the test result is Abnormal.

**Business value:** Helps identify a group of records for additional review and supports descriptive monitoring of emergency admissions.

## 7. Executive Dashboard
An executive dashboard was developed using HTML, CSS, and JavaScript to communicate the analysis through a management-friendly interface.

### Dashboard features

**KPI cards**
- Total admissions
- Total billing
- Average billing
- Average length of stay
- Emergency admission share
- High-cost admission count

**Interactive filters**
- Medical condition
- Insurance provider
- Gender
- Admission type
- Year

**Visualizations**
- Medical-condition distribution
- Patient age distribution
- Monthly billing trends
- Age versus billing scatter plot
- Insurance-provider share
- Emergency admission analysis

**Management insights**

The dashboard summarizes important patterns and presents findings that can guide further operational investigation.

## 8. Business Recommendations
The analysis suggests several areas where a healthcare organization could investigate its operations further.

### 1. Monitor high-cost admissions
**Finding:** 5,497 records fall into the high-cost group defined by the 90th-percentile billing threshold.

**Recommendation:** Review high-billing records to understand which services, admission types, or other factors contribute to higher costs. Validate unusual charges before making operational decisions.

### 2. Review emergency admission patterns
**Finding:** Emergency admissions account for approximately 32.9% of the records.

**Recommendation:** Examine admission volumes across months and compare them with actual staffing and bed-capacity information before adjusting resource allocation.

### 3. Investigate abnormal test results in emergency admissions
**Finding:** 6,038 emergency admission records have abnormal test results.

**Recommendation:** Use appropriate clinical review processes to investigate these records. Do not treat this count alone as evidence of patient deterioration or medical risk.

### 4. Evaluate insurance-provider distribution
**Finding:** Admissions are distributed across multiple insurance providers.

**Recommendation:** Monitor admission volume, average billing, and billing variation by provider. Investigate differences while accounting for the types of services and patients involved.

### 5. Investigate billing trends
**Finding:** Monthly average billing varies over time.

**Recommendation:** Compare monthly billing with admission volume, service mix, and other relevant operational data to understand the reasons for fluctuations.

### 6. Examine patient demographics and cost patterns
**Finding:** The dataset contains patients across a wide age range.

**Recommendation:** Investigate billing patterns across age groups and medical conditions to determine whether meaningful differences exist. Use statistical analysis before drawing conclusions.

**Important:** These recommendations are exploratory suggestions based on synthetic data. They are not validated clinical or operational recommendations for a real hospital.

## 9. Project Workflow

The project follows a typical data analytics workflow:

1. **Data collection:** Load the synthetic healthcare dataset.
2. **Data cleaning:** Remove duplicates, standardize fields, handle invalid values, and convert dates.
3. **Feature engineering:** Calculate length of stay.
4. **Exploratory data analysis:** Examine distributions, trends, and relationships.
5. **Ad-hoc analysis:** Answer specific business questions through filtering and aggregation.
6. **Visualization:** Create charts using Matplotlib.
7. **Dashboard development:** Present key metrics and findings using HTML, CSS, and JavaScript.
8. **Business recommendations:** Identify areas for further investigation based on the analysis.

## 10. Repository Structure
- `healthcare.ipynb` — Python data cleaning, EDA, visualizations, and ad-hoc analysis.
- `index.html` — Executive dashboard website.
- `README.md` — Project documentation.

Update the file structure if your actual repository uses different filenames.

## 11. How to Run the Project

### Run the Python notebook
1. Clone or download the repository.
2. Install Python and Jupyter Notebook, or use VS Code.
3. Install the required packages:

```bash
pip install pandas numpy matplotlib jupyter
```

4. Place the dataset in the location expected by the notebook.
5. Open `healthcare.ipynb`.
6. Run the cells in sequence.

### Open the dashboard locally
Open `index.html` in a web browser.

If the dashboard depends on external files, keep the files in their expected relative locations.

### Publish the dashboard using GitHub Pages
1. Upload the project files to a public GitHub repository.
2. Ensure `index.html` is in the repository root.
3. Open **Settings → Pages**.
4. Select **Deploy from a branch**.
5. Choose the `main` branch and `/(root)` folder.
6. Save and wait for deployment.
7. Open the published website using the URL shown in GitHub Pages settings.

## 12. Limitations and Future Improvements

- The dataset is synthetic and may not reflect real healthcare operations.
- Billing values and admission patterns should not be generalized to actual hospitals.
- Mean imputation of negative billing values may affect the distribution; alternative data-quality treatments should be evaluated.
- Correlation and descriptive comparisons do not establish causation.
- Future work could include SQL-based analysis, Power BI reporting, statistical testing, and a separately validated multi-class classification model for test results.
- A machine-learning model should only be included after defining the target, evaluating the model, and reporting appropriate performance metrics.

## 13. Conclusion
This project demonstrates an end-to-end descriptive analytics workflow, from healthcare data cleaning and exploratory analysis to business-question investigation and executive dashboard development.
By combining Python analysis with an interactive web dashboard, the project presents data in a structured and accessible format, highlighting billing patterns, patient demographics, insurance distribution, and emergency admissions.
The project demonstrates practical skills in data preprocessing, EDA, visualization, business analysis, and communicating findings to stakeholders.

## Disclaimer
This project is for educational and portfolio purposes only. The dataset is synthetic and contains no real patient information. The findings and recommendations should not be used for clinical diagnosis, treatment decisions, or actual hospital operational decisions without appropriate validation.
