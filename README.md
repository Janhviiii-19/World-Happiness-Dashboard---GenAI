# World Happiness Dashboard

Interactive Plotly dashboard analyzing the 2016 World Happiness Report. Explores how GDP per capita, health, family, freedom, trust, and generosity relate to happiness scores across world regions — visualized through a correlation heatmap, regional scatter plot, pie chart, and an interactive choropleth map.

## Overview

The World Happiness Report ranks countries by self-reported well-being and breaks down the score into contributing factors such as economic output, social support, health, freedom, trust in government, and generosity. This project cleans the 2016 dataset, examines the relationships between those factors, and packages the findings into a single interactive HTML dashboard.

## Tools Used
Here's the full toolset used across this project:

## Python Libraries

| Tool | Purpose |
|---|---|
| **pandas** | Reading the CSV, cleaning data (whitespace stripping, NaN handling, dtype conversion, mean imputation), aggregating (`groupby`) for the pie chart |
| **numpy** | Numeric type checks and NaN handling during cleaning |
| **plotly.express** | High-level chart creation — scatter plot (fig3), pie chart (fig4), choropleth map (fig5), correlation heatmap (fig2 via `px.imshow`) |
| **plotly.graph_objects** | Lower-level bar chart construction (fig1) |
| **plotly.io** | Exporting figures to HTML and combining them into the final `dashboard.html` |

## Environment / Platform

- **Google Colab** — where you're running the notebook (based on the `/content/drive/MyDrive/...` file path and `google.colab.files.download()` usage)
- **Google Drive** — source of the `2016.csv` dataset
- 
## Data Source

- **Kaggle** — origin of the `2016.csv` World Happiness Report dataset

---

If you meant something different by "tools" — like tools *I* (Claude) used in this chat to help you — I used code generation and file creation (for the `README.md`), but no external searches or data lookups, since everything was based on the code and analysis we built together in the conversation. Let me know which you were asking about if I read it wrong.

## Dashboard Contents

| Chart | Description |
|---|---|
| **Correlation Heatmap** | Correlation between Happiness Score and six contributing factors (GDP, Family, Health, Freedom, Trust, Generosity) |
| **Regional Scatter Plot** | GDP per Capita vs. Happiness Score, colored by Region, to explore whether wealth predicts well-being |
| **Regional Pie Chart** | Average Happiness Score distribution across world regions |
| **Choropleth Map** | GDP per Capita by country, with Healthy Life Expectancy shown on hover |

## Tech Stack

- **Python 3**
- **Pandas** — data loading, cleaning, and aggregation
- **Plotly** (Express & Graph Objects) — interactive visualizations
- **Jupyter / Google Colab** — development environment

## Project Structure

```
world-happiness-dashboard/
├── happiness_dashboard.py     # Main analysis + chart-generation script
├── dashboard.html             # Combined interactive dashboard (output)
├── README.md
├── requirements.txt
└── .gitignore
```

## Data Cleaning Steps

- Loaded the CSV with headers, verified column data types
- Stripped leading/trailing whitespace from string columns
- Replaced empty strings with `NaN`
- Converted columns to appropriate dtypes
- Imputed missing numeric values using column means

## Key Insights

- **GDP per Capita, Family, and Health (Life Expectancy)** show the strongest positive correlation with Happiness Score.
- Wealthier regions (Western Europe, North America, Australia/New Zealand) consistently report higher happiness, but **the relationship isn't purely economic** — some lower-GDP regions outperform their income level on happiness.
- Happiness is **unevenly distributed geographically**, with a persistent gap between the highest- and lowest-scoring regions.
