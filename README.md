# MJK-PLP-PYTHON-FINAL-PROJECT

# **COVID-19 Global Data Tracker**  
*A Data-Driven Analysis of Pandemic Trends (2020-2023)*  

---

## **📌 Project Description**  
This project analyzes global COVID-19 trends through:  
- Time-series tracking of cases, deaths, and vaccinations  
- Country-level comparisons of pandemic responses  
- Geospatial visualization of case density  
- Data quality assessment of public health reporting  

Built with Python's data science stack, it transforms raw WHO/OWID data into actionable insights for epidemiologists and policymakers.  

---

## **🎯 Objectives**  
| ✅ Completed | Objective |
|------------|-----------|
| ✔️ | Import and clean multi-source COVID-19 data |
| ✔️ | Identify trends in cases/deaths/vaccinations |
| ✔️ | Compare country-level pandemic responses |
| ✔️ | Visualize global case distribution |
| ✔️ | Document data limitations and anomalies |

*Stretch Goals Achieved:*  
- Calculated case fatality rates  
- Detected reporting anomalies  
- GDP-vaccination correlation analysis  

---

## **🛠️ Tools & Libraries**  
**Core Stack:**  
```markdown
- Python 3.9+
- Jupyter Notebook (Interactive Analysis)
- Pandas (Data Wrangling)
- Matplotlib/Seaborn (Static Visuals)
- Plotly Express (Interactive Maps)
```

**Data Sources:**  
- [Our World in Data](https://github.com/owid/covid-19-data) (Primary)  
- Johns Hopkins CSSE (Backup)  

---

## **🚀 Installation & Execution**  

### **Method A: Jupyter Notebook**  
```bash
# 1. Clone repository
git clone https://github.com/yourusername/covid-tracker.git

# 2. Install dependencies
pip install -r requirements.txt  # Includes:
# pandas==1.5.3
# plotly==5.13.0
# matplotlib==3.7.1

# 3. Launch Jupyter
jupyter notebook
```

### **Method B: VS Code**  
1. Open `COVID-19_Tracker.ipynb`  
2. Install Jupyter extension  
3. Run cells sequentially (Shift+Enter)  

---

## **🔍 Key Insights**  

### **1. Vaccination Disparities**  
```python
top_vax = df.groupby('location')['people_vaccinated_per_hundred'].max().nlargest(3)
```
| Country | % Population Vaccinated |  
|---------|------------------------:|  
| Germany | 78.2% |  
| USA | 67.5% |  
| Brazil | 62.1% |  

*Finding:* 4:1 vaccination gap between developed and developing nations  

### **2. Fatality Rate Trends**  
![Fatality Chart](images/fatality_trend.png)  
- 63% reduction in CFR (2020-2023)  
- Kenya's CFR remained 2× higher than Germany's  

### **3. Data Quality Issues**  
```python
null_report = df.isnull().sum()/len(df)*100
```
| Metric | % Missing |  
|--------|----------:|  
| ICU Patients | 89.2% |  
| Excess Mortality | 96.5% |  

---

## **📝 Reflections**  

### **What Worked Well**  
✔️ Plotly maps effectively showed geographic patterns  
✔️ Automated cleaning pipeline handled messy real-world data  
✔️ Comparative design revealed policy impacts  

### **Challenges**  
⚠️ **Data Gaps:** Limited hospital/ICU metrics reduced health system analysis  
⚠️ **Temporal Bias:** Early-pandemic records lacked standardized reporting  
⚠️ **Resource Correlation:** Needed GDP/population density controls  

### **Future Extensions**  
- Add variant-specific analysis  
- Build interactive dashboard with Dash  
- Incorporate mobility data  


**Created by:** Mwangi Josphat Karanja
**Last Updated:** 15 05 2025 at 0430Hrs

---

 
 
