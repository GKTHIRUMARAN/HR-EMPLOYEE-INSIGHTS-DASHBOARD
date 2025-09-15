HR Employee Insights Dashboard

📌 Project Overview
The HR Employee Insights Dashboard is an interactive web application built with Streamlit, designed to provide comprehensive analytics on employee data. This dashboard empowers HR professionals and data analysts to:

- Visualize Key Metrics: Gain insights into employee attrition, satisfaction, income distribution, and more.
- Upload and Merge Data: Seamlessly upload new employee datasets and merge them with existing records.
- Column Mapping Interface: Automatically map and align mismatched column names during data uploads to ensure consistency.
- Data Filtering: Apply dynamic filters to analyze specific subsets of the workforce.

Downloadable Reports: Export filtered datasets for further analysis or reporting.

🛠️ Technologies Used
Streamlit for building the interactive web application
Pandas for data manipulation and analysis
Plotly for creating interactive visualizations
Python as the primary programming language
Docker for containerizing the application for cloud deployment
GCP Cloud Run for deploying the app as a scalable serverless service

🚀 Features
Dynamic KPIs: Real-time metrics such as total employees, attrition rate, and average monthly income
Interactive Visualizations: Charts depicting attrition by department, job role, age distribution, and more
Column Mapping UI: User-friendly interface to map and align columns during data uploads
Data Filtering: Sidebar filters to segment data by department, gender, and other attributes
Data Export: Option to download the filtered dataset as a CSV file

📁 Installation & Setup
Prerequisites
Python 3.7 or higher
Docker (optional for containerization or cloud deployment)
Recommended: use a virtual environment

Steps
Clone the repository:
git clone https://github.com/GKTHIRUMARAN/HR-Employee-Insights-Dashboard.git

cd hr-employee-dashboard

Install dependencies:
pip install -r requirements.txt

Run locally:
streamlit run app.py
Access the dashboard at http://localhost:8501

🐳 Docker Setup (Optional)
Build Docker image:
docker build -t hr-dashboard .

Run container locally:
docker run -p 8501:8501 hr-dashboard
Check dashboard at http://localhost:8501

☁️ GCP Deployment Steps
Authenticate and set project:
gcloud auth login
gcloud config set project hr-insights-472208

Enable required services:
gcloud services enable run.googleapis.com cloudbuild.googleapis.com

Build container on Cloud Build:
gcloud builds submit --tag gcr.io/hr-insights-472208/hr-dashboard

Deploy to Cloud Run:
gcloud run deploy hr-dashboard --image gcr.io/hr-insights-472208/hr-dashboard --platform managed --region asia-south1 --allow-unauthenticated --port 8501

After deployment, you will get a public URL for your live dashboard.

you can see my cloud deploy:https://hr-dashboard-20663453869.asia-south1.run.app

🔄 Data Flow
Upload Data: Users upload CSV employee datasets
Column Mapping: Mismatched columns are mapped to the standard schema
Data Merge: New data is merged with existing records, avoiding duplicates
Data Analysis: KPIs and visualizations update dynamically
Data Export: Download filtered datasets or the full updated dataset as CSV

📄 License
This project is licensed under the MIT License, see the LICENSE file for details
