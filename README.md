# **Customer Segmentation Prediction**  

![Customer Clusters](artifacts/cluster_visualization.png)  

## **📌 Overview**  
This project uses **K-Means clustering** to segment customers into distinct groups based on their:  
- **Annual Income (USD)**  
- **Spending Score (0-100 scale)**  
- **Savings (USD)**  
- **Age (years)**  

The goal is to help businesses **personalize marketing strategies**, improve **customer targeting**, and optimize **loyalty programs**.  

🔗 **Live Demo (Streamlit App):** [Link to App](#) *(Coming Soon)*  

---

## **🎯 Objectives**  
✅ **Identify meaningful customer clusters** (e.g., high spenders, budget-conscious, young professionals).  
✅ **Automate data preprocessing** for efficient model training.  
✅ **Track experiments** using **MLflow** for reproducibility.  
✅ **Deploy an interactive dashboard** (Streamlit) for businesses to visualize and predict customer segments.  

---

## **🔍 Problem Solved**  
Many businesses struggle with:  
❌ **Generic marketing** (one-size-fits-all promotions).  
❌ **Poor customer insights** (no segmentation).  
❌ **Manual data analysis** (time-consuming, error-prone).  

This project solves these by:  
✔ **Automating customer grouping** using ML.  
✔ **Providing actionable insights** (e.g., "Which customers respond best to discounts?").  
✔ **Enabling real-time predictions** via a **Streamlit dashboard**.  

---

## **📂 Project Structure**  
```
📂 Customer_Segmentation/  
├── 📂 data/  
│   └── segmentation_data.csv  
├── 📂 artifacts/  
│   ├── correlation_matrix.png  
│   ├── distribution_income.png  
│   ├── elbow_method.png  
│   └── cluster_visualization.png  
├── 📜 EDA.py  
├── 📜 train_model.py  
├── 📜 app.py (Streamlit)  
└── 📜 README.md  
```

---

## **⚙️ Workflow**  
1. **📤 Data Uploading**  
   - Input: `segmentation_data.csv` (customer records).  
   - Columns: `annual_income`, `spending_score`, `savings`, `age`.  

2. **🧹 Data Cleaning**  
   - Handle missing values.  
   - Remove duplicates.  
   - Standardize scales (e.g., `StandardScaler`).  

3. **📊 Exploratory Data Analysis (EDA)**  
   - **Correlation heatmaps** (to detect relationships).  
   - **Distribution plots** (to check skewness).  
   - **Elbow method** (to find optimal clusters).  

4. **🛠️ Data Preprocessing**  
   - Normalize features.  
   - Apply **PCA** for dimensionality reduction.  

5. **🤖 Model Training (K-Means Clustering)**  
   - Train with optimal `K` (from elbow plot).  
   - Evaluate using **Silhouette Score** (`0.194`).  

6. **📊 MLflow Integration**  
   - Log experiments (hyperparameters, metrics).  
   - Compare different clustering runs.  

7. **🚀 Streamlit Deployment**  
   - Interactive dashboard to:  
     - **Visualize clusters**.  
     - **Predict segments** for new customers.  

---

## **📈 Key Results**  
- **Optimal Clusters (K):** `4` (from elbow method).  
- **Silhouette Score:** `0.194` (higher = better separation).  
- **Sample Clusters:**  
  | Cluster | Profile |  
  |---------|-------------------------------|  
  | **0**   | Moderate income, average spenders |  
  | **1**   | High income, high spenders |  
  | **2**   | Low income, low spenders |  
  | **3**   | Young professionals (high spend, low savings) |  

*(See [Simple Explanation](#) for more details.)*  

---

## **👥 Stakeholders**  
- **Marketing Teams:** Better ad targeting.  
- **Sales Teams:** Personalized upsell strategies.  
- **Business Analysts:** Data-driven decision-making.  

---

## **🚀 How to Run**  
1. Clone repo:  
   ```bash
   git clone https://github.com/yourusername/Customer_Segmentation.git
   ```
2. Install dependencies:  
   ```bash
   pip install -r requirements.txt
   ```
3. Run EDA:  
   ```bash
   python EDA.py
   ```
4. Train model:  
   ```bash
   python train_model.py
   ```
5. Launch Streamlit app:  
   ```bash
   streamlit run app.py
   ```


# Problem Statement
## Objective: 
Use K-Means clustering to segment customers into distinct groups based on annual_income (USD), spending_score (0-100 scale), savings (USD), and age (years). The model will help a retail company tailor marketing strategies for different customer segments (e.g., high-income spenders, conservative savers).

## Business Context: 
Understanding customer segments enables personalized marketing, product recommendations, and loyalty programs. The project includes automated data preprocessing, experiment tracking with MLflow, and a Streamlit app for visualizing customer segments and predicting segment membership for new customers.

## Success Criteria: 
Identify meaningful clusters (e.g., 3-5 clusters based on the elbow method), achieve low inertia (indicating tight clusters), track experiments with MLflow, and deploy a user-friendly Streamlit interface for segment prediction and visualization.
