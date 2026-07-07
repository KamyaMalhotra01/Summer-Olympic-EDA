# Summer Olympic Data — Exploratory Data Analysis

A Jupyter notebook that performs exploratory data analysis (EDA) on historical Summer Olympics results, covering data quality checks, univariate analysis, and bivariate/multivariate trend analysis.

## 📁 Dataset
The dataset, summer.csv, is included in this repository. It contains Summer Olympics medal records with the following columns (based on the analysis performed):

- `Year` — Year the Olympics took place
- `City` — Host city
- `Sport` — Sport category
- `Athlete` — Athlete name
- `Country` — Country represented
- `Gender` — Athlete gender
- Additional columns for event/discipline and medal details

**Note:** you'll need to supply your own `summer.csv` (e.g. from the [Kaggle "120 years of Olympic history" / Summer Olympics dataset](https://www.kaggle.com/datasets)) — it is not included in this repo.

## 🛠 Requirements

```bash
pip install pandas matplotlib seaborn
```

Tested in a Jupyter Notebook / JupyterLab environment.

## 📊 What the notebook does

### 1. Setup
- Imports `pandas` for data handling and, later, `matplotlib`/`seaborn` for visualization.
- Loads the dataset with `pd.read_csv('summer.csv')`.

### 2. Understanding the Data (basic questions)
- **Shape** — size of the dataset (rows × columns)
- **Sample rows** — a quick look at random records
- **Data types** — column dtypes via `df.info()`
- **Missing values** — checks for nulls via `df.isna().sum()`
- **Summary statistics** — `df.describe()`
- **Duplicates** — detects and inspects duplicate rows (and drops them)
- **Correlation** — correlation matrix between numeric columns

### 3. Univariate Analysis (single-variable visualizations)
- Bar chart of the **top 10 countries** by medal count
- Count plot of **medals by gender**
- Pie chart of the **top 10 countries'** share of medals
- Pie chart of **medal proportion by gender**

### 4. Bivariate / Multivariate Analysis (trends over time)
- **Countries per Olympics** — line plot showing growth in participating countries over the years
- **Athlete participation over time** — histogram + line plot showing distribution and trend of athlete counts per Games
- **Sports/events over time** — histogram + line plot showing how the number of sports/events grew across Olympic Games
- **Host cities** — bar chart of which cities have hosted the Summer Olympics most often

## 📈 Key Observations Documented in the Notebook

- The dataset contains **31,165 rows and 9 columns**.
- **4 records** have missing country values.
- **2 duplicate rows** were found in the data.
- Country participation in the Summer Olympics has **increased over the years**.

## 🚀 Usage

1. Place `summer.csv` in the same directory as the notebook.
2. Open `Summer_Olympic_Data_EDA.ipynb` in Jupyter Notebook/Lab.
3. Run all cells sequentially (`Kernel → Restart & Run All`).
