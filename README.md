# 🚀 Space Launch Cost Analysis

**By Karen Cardiel**

## 📊 Overview

This project analyzes the cost of space launches to low Earth orbit, examining trends in launch costs, frequency, and the relationship between rocket class and pricing over time.

## 📈 The Data

### Dataset Source
The dataset was obtained from [Our World in Data](https://ourworldindata.org/) by downloading the full data (CSV format). The data contains information about the initial flight of various rockets and their cost efficiency for carrying payloads to space.

### Variables Description
| Variable | Description |
|----------|-------------|
| `Entity` | The model/name of the rocket |
| `Year` | The year of the rocket's first launch |
| `cost_per_kg` | The cost in USD to carry one kilogram to space |
| `launch_class` | Classification of the rocket as Heavy, Medium, or Small |

## 🛠️ Setup and Dependencies

```python
import seaborn as sns
import pandas as pd
import matplotlib.pyplot as plt
from google.colab import drive
```

### 📂 Data Loading
The analysis uses Google Colab with Google Drive integration to access the dataset:

```python
drive.mount("/content/drive/")
launches = pd.read_csv("/content/drive/MyDrive/datasets/cost-space-launches-low-earth-orbit.csv")
```

## 📋 Data Sample
| Entity | Year | cost_per_kg | launch_class |
|---------|------|-------------|--------------|
| Angara | 2014 | 4,500 | Heavy |
| Antares | 2013 | 13,600 | Medium |
| Ariane 44 | 1988 | 18,300 | Medium |
| Ariane 5G | 1997 | 10,200 | Heavy |
| Athena 1 | 1997 | 19,200 | Small |

## 📊 Visualizations

### 1. 📊 Histogram Charts

#### 🗓️ First Successful Launches by Year
- **Purpose**: Shows the distribution of first successful rocket launches over time
- **Color**: `#7C00FE` (Purple)
- **Insights**: Reveals trends in space technology development and market entry

#### 🏷️ Launch Distribution by Class
- **Purpose**: Displays the count of rockets in each payload class category
- **Color**: `#009FBD` (Blue)
- **Categories**: Heavy, Medium, Small rockets

#### 💰 Cost Distribution
- **Purpose**: Shows the frequency distribution of launch costs per kilogram
- **Color**: `#FF6969` (Red)
- **Insights**: Reveals the range and common pricing points in the industry

### 2. 🎯 Scatter Plot Analysis

#### 📈 Cost vs. Year by Launch Class
- **Purpose**: Examines the relationship between launch year, cost efficiency, and rocket class
- **Colors**: 
  - 🟣 `#7C00FE` (Purple)
  - 🟡 `#E90074` (Pink)
  - 🔵 `#009FBD` (Blue)
- **Features**: Grid overlay for better readability
- **Insights**: Shows how launch costs have evolved over time and varies by rocket class

## ❓ Key Analysis Questions

This visualization suite helps answer:
1. ⏰ How has the frequency of new rocket development changed over time?
2. 📊 What is the distribution of rocket classes in the market?
3. 💸 How do launch costs vary across the industry?
4. 📉 Is there a relationship between launch year and cost efficiency?
5. ⚖️ How do different rocket classes compare in terms of cost per kilogram?

## Technical Notes

- All charts include grid overlays for improved readability
- Spanish labels are used for titles and axis labels
- Consistent color scheme across related visualizations
- Alpha transparency (0.6) used for better visual appeal

## File Structure
```
project/
├── cost-space-launches-low-earth-orbit.csv
├── analysis.ipynb
└── README.md
```

## Future Enhancements

Potential areas for expansion:
- Time series analysis of cost trends
- Statistical correlation analysis
- Comparison with inflation-adjusted costs
- Success rate analysis by rocket class
- Geographic analysis by country/company
