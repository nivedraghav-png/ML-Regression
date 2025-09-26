# ML-Data_Preprocessing
Data Pre Processing for Machine Learning 
📌 Objective
The goal of this project is to design and implement a robust data preprocessing pipeline that improves the quality, reliability, and usefulness of raw data for machine learning applications.

⚙️ Key Steps
1. Data Exploration
        Explored dataset structure and unique values per column
        Performed statistical analysis
        Renamed columns for clarity
2. Data Cleaning
        Treated missing values and inappropriate entries
        Replaced Age = 0 with NaN and imputed missing values
        Removed duplicate rows
        Detected outliers using IQR method
3. Data Analysis
        Filtered dataset (Age > 40, Salary < 5000) and visualized Age vs Salary
        Counted people by Place and represented results visually
4. Data Encoding
        Converted categorical features into numerical values using:
           Label Encoding
           One-Hot Encoding
5. Feature Scaling
       Applied StandardScaler (mean = 0, std = 1)
       Applied MinMaxScaler (scaled to 0–1 range)


🛠️ Tools & Libraries
       Python 3
       Pandas, NumPy → Data Handling
       Matplotlib, Seaborn → Visualization
       Scikit-learn → Encoding & Scaling
