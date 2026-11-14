<div align="center">

# 🌍 Global Terrorism Data Visualization & Analysis

### Exploring Global Terrorism Patterns Through Python, Data Analytics & Geospatial Visualization

<p>
  <img src="https://img.shields.io/badge/Python-3.x-blue?style=for-the-badge&logo=python&logoColor=white">
  <img src="https://img.shields.io/badge/Pandas-Data%20Analysis-150458?style=for-the-badge&logo=pandas">
  <img src="https://img.shields.io/badge/Visualization-Plotly%20%7C%20Matplotlib-orange?style=for-the-badge">
  <img src="https://img.shields.io/badge/Geospatial-GeoPandas-green?style=for-the-badge">
  <img src="https://img.shields.io/badge/Project-Exploratory%20Data%20Analysis-purple?style=for-the-badge">
</p>

<p>
  <a href="#overview">Overview</a> •
  <a href="#dataset">Dataset</a> •
  <a href="#methodology">Methodology</a> •
  <a href="#visualizations">Visualizations</a> •
  <a href="#technology-stack">Technology</a> •
  <a href="#installation">Installation</a>
</p>

**Transforming historical terrorism data into meaningful analytical insights through interactive charts, geographical maps, statistical analysis, and advanced visualization techniques.**

[![GitHub Stars](https://img.shields.io/github/stars/shahidazam2020-oss/Data-Visualization?style=social)](https://github.com/shahidazam2020-oss/Data-Visualization/stargazers)
[![GitHub Forks](https://img.shields.io/github/forks/shahidazam2020-oss/Data-Visualization?style=social)](https://github.com/shahidazam2020-oss/Data-Visualization/forks)
</div>


---

## 📌 Project Overview

This project presents an exploratory data analysis and visualization of global terrorism incidents using the **Global Terrorism Database (GTD)**.

**Developed with Python, the project explores historical terrorism patterns across countries, regions, years, attack types, target categories, and casualty distributions.**

**The notebook combines data cleaning, preprocessing, feature selection, statistical visualization, and geospatial analysis to transform a large dataset into understandable visual insights.**

**It includes both static and interactive visualizations, enabling users to explore complex relationships within the dataset.**

### 🎯 Main Objectives

- 🌍 Explore the geographical distribution of terrorism incidents.
- 📅 Analyze historical terrorism trends across different years.
- ⚔️ Identify frequently recorded attack types.
- 🎯 Examine different target categories.
- 💀 Investigate casualties associated with recorded incidents.
- 🗺️ Visualize global incident distributions using geographical maps.
- 📊 Compare countries by incident frequency.
- 🔥 Examine geographical casualty concentrations.
- 📈 Analyze changes in attack patterns over time.
- 🧊 Demonstrate multidimensional and 3D data visualization.

---

## 📂 Dataset

### Global Terrorism Database (GTD)

**The project uses the Global Terrorism Database, accessed through KaggleHub.**

**Dataset source:** START-UMD / Global Terrorism Database

```python
import kagglehub

path = kagglehub.dataset_download("START-UMD/gtd")
```

**The dataset contains incident-level information, including:**

| Category | Example Attributes |
|---|---|
| Time | Year, Month, Day |
| Geography | Country, Region, Latitude, Longitude |
| Attack Information | Attack Type, Weapon Type |
| Target Information | Target Type |
| Organizations | Terrorist Group |
| Human Impact | Number Killed, Number Wounded |
| Incident Characteristics | Suicide Attack, Successful Attack |
| Property Impact | Property Damage |

**The notebook selects relevant attributes for exploratory analysis and visualization.**

---

## 🧹 Data Preprocessing & Preparation

**Before generating visualizations, the dataset undergoes several preparation steps.**

### Data Cleaning

- Load the dataset using Pandas.
- Inspect missing values.
- Select relevant columns.
- Handle missing casualty values.
- Create a cleaned DataFrame.
- Optimize numerical data types.
- Prepare variables for visualization.

### Casualty Calculation

**The project combines fatalities and injuries into a single casualty measure:**

```python
casualties = number_killed + number_wounded
```

**This variable supports comparisons of the human impact of recorded incidents.**

### Feature Selection

**Relevant attributes are selected according to the analytical objectives, reducing unnecessary data and simplifying visualization.**

---

## 🔬 Analytical Methodology

**The project follows a structured data analytics workflow.**

```text
             GLOBAL TERRORISM DATABASE
                         │
                         ▼
                  DATA ACQUISITION
                         │
                         ▼
                   DATA EXPLORATION
                         │
                         ▼
                    DATA CLEANING
                         │
                         ▼
                  DATA PREPROCESSING
                         │
                         ▼
                   FEATURE SELECTION
                         │
                         ▼
                EXPLORATORY DATA ANALYSIS
                         │
             ┌───────────┼───────────┐
             ▼           ▼           ▼
         TEMPORAL     GEOGRAPHIC   CATEGORICAL
          ANALYSIS     ANALYSIS     ANALYSIS
             │           │           │
             └───────────┼───────────┘
                         ▼
                   DATA VISUALIZATION
                         │
                         ▼
                 ANALYTICAL INSIGHTS
```

---

## 📊 Visualizations & Analytical Insights

**The project includes a collection of static, interactive, geographical, and multidimensional visualizations.**

### 1. 🥇 Top 20 Countries by Terrorism Incidents

**An interactive horizontal bar chart compares the countries with the highest numbers of recorded terrorism incidents.**

**Highlights:**
- Country-level comparison.
- Ranked incident frequency.
- Interactive tooltips.
- Visual comparison of incident counts.

### 2. 📉 Countries with the Lowest Number of Incidents

**A comparative visualization examines countries with relatively low recorded incident counts.**

**This provides a contrasting perspective on the global distribution of incidents.**

### 3. 💀 Casualties by Attack Type

**A scatter/strip-style visualization explores casualty distributions across different attack categories.**

Analytical dimensions include:
- Attack type.
- Casualties.
- Country.
- Region.
- Recorded organization.

### 4. 📅 Global Terrorism Incidents Over Time

**A time-based analysis examines the historical frequency of recorded incidents.**

It helps explore:
- Long-term trends.
- Periods of increasing activity.
- Periods of decreasing activity.
- Changes in incident frequency.

### 5. ⚔️ Incidents by Attack Type

**A bar chart compares the frequency of different recorded attack methods.**

**This visualization helps identify the most frequently represented attack categories in the dataset.**

### 6. 📈 Attack Type Trends Over Time

**This visualization examines how different attack categories change throughout the historical period covered by the dataset.**

**It provides a comparative view of temporal patterns across attack categories.**

### 7. 🔥 Attack Type vs. Target Type Heatmap

**A heatmap visualizes the relationship between attack categories and target categories.**

**Analytical dimensions:**

**`Attack Type × Target Type`**

It helps identify:
- Common attack-target combinations.
- Frequently represented target sectors.
- Relationships between categorical variables.
- Areas of higher incident frequency.

### 8. 🌍 Global Terrorism Incident Map

**A geographical visualization uses GeoPandas and Matplotlib to represent terrorism incidents across countries.**

**Countries are shaded according to recorded incident counts.**

**Technologies:**
- GeoPandas
- Matplotlib
- Geographic shapefiles

### 9. 🗺️ Interactive Choropleth Map

**An interactive Plotly map displays country-level incident distributions.**

**Features:**
- Global geographical coverage.
- Interactive country information.
- Continuous color scales.
- Country-level exploration.
- ISO Alpha-3 country-code conversion.

**The notebook also includes manual country mappings to accommodate historical country names and geographical changes.**

### 10. 🧊 3D Terrorism Visualization

**An interactive 3D scatter visualization explores multiple dimensions of the dataset.**

| Dimension | Variable |
|---|---|
| X-axis | Year |
| Y-axis | Region |
| Z-axis | Casualties |

**This visualization provides a multidimensional perspective on historical, regional, and casualty-related patterns.**

### 11. 🔥 Casualty Density by Country

**A choropleth visualization aggregates casualties by country.**

**Unlike incident-frequency maps, this analysis focuses on the combined number of people killed and wounded.**

**It allows comparisons between incident frequency and casualty impact.**

### 12. 🌡️ Geographical Casualty Density Heatmap

**A geographical density visualization uses:**
- Latitude.
- Longitude.
- Casualty values.
- Map-based density representation.

It provides a spatial perspective on the distribution of recorded casualties.

---

## 🛠️ Technology Stack

| Technology | Purpose |
|---|---|
| Python | Core programming language |
| Pandas | Data manipulation and cleaning |
| NumPy | Numerical computation |
| Matplotlib | Static visualizations |
| Seaborn | Statistical visualization |
| Plotly | Interactive charts and maps |
| GeoPandas | Geospatial data processing |
| PyCountry | Country-code conversion |
| Scikit-learn | Label encoding |
| KaggleHub | Dataset acquisition |
| Jupyter Notebook | Development environment |

---

## ⭐ Key Project Features

| Feature | Description |
|---|---|
| Data Cleaning | Missing-value inspection and preprocessing |
| Exploratory Analysis | Investigation of historical and categorical patterns |
| Statistical Visualization | Bar charts, scatter plots, and heatmaps |
| Time-Series Analysis | Historical incident trends |
| Geospatial Analysis | Country-level maps and geographical distributions |
| Interactive Mapping | Plotly choropleth visualizations |
| Advanced Visualization | Interactive 3D scatter plots |
| Casualty Analysis | Examination of fatalities and injuries |

---

## 📁 Repository Structure

The currently visible repository contains:

```text
Global-Terrorism-/
│
├── README.md
│
└── datavis_mid2025.ipynb
```

The README also documents visualization image filenames and a project notebook reference using a slightly different filename. Verify those paths and filenames before adding them to the repository structure.

---

## 🚀 Installation & Execution

### 1. Clone the Repository

```bash
git clone https://github.com/shahidazam2020-oss/Global-Terrorism-.git
```

### 2. Navigate to the Project

```bash
cd Global-Terrorism-
```

### 3. Install Dependencies

```bash
pip install pandas numpy matplotlib seaborn plotly geopandas pycountry kagglehub scikit-learn
```

### 4. Launch Jupyter Notebook

```bash
jupyter notebook
```

### 5. Open the Project Notebook

Open:

```text
datavis_mid2025.ipynb
```

### 6. Execute the Notebook

Run the notebook cells sequentially to reproduce the data preparation, exploratory analysis, and visualizations.

> **Note:** Some notebook cells use local Windows paths for geographic shapefiles and exported images. Update these paths when running the project on another computer.

---

## 🎓 Learning Outcomes

This project demonstrates practical experience in:

- Python programming.
- Data cleaning and preprocessing.
- Exploratory Data Analysis (EDA).
- Pandas and NumPy.
- Statistical data visualization.
- Interactive visualization with Plotly.
- Geospatial data processing.
- Choropleth mapping.
- Heatmap construction.
- 3D visualization.
- Time-series exploration.
- Categorical data analysis.
- Multidimensional data exploration.

---

## 🌐 Potential Applications

The analytical and visualization techniques demonstrated in this project can be adapted for:

- Geographic risk analysis.
- Historical event analysis.
- Geospatial intelligence dashboards.
- Public safety analytics.
- Academic research.
- Exploratory data analysis.
- Interactive analytical dashboards.

**Disclaimer:** These visualizations describe patterns in the available dataset. They do not establish causation, predict future incidents, or provide a complete measure of real-world security conditions.

---

## 🔭 Future Improvements

Potential extensions include:

- Develop an interactive analytical dashboard.
- Add more detailed statistical summaries.
- Include country and region comparison filters.
- Improve missing-data handling.
- Add year-range filtering.
- Integrate additional geospatial visualization techniques.
- Include correlation analysis.
- Add downloadable analytical reports.
- Improve reproducibility through a requirements file.
- Add screenshots of the actual notebook visualizations.

---

## 👨‍💻 About the Developer

### Shahid Azam

**MS Computer Science | Artificial Intelligence**

Institute of Management Sciences, Peshawar, Pakistan

Interested in Artificial Intelligence, Machine Learning, Data Visualization, and research-oriented software development.

### Connect With Me

- 💻 GitHub: [shahidazam2020-oss](https://github.com/shahidazam2020-oss)
- 🔗 LinkedIn: [Shahid Azam](https://www.linkedin.com/in/shahid-azam-mughal-787b58235/)
- 📚 ResearchGate: [Shahid Azam](https://www.researchgate.net/profile/Shahid-Azam-5)
- 🆔 ORCID: [0009-0001-6825-8863](https://orcid.org/0009-0001-6825-8863)
- 📧 Email: shahidazam2020@gmail.com

---

## 🤝 Contributions

Suggestions, improvements, and contributions are welcome.

1. Fork this repository.
2. Create a new branch.
3. Make your changes.
4. Submit a pull request.

---

## 📜 Disclaimer

This repository is an academic data visualization and exploratory analysis project based on the Global Terrorism Database.

The project is intended for educational and analytical purposes. Its visualizations should not be interpreted as causal conclusions about terrorism, individual countries, communities, or populations.

---

<div align="center">

## ⭐ Support This Project

If you find this project useful, consider giving the repository a star.

**Explore • Analyze • Visualize • Learn**

🌍 *Turning Historical Data into Meaningful Visual Insights*

</div>
