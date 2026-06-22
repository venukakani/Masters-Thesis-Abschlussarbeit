# 🚢 Data-Driven Decision Support System for Predicting Ferry Ship Emissions

> **Master's Thesis** | Universität Duisburg-Essen | MSc Technische Logistik | 2024  
> **Author:** Venu Kakani

---

## 📌 Project Overview

This project develops a **Data-Driven Decision Support System (DSS)** to predict and visualize greenhouse gas emissions from the **Hammershus ferry ship** (Bornholm–Sjaelland route, Denmark) using real-world AIS data from 2021.

The system combines **Python-based physics modelling** with an **interactive Power BI dashboard**, enabling ferry operators to monitor emissions in real time and make data-driven decisions to reduce environmental impact.

**Key Result: A 10% speed reduction led to a 27% drop in fuel consumption and emissions (CO₂, NOₓ, SOₓ, PM).**

---

## 🎯 Objectives

- Predict ferry ship resistance and fuel consumption using the **Holtrop-Mennen method**
- Estimate emissions (CO₂, NOₓ, SOₓ, PM) from real AIS operational data
- Build an interactive **Power BI dashboard** as the DSS user interface
- Identify optimization strategies to reduce maritime emissions

---

## 🛠️ Tech Stack

| Tool | Purpose |
|------|---------|
| **Python** | Holtrop-Mennen resistance & emissions calculations |
| **Power BI** | Interactive dashboard & data visualization |
| **Pandas / NumPy** | Data processing and transformation |
| **Power Query (M)** | ETL pipeline within Power BI |
| **DAX** | KPI measures and calculated columns |
| **AIS Data (CSV)** | Real-world ship voyage data (Danish Maritime Authority) |

---

## 🔬 Methodology

### 1. Data Acquisition
- Historical AIS data for the Hammershus ferry (2021) sourced from the **Danish Maritime Authority**
- Key parameters: Speed Over Ground (SOG), heading, current speed/direction, latitude, longitude

### 2. Resistance & Power Prediction (Python)
- Implemented the **Holtrop-Mennen empirical method** in Python
- Calculated: frictional resistance, wave-making resistance, appendage resistance, brake power, propulsive efficiency
- Python script integrated directly into **Power BI Desktop** as a data source

### 3. Emissions Estimation
Using IMO-compliant emission factors for MDO (Marine Diesel Oil):

| Emission | Factor |
|----------|--------|
| CO₂ | 3.206 g/g |
| NOₓ | 2.6 g/g (Tier 3, MSD) |
| SOₓ | 0.0011027 g/g |
| PM | 0.18 g/g |

### 4. Power BI Dashboard
- 8-page interactive dashboard covering fuel consumption, CO₂, NOₓ, SOₓ, PM, route mapping
- Haversine formula used for trip distance & journey frequency calculation
- Optimization scenario: speed reduction impact analysis

---

## 📊 Key Results

| Metric | Value |
|--------|-------|
| Total Fuel Consumption (2021) | 1.37M tonnes/kWh |
| Total CO₂ Emissions | 4.40M tonnes |
| Total NOₓ Emissions | 3.57M tonnes |
| Total SOₓ Emissions | 1.51K tonnes |
| Total PM Emissions | 247.16K tonnes |
| **CO₂ Reduction (10% speed cut)** | **~27%** |

---

## 🗂️ Repository Structure

```
📁 data/               # Sample/anonymized AIS input data (CSV)
📁 python/             # Holtrop-Mennen Python script
📁 dashboard/          # Power BI screenshots & PDF export
📁 docs/               # Thesis summary & methodology notes
README.md
```

---

## 🚀 How to Run

1. **Clone the repo**
```bash
git clone https://github.com/venukakani/ferry-emissions-dss.git
```

2. **Install Python dependencies**
```bash
pip install pandas numpy openpyxl math
```

3. **Run the emissions calculation script**
```bash
python python/holtrop_mennen_emissions.py
```

4. **Open Power BI dashboard**
   - Open `dashboard/Ferry_Emissions_Dashboard.pbix` in Power BI Desktop
   - Connect to the AIS data source
   - Refresh to load emissions calculations

---

## 📈 Dashboard Preview

> *Screenshots of the Power BI dashboard pages — Fuel Consumption, CO₂, NOₓ, SOₓ, PM, Route Mapping*

*(Add screenshots here)*

---

## 🌍 Real-World Impact

This DSS supports the **EU MRV Regulation (2015/757)** and **IMO GHG Strategy** goals by enabling:
- Real-time emissions monitoring for ferry operators
- Evidence-based speed optimization decisions
- Transparent reporting for regulatory compliance
- A replicable framework for any vessel with AIS data

---

## 📚 References

- Holtrop & Mennen (1982) — *An Approximate Power Prediction Method*
- IMO Fourth GHG Study (2020)
- Danish Maritime Authority — AIS Data
- van den Berg (2022) — *Estimate Vessel Emissions Using AIS Data*, TU Delft

---

## 📬 Contact

**Venu Kakani**  
MSc Technische Logistik | Universität Duisburg-Essen  
📧 venukakani06@gmail.com  
🔗 [LinkedIn](https://linkedin.com/in/venukakani)

---

*This project was submitted as a Master's thesis on 05.07.2024.*
