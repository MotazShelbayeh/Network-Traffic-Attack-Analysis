# Network Traffic Attack Analysis

## Project Overview
This project analyzes network traffic attacks to provide insights into patterns, targeted devices, and response strategies. The analysis focuses on detecting anomalies, understanding attack distributions, and visualizing trends to improve network security measures.

The dataset contains over **40,000 attack records** with detailed information about devices, protocols, packet types, and attack severity levels.

---

## Step One: Data Preprocessing

### 1) Handling Missing Values
Missing values were identified using `df.isna().sum()` and handled appropriately:

- **Alerts/Warnings:** Converted to binary labels (Yes / No).  
- **Malware Indicators:** Missing values replaced with `"No Detection"`.  
- **Proxy Information:** Missing values replaced with `"No proxy"`.  
- **Firewall Logs and IDS/IPS Alerts:** Missing values replaced with `"No Data"`.  

### 2) Checking for Duplicates
Duplicate records were checked using `df.duplicated()` and no duplicates were found, ensuring data consistency and accuracy.

### 3) Splitting Device Information
The `Device Information` column was split into **Browser** and **Operating System** columns to enable more detailed analysis.

### 4) Converting Timestamp
The `Timestamp` column was converted to proper datetime format using `pd.to_datetime()`, enabling accurate time-based analysis for trends, peak activity periods, and anomaly detection.

### 5) Numerical Data Statistics
Statistical summaries were generated using `df.describe()`, providing key metrics such as:

- Mean, Median  
- Standard Deviation  
- Minimum and Maximum values  

![Numerical Data Statistics](<img width="673" height="354" alt="Screenshot 2026-03-26 153213" src="https://github.com/user-attachments/assets/3ad44bda-771e-4c13-af86-32064477b96a"/>)

---

## Step Two: Data Visualization

The visual analysis was performed using Tableau. An interactive dashboard is available [here](https://public.tableau.com/app/profile/motaz.shelbayeh/viz/NetworkTrafficAttack/NETWORKTRAFFICATTACK).

![Network Traffic Attack Dashboard](<img width="1683" height="877" alt="{A1337299-140C-49A3-AF69-6913CDF93A6A}" src="https://github.com/user-attachments/assets/867b58eb-b875-4da6-a366-d6536716ca75"/>)

### Key Insights:

1. **Operating System Targeting:**  
   - Windows is the most targeted OS, followed by Linux and macOS.

2. **Browser Targeting:**  
   - Mozilla-based browsers experience significantly more attacks compared to Opera.

3. **Attack Types & Severity:**  
   - DDoS, Intrusion, and Malware attacks span different severity levels, with consistently high volumes.

4. **Network Protocols & Traffic:**  
   - Traffic is fairly balanced across TCP, UDP, ICMP protocols and HTTP, FTP, DNS traffic types.

5. **Packet Distribution:**  
   - Control vs Data packets are nearly evenly distributed.

6. **Network Segments:**  
   - Attacks are spread almost equally across network segments A, B, and C.

7. **Response Actions:**  
   - Actions such as Blocked, Ignored, and Logged are balanced, indicating consistent security strategies.

---

## Datafolio Overview

![Datafolio Overview](<img width="1920" height="1080" alt="Datafolio" src="https://github.com/user-attachments/assets/597ef692-2059-4716-9c3e-27f95d0bca8d"/>)

The **Datafolio** image summarizes the entire project workflow, from data preprocessing to visualization and insights.

---

## Tools & Technologies Used

- **Python (pandas, numpy)** – Data preprocessing & analysis  
- **Matplotlib / Seaborn** – Data visualization  
- **Tableau** – Interactive dashboards  
- **Jupyter Notebook** – Project documentation & analysis  

---

## Conclusion

This project provides a comprehensive analysis of network traffic attacks. It identifies key trends, targeted devices, and attack distributions, helping organizations enhance their network security measures and response strategies.
