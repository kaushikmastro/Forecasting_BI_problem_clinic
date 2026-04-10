# Forecasting Clinic Revenues and Patients (BI Problem)

This repository contains an analysis and forecasting project aimed at estimating future clinic revenues, appointments, and unique patients for the year 2023. The predictions are built on historical data from 2022, while also factoring in business expansion plans (the opening of new clinics).

## 📊 Project Overview

The main objective of this challenge is to analyze historical clinic data and project future performance. Specifically, the analysis answers:
- How much revenue can we expect in 2023?
- How many unique patients will we have acquired by the end of 2023?

The forecasting model takes into account the current growth rate of existing clinics and adjusts the estimations based on planned expansions (e.g., adding a new clinic in March and another in July).

## 📂 Repository Structure

- **`Forecasting_revenues_unique_patients.ipynb`**: The main Jupyter Notebook containing the entire data pipeline, from loading and cleaning the data to exploratory data analysis (EDA) and final forecasting.
- **`p21_bi_intern_test_appointments.csv`**: Historical dataset containing details about clinic appointments (e.g., appointment dates, patient IDs, clinic IDs, practitioner IDs).
- **`p21_bi_intern_test_revenues.csv`**: Historical dataset containing the revenues associated with specific appointments.

## ⚙️ Methodology

1. **Data Preprocessing**: 
   - Merged the appointments and revenues datasets using an inner join on `appointment_id`.
   - Handled missing data by imputing missing revenue values with the mean revenue.
   - Converted date strings into proper datetime objects to extract month and year features.
2. **Exploratory Data Analysis (EDA)**:
   - Grouped data to calculate monthly statistics for 2022 (appointment counts, total revenues, and unique patient counts).
   - Visualized historical trends using line plots to understand the baseline growth.
3. **Forecasting (2023)**:
   - Calculated the mean monthly growth rate based on 2022 data.
   - Forecasted 2023 figures by applying the historical growth rate while applying scaling multipliers to account for the opening of two new clinics in March and July.

## 🛠️ Technologies Used

- **Python 3**
- **Pandas** (Data manipulation and merging)
- **NumPy** (Numerical operations)
- **Matplotlib** (Data visualization)
- **Jupyter Notebook** (Interactive analysis environment)

## 🚀 How to Run

1. Clone this repository to your local machine:
   ```bash
   git clone https://github.com/kaushikmastro/Forecasting_BI_problem_clinic.git
   ```
2. Navigate to the project directory:
   ```bash
   cd Forecasting_BI_problem_clinic
   ```
3. Ensure you have the required Python libraries installed:
   ```bash
   pip install pandas numpy matplotlib jupyter
   ```
4. Start the Jupyter Notebook server:
   ```bash
   jupyter notebook
   ```
5. Open `Forecasting_revenues_unique_patients.ipynb` and run the cells sequentially to view the analysis and forecasts.
