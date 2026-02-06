CSCN8010 Practical Lab 1: Predictive Maintenance with Linear Regression-Based Alerts

Student: Lohith Reddy Danda

## Project Overview

- Data cleaning and preprocessing  
- Linear regression modeling for each axis  
- Residual analysis  
- Manual thresholding (MinC, MaxC, T)  
- Alert and error detection  
- Streaming simulation (row‑by‑row real‑time processing)  
- Event logging (start time, end time, duration)  
- Visualizations for model performance  
- Cloud database integration using Neon PostgreSQL

## Project Structure
│── data/
│   ├── alerts## 📁 Project Structure (Table View)

| Path / File | Description |
|------------|-------------|
| **data/** | Folder containing all datasets |
| ├── alerts_log.csv | Logged alerts from streaming simulation |
| ├── RMBR4-2_export_test.csv | Raw robot test dataset |
| ├── test_data_synthetic.csv | Synthetic test dataset |
| **notebooks/** | Jupyter notebooks for analysis |
| └── analysis.ipynb | Full pipeline: cleaning → regression → alerts → SQL → plots |
| **src/** | Source code modules |
| ├── __init__.py | Package initializer |
| ├── alerts.py | Alert & error classification logic |
| ├── plots.py | Visualization functions |
| ├── regression.py | Linear regression + residual calculations |
| ├── streaming_sim.py | Real‑time streaming simulation |
| ├── thresholds.py | MinC, MaxC, T threshold definitions |


#Create and activate a virtual environment:python -m venv venv venv\Scripts\activate  
# Windows source venv/bin/activate   # Mac/Linux

#
Install dependencies: pip install -r requirements.txt


The file includes:
 pandas 
  numpy
matplotlib
 scikit-learn
 sqlalchemy 
 psycopg2-binary
 jupyter 
 python-dotenv



---

##  How to Run the Notebook

Start Jupyter:jupyter notebook

Open:notebooks/analysis.ipynb


Run all cells in order to reproduce:

- data cleaning  
- regression modeling  
- thresholding  
- alert/error detection  
- streaming simulation  
- event logging  
- SQL integration  
- visualizations  

---

##  SQL Database Setup (Neon)

Create a `.env` file in the project root:
Run all cells in order to reproduce:

- data cleaning  
- regression modeling  
- thresholding  
- alert/error detection  
- streaming simulation  
- event logging  
- SQL integration  
- visualizations  

---

##  SQL Database Setup (Neon)

Create a `.env` file in the project root:
DB_USER=neondb_owner 
DB_PASS=your_password_here 
DB_HOST=your_host_here
DB_NAME=neondb


Ensure `.env` is **not** committed to GitHub.

Load environment variables in the notebook:

'''python
from dotenv import load_dotenv
import os

load_dotenv()'''
The notebook will automatically connect to your Neon PostgreSQL database.

#Project Workflow
- Load raw robot current data
- Clean and preprocess
- Fit linear regression models
- Compute residuals
- Apply MinC, MaxC, T thresholds
- Detect alerts and errors
- Simulate real‑time streaming
- Log events (start, end, duration)
- Store and load data from Neon SQL
- Generate visualizations

 #Results
- Regression models successfully captured expected current behavior
- Residuals revealed abnormal patterns
- Alerts and errors were detected correctly
- Streaming simulation behaved like a real robot controller
- Event logging captured accurate start/end times
- SQL integration worked smoothly
- Visualizations confirmed the anomaly detection pipeline

# Conclusion
This project demonstrates a complete predictive maintenance pipeline for a multi‑axis robotic system. It includes data cleaning, regression modeling, thresholding, real‑time simulation, event logging, SQL integration, and visualizations. The system is fully reproducible and ready for deployment or further research.
