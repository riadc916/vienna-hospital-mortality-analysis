# Dr. Semmelweis & The Discovery of Handwashing

Statistical and time-series data analysis of Dr. Ignaz Semmelweis's 1840s Vienna General Hospital maternity clinic records (`annual_deaths_by_clinic.csv` & `monthly_deaths.csv`), investigating the impact of handwashing on maternal mortality rates.

---

## Project Overview

In the mid-19th century, childbed (puerperal) fever was a major cause of maternal mortality in maternity wards[cite: 23]. Working at the Vienna General Hospital[cite: 23], Hungarian physician **Dr. Ignaz Semmelweis** suspected that physicians and medical students were transmitting infectious particles from autopsy rooms to expectant mothers[cite: 23].

This project recreates Dr. Semmelweis's historical investigation using Python[cite: 23, 37]. Through exploratory data analysis (EDA), time-series visualization, moving-average smoothing, and statistical hypothesis testing[cite: 29, 34, 37], the notebook evaluates how introducing mandatory handwashing with chlorinated lime in **June 1847** dramatically reduced maternal death rates.

---

## Datasets Used

* **`annual_deaths_by_clinic.csv`**: Yearly counts of births and maternal deaths across Clinic 1 (staffed by doctors and medical students) and Clinic 2 (staffed by midwives) from 1841 to 1846[cite: 23, 26, 27].
* **`monthly_deaths.csv`**: Monthly birth and death records in Clinic 1 before and after the introduction of mandatory handwashing[cite: 23, 24, 29].

---

## Key Analytical Steps & Visualizations

All generated charts and visual outputs are stored in the `Results*` directory[cite: 37]:

1. **Data Exploration & Cleaning:** Handled missing values, converted date strings into `datetime` objects, and engineered mortality proportion features (`pct_deaths`)[cite: 28, 30].
2. **Clinic Comparison (1841–1846):** Visualized yearly births, deaths, and mortality rates using Plotly line charts, revealing that Clinic 1 consistently experienced significantly higher mortality rates than Clinic 2[cite: 26, 27, 28].
3. **Time-Series & Moving Average Analysis:** Plotted monthly birth and death trends alongside a **6-month rolling average** to highlight the sharp, sustained drop in mortality immediately following June 1847[cite: 24, 25, 29].
4. **Distribution & Boxplot Comparisons:** Compared pre- and post-handwashing death rate distributions using boxplots, histograms, and Kernel Density Estimation (KDE) plots[cite: 30, 31, 32, 33].
5. **Statistical Hypothesis Testing:** Performed a two-sample independent **t-test** to verify whether the observed drop in mortality was statistically significant[cite: 34].

---

## Key Findings

* **Drastic Drop in Mortality Rate:** Following the June 1847 handwashing mandate, the average monthly maternal death rate fell from **~10.5%** to **~2.1%**.
* **Statistical Significance:** The two-sample t-test produced a **t-statistic of 5.512** and a **p-value of 0.0000002985** ($p < 0.01$)[cite: 34], confirming with overwhelming statistical certainty that handwashing directly caused the reduction in deaths.

---

## Tools & Libraries

* **Language:** Python 3[cite: 23, 37]
* **Data Manipulation:** `Pandas`, `NumPy`
* **Visualization:** `Matplotlib`, `Seaborn`, `Plotly Express`[cite: 37]
* **Statistical Analysis:** `SciPy (scipy.stats)`[cite: 34]
