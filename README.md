# World Happiness Dashboard

Interactive Plotly dashboard analyzing the 2016 World Happiness Report. Explores how GDP per capita, health, family, freedom, trust, and generosity relate to happiness scores across world regions — visualized through a correlation heatmap, regional scatter plot, pie chart, and an interactive choropleth map.

## Overview

The World Happiness Report ranks countries by self-reported well-being and breaks down the score into contributing factors such as economic output, social support, health, freedom, trust in government, and generosity. This project cleans the 2016 dataset, examines the relationships between those factors, and packages the findings into a single interactive HTML dashboard.

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
