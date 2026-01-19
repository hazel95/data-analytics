## 📈 Project Workflow

### 🛠 Step 1: Data Preparation
- **Import data**: Load copy of the original dataset (CSV) into Power BI.  
- **Clean data**:
  - Handle missing values and null(e.g., bureau scores, document flags).  
  - Standardize categorical fields (employment type, manufacturer, state).  
  - Convert dates (DOB, disbursement date) into usable features (age, loan age).
  - Remove unnecessary columns  
- **Create calculated columns**:  
  - Loan-to-value ratio (verify consistency).  
  - Customer age = `DATEDIFF([DOB], [DisbursementDate], YEAR)`.  
  - Debt-to-income proxy (if income data is available later).  

---

### 📊 Step 2: Exploratory Analysis in Power BI
- **Loan Portfolio Dashboard**:  
  - Total disbursement by branch, dealer, manufacturer.  
  - Average loan amount vs asset cost.  
- **Customer Profile Dashboard**:  
  - Age distribution, employment type breakdown.  
  - Documentation completeness (PAN, Aadhaar, etc.).  
- **Credit Bureau Dashboard**:  
  - Bureau score distribution.  
  - Active loans vs defaults per customer.  
  - Outstanding principal vs sanctioned amounts.  

---

### 📈 Step 3: Risk & Default Analysis
- **Default Segmentation**:  
  - Compare default rates by employment type, manufacturer, branch.  
  - Correlate bureau scores with defaults.  
- **Behavioral Insights**:  
  - New loans in last 6 months vs defaults in last 6 months.  
  - First EMI default flag analysis.  
- **Trend Analysis**:  
  - Defaults over time (monthly/quarterly).  
  - Loan tenure vs default probability.  

---

### 🤖 Step 4: Predictive Modeling (outside Power BI)
- **Export dataset**: Save cleaned data from Power BI into CSV/Excel.  
- **Model training in Python/R**:  
  - Classification models: Logistic Regression, Random Forest, XGBoost.  
  - Features: bureau score, loan-to-value, documentation flags, loan history, EMI amounts.  
  - Target: Default flag (e.g., first EMI default or historical defaults).  
- **Evaluate model**:  
  - Accuracy, precision, recall, ROC-AUC.  
  - Feature importance (which variables drive defaults).  

---

### 🔗 Step 5: Integration Back into Power BI
- **Import predictions**: Bring model outputs (default probability scores) back into Power BI.  
- **Risk Dashboard**:  
  - Segment customers into risk tiers (low, medium, high).  
  - Compare predicted vs actual defaults.  
- **Scenario Analysis**:  
  - Simulate stricter credit score thresholds.  
  - Visualize impact on default rates and loan approvals.  

