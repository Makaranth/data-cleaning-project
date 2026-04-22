# 📊 Student Performance Analysis

A Python-based data analysis project that explores student academic performance across **Math**, **Science**, and **English**, alongside attendance records — from raw data to visual insights.

---

## 📁 Project Structure

```
├── Student_data.csv       # Raw input data
├── cleaned_data.csv       # Processed data (imputed values + averages)
├── project_code.py        # Main analysis & visualization script
├── app.py                 # Application entry point
├── bar_chart.png          # Average marks bar chart
├── Line_Chart.jpeg        # Marks trend line chart
└── Heatmap.jpeg           # Correlation heatmap
```

---

## 🔄 Pipeline

```
Raw Data → Cleaning → Analysis → Visualization
```

1. **Load** — Read `Student_data.csv` into a DataFrame
2. **Clean** — Impute missing values, compute per-student averages
3. **Analyze** — Correlation matrix + descriptive statistics
4. **Visualize** — Generate bar chart, line chart, and heatmap

---

## 📈 Visualizations

### Average Marks (Bar Chart)
Compares class-wide averages across subjects.
> English leads (~85), followed by Math (~81) and Science (~80).

### Marks Trend (Line Chart)
Tracks individual student scores across all three subjects, highlighting performance consistency vs. variance.

### Correlation Heatmap
Pearson correlation between all numeric features (Math, Science, English, Attendance, Average).

| Feature Pair         | Correlation |
|----------------------|-------------|
| Math ↔ Average       | 0.98        |
| English ↔ Average    | 0.98        |
| Science ↔ Attendance | 0.96        |
| Attendance ↔ English | 0.94        |
| Math ↔ Attendance    | 0.93        |

---

## 🔍 Key Findings

- ✅ All subjects are **strongly correlated** with each other (r > 0.90)
- 📅 **Attendance** is a significant predictor of performance across all subjects
- 🏆 **English** has the highest class average among the three subjects
- 📊 **Average score** shows the strongest overall correlation with individual subjects

---

## 🛠️ Tech Stack

| Tool | Purpose |
|------|---------|
| `pandas` | Data loading & cleaning |
| `numpy` | Numerical computations |
| `matplotlib` | Bar chart & line chart |
| `seaborn` | Correlation heatmap |

---

## 🚀 Getting Started

```bash
# Install dependencies
pip install pandas numpy matplotlib seaborn

# Run the analysis
python project_code.py

# Or launch the app
python app.py
```

---

## 📄 Data Description

| Column     | Description                        |
|------------|------------------------------------|
| Name       | Student identifier                 |
| Math       | Math score (out of 100)            |
| Science    | Science score (out of 100)         |
| English    | English score (out of 100)         |
| Attendance | Attendance percentage              |
| Average    | Mean of Math, Science, and English |
