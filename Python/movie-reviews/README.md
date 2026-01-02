# Maven Rotten Tomatoes Movie Reviews — Data Analysis with Seaborn

This project explores the **Maven Rotten Tomatoes Movie Reviews** dataset to uncover insights about movie ratings, genres, and review patterns using Python and Seaborn for visualization.

---

## 🎯 Project Objectives
- Perform **exploratory data analysis (EDA)** on Rotten Tomatoes movie reviews.
- Visualize trends in **critic vs audience scores**, **genre distributions**, and **review counts**.
- Practice **data cleaning, aggregation, and visualization** using:
  - pandas
  - seaborn
  - matplotlib

---

## 📂 Repository Structure
```
.
├── README.md
├── requirements.txt
├── data/
│   └── rotten_tomatoes.csv   # Maven dataset
├── notebooks/
│   └── 01_eda_visualizations.ipynb
└── src/
    └── analysis.py
```

---

## 🛠️ Setup Instructions
1. Clone the repository:
   ```bash
git clone <your-repo-url>
cd <repo-folder>
```
2. Create and activate a virtual environment:
   ```bash
python -m venv .venv
source .venv/bin/activate   # Windows: .venv\Scripts\activate
```
3. Install dependencies:
   ```bash
pip install -r requirements.txt
```

Example `requirements.txt`:
```txt
pandas
numpy
matplotlib
seaborn
jupyter
```

---

## 🚀 How to Run
- Place the Maven Rotten Tomatoes dataset in `data/rotten_tomatoes.csv`.
- Launch Jupyter Notebook:
   ```bash
jupyter notebook notebooks/01_eda_visualizations.ipynb
```
- Explore visualizations like:
  - Distribution of **critic vs audience scores**
  - **Genre popularity** and average ratings
  - Correlation heatmaps for numeric features

---

## 📊 Example Visualizations
- **Histogram** of critic scores
- **Boxplot** comparing critic and audience ratings by genre
- **Heatmap** of correlations between numeric features

---

## ✅ Next Steps
- Add sentiment analysis on review text.
- Build predictive models for audience score.
- Create interactive dashboards using Plotly or Streamlit.

---

## 📬 Acknowledgments
- **Maven Analytics** for providing the dataset.
- Python libraries: pandas, seaborn, matplotlib.

---

License: MIT
