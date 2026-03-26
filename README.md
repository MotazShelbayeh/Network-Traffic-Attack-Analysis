# Network-Traffic-Attack-Analysis

## Step One: Data preprocessing 

### 1) Handling Missing Value
In this step, missing values in the dataset were identified using df.isna().sum() to understand the distribution of null values across columns. Based on the results, appropriate handling techniques were applied:
  *Columns with categorical or status-based data were filled with meaningful labels instead of leaving them empty:
     -Alerts/Warnings: Converted to binary labels (yes / no) to simplify analysis.
     -Malware Indicators: Missing values replaced with "No Detection".
     -Proxy Information: Missing values replaced with "No proxy".
     -Firewall Logs and IDS/IPS Alerts: Missing values replaced with "No Data".
     
### 2) Check Duplicate
Checked for duplicate records using df.duplicated(), and no duplicates were found, ensuring data consistency and accuracy.

### 3) Split Device Information Column into Browser and Operating system
Separated the Device Information column into Browser and Operating System to improve data analysis and enable more detailed insights.

### 4) Convert Timestamp format into datetime
In this step, the Timestamp column was converted into a proper datetime format using appropriate functions (e.g., pd.to_datetime()). This transformation ensures that time-based data is accurately interpreted and can be used for analysis.

Converting the timestamp enables efficient time-series analysis, such as tracking traffic patterns over time, identifying peak activity periods, and detecting anomalies. It also improves sorting, filtering, and aggregation operations based on date and time.

### 5) Numerical Data Statistics
In this step, statistical summaries were generated for all numerical columns in the dataset using methods such as df.describe(). Key metrics including mean, median, standard deviation, minimum, and maximum values were analyzed to understand the distribution and behavior of the data.

<img width="673" height="354" alt="image" src="https://github.com/user-attachments/assets/b88139c1-7583-4c15-9f13-535bfbbcffbd" />
