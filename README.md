≈# DataScienceBlogPost

# Developer Salaries & Experience: What Actually Drives a Tech Career?

## 📰 Read the Blog Post

👉 [What 65,000 Developers Taught Me About Salary, Experience, and Happiness](https://medium.com/@abduallah.s2004/what-65-000-developers-taught-me-about-salary-experience-and-happiness-9e1e43308fe9)

A non-technical summary of the findings, written for anyone curious about developer careers.

## 💡 Motivation

As someone learning data science, I wanted to answer questions I personally wonder 
about as a future developer: *Does experience really lead to higher pay? Does a 
degree matter? Are experienced developers actually happier?*

This project analyzes the **2024 Stack Overflow Developer Survey** (65,000+ 
responses from developers worldwide) to explore four business questions:

1. Does education level affect salary?
2. Does education level affect years of experience?
3. Does experience affect job satisfaction?
4. Does experience affect salary?

I picked the Stack Overflow survey because it's **relatable and realistic** — the 
data is about developers like me, and the findings speak directly to anyone 
planning a tech career: students, junior developers, career changers, and 
experienced engineers wondering what actually drives success in this field.

## 📚 Libraries Used

This project was built in Python using:
- **pandas** — loading CSVs, cleaning data, and creating DataFrames
- **numpy** — numerical operations
- **matplotlib** — scatter plots and boxplots
- **seaborn** — statistical visualization built on matplotlib
- **scikit-learn** — machine learning:
  - `LinearRegression` for modeling
  - `mean_squared_error`, `root_mean_squared_error`, `r2_score` for evaluation

## 📂 Files in the Repository

| File | Description |
|------|-------------|
| `analysis.ipynb` | Main Jupyter notebook containing all data cleaning, exploration, modeling, and visualization |
| `README.md` | This file — project overview, motivation, and results summary |
| `stack-overflow-developer-survey-2024/` | Folder containing the dataset (download separately — see below) |

### 📥 Getting the Data

The dataset is **not included** in this repository due to its size. To run the notebook:

1. Download the 2024 Stack Overflow Developer Survey from [survey.stackoverflow.co](https://survey.stackoverflow.co/)
2. Extract the ZIP and place the folder `stack-overflow-developer-survey-2024/` in the project root
3. The notebook will read `survey_results_public.csv` from that folder

## 📊 Summary of Results

After cleaning the dataset (65,437 → ~20,000 usable rows), I ran a linear 
regression for each question and evaluated it with R² and RMSE.

| Question | R² | Finding |
|----------|-----|---------|
| **Q1** — Does education affect salary? | 0.005 | Almost no linear effect, but boxplots reveal a *ceiling effect* — higher education increases the chance of reaching top salaries ($300K+) without raising the typical salary. |
| **Q2** — Does education affect experience? | 0.0008 | Zero effect. Developers at every education level span the full experience range. Experience depends on *age and when you started coding*, not on school. |
| **Q3** — Does experience affect job satisfaction? | 0.008 | Almost no effect. Developers at every experience level report the full range of satisfaction (0–10). Happiness is driven by other factors. |
| **Q4** — Does experience affect salary? | 0.111 | The strongest predictor found, but still weak. On average, predictions are off by ~$63,000 — roughly a median salary ~$65,000. |

### 🎯 Key Takeaway

**Developer careers are complicated.** Neither experience nor education alone 
reliably predicts salary, happiness, or each other. The factors that *really* 
drive outcomes are likely things not captured in the survey — the specific 
company, country, negotiation skills, network, and luck. Experience is the 
best single predictor of salary found in this analysis, but it still explains 
only ~11% of the variation.

The real story isn't *"do this one thing to succeed"* — it's *"success 
depends on many things working together."*
