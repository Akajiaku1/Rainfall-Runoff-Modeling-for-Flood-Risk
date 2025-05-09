# 🌧️ Rainfall-Runoff Modeling for Flood Risk

This project implements a basic **Rainfall-Runoff Modeling** framework using the **SCS Curve Number (CN) Method** to assess flood risk based on daily rainfall data. It visualizes runoff and flags flood-prone events using a threshold-based system.

---

## 🧰 Features

- Estimates runoff from daily rainfall using the **SCS Curve Number method**
- Flags days with **high flood risk** based on runoff threshold
- Generates a clear **time series plot** of rainfall and runoff
- Outputs a tabular dataset with **runoff depth and flood risk status**

---

## 📈 Methodology

The **SCS Curve Number (CN)** method is used to calculate surface runoff:

1. **Potential Maximum Retention (S):**

   \[
   S = \frac{25400}{CN} - 254
   \]

2. **Initial Abstraction (Ia):**

   \[
   Ia = 0.2 \cdot S
   \]

3. **Runoff (Q):**

   \[
   Q = \frac{(P - Ia)^2}{(P - Ia + S)} \quad \text{for } P > Ia, \text{ else } Q = 0
   \]

Where:
- \( P \) = Rainfall in mm
- \( CN \) = Curve Number (based on land use, soil, slope)
- \( Q \) = Runoff in mm

---

## 📦 Dependencies

Install the required Python packages:

```bash
pip install pandas numpy matplotlib

🚀 How to Use

    Clone the repository:

git clone https://github.com/yourusername/rainfall-runoff-flood-risk.git
cd rainfall-runoff-flood-risk

    Run the script:

python rainfall_runoff_model.py

    View:

        A plot of rainfall vs runoff with a flood risk threshold

        A table showing dates, rainfall, runoff, and flood risk level

📊 Output Sample
Date	Rainfall_mm	Runoff_mm	Flood_Risk
2023-09-01	5	0.00	Low
2023-09-04	80	43.55	High
🔬 Future Work

    Integrate with GIS shapefiles and DEM data

    Use real-time weather API for rainfall input

    Incorporate machine learning for predictive flood modeling

    Extend for HEC-HMS or SWAT integration

📜 License

This project is licensed under the MIT License.
👨‍💻 Author

Ugochukwu Charles A. 
Data Scientist | Flood Risk Analyst
