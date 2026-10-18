# 🌍 Global Terrorism Data Visualization & Analysis

<p align="center">
  <b>📊 Interactive Data Visualization Project using Python</b><br>
  <i>Exploring global terrorism incidents, casualties, attack types, targets, regions, and geographical patterns</i>
</p>

---

## 📌 Project Overview

This project presents a comprehensive **data visualization and exploratory analysis of global terrorism incidents** using the **Global Terrorism Database (GTD)**.

The notebook transforms a large-scale terrorism dataset into meaningful visual insights using **Python-based data analysis and visualization techniques**. The project focuses on understanding the distribution, trends, geographical concentration, attack methods, target types, and casualties associated with terrorism incidents.

The analysis includes both **static and interactive visualizations**, allowing users to explore complex patterns in the data through charts, maps, heatmaps, and 3D graphics.

---

# 🎯 Project Objectives

**The main objectives of this project are to:**

* 🌍 Analyze the geographical distribution of terrorism incidents
* 📅 Examine terrorism incidents across different years
* ⚔️ Identify the most common attack types
* 🎯 Analyze different target types
* 💀 Investigate casualties associated with terrorism attacks
* 🗺️ Visualize incidents using geographical maps
* 📊 Compare countries based on the number of incidents
* 🔥 Identify areas with high casualty density
* 📈 Explore attack trends over time
* 🔗 Analyze relationships between attack types and target types
* 🧊 Demonstrate advanced 3D data visualization

---

# 📂 Dataset

The project uses the **Global Terrorism Database (GTD)**, downloaded programmatically using KaggleHub.

```python
import kagglehub

path = kagglehub.dataset_download("START-UMD/gtd")
```

**The dataset contains information about terrorism incidents, including:**

* Year
* Month
* Day
* Country
* Region
* Attack type
* Target type
* Terrorist group
* Number killed
* Number wounded
* Weapon type
* Property damage
* Suicide attacks
* International characteristics
* Attack success
* And other incident-related attributes

**The project selects relevant attributes from the original dataset before performing visualization and analysis.**

---

# 🧹 Data Preparation

**The notebook performs several preprocessing steps before visualization.**

### Data Cleaning

The project:

* Loads the GTD dataset using Pandas
* Examines missing values
* Selects relevant variables
* Handles missing casualty values
* Creates a cleaned dataframe
* Converts numerical columns to smaller data types to reduce memory usage
* Creates a new **casualties** variable

**The casualty variable is calculated as:**

```python
casualties = number killed + number wounded
```

**This provides a combined measure of the human impact of an incident.**

---

# 📊 Visualizations

## 🥇 1. Top 20 Countries by Terrorism Incidents

**A horizontal interactive bar chart is used to identify countries with the highest number of recorded terrorism incidents.**

### Visualization highlights:

* Country-level comparison
* Number of incidents
* Interactive tooltips
* Ranked presentation
* Color intensity based on incident count

**Purpose:**
**This visualization makes it easy to compare the countries with the largest numbers of recorded incidents.**

---

## 📉 2. Countries with the Lowest Number of Incidents

**The project also visualizes countries with relatively low numbers of recorded terrorism incidents.**

**This provides a contrasting view to the top-country analysis and demonstrates how incident frequency varies across countries.**

---

## 💀 3. Casualties by Attack Type

**A strip/scatter-style visualization is used to analyze casualties associated with different attack types.**

**The visualization considers:**

* Attack type
* Total casualties
* Country
* Region
* Terrorist organization

**Purpose:**
**To investigate how casualty levels vary between different methods of attack.**

---

## 📅 4. Terrorism Incidents Over Time

**The project analyzes the number of terrorism incidents recorded for each year.**

**This visualization helps identify:**

* Periods of increasing activity
* Periods of decreasing activity
* Long-term patterns
* Changes in incident frequency

---

## ⚔️ 5. Incidents by Attack Type

**A bar chart compares the frequency of different attack methods.**

**Examples of attack categories represented in the dataset include different forms of armed attacks, bombings, kidnappings, and other methods.**

**Purpose:**
**To determine which attack types occur most frequently within the dataset.**

---

## 📈 6. Attack Type Trends Over Time

*The project goes beyond a simple frequency comparison by examining how different attack types change over time.*

*Multiple attack categories are plotted across the years, allowing trends to be compared.*

*This provides a deeper understanding of how the nature of terrorism incidents has changed over the historical period covered by the dataset.*

---

# 🔥 7. Attack Type vs Target Type Heatmap

**A heatmap is created using a pivot table containing:**

**Attack Type × Target Type**

**The cells represent the number of incidents associated with each combination.**

### Why this visualization is useful

**It helps identify:**

* Common attack-target combinations
* Frequently targeted sectors
* Relationships between attack methods and targets
* Areas with relatively high incident concentrations

**This is one of the most useful visualizations in the project for discovering relationships between categorical variables.**

---

# 🌍 8. Global Terrorism Incident Map

A geographical visualization is created using **GeoPandas** to display terrorism incidents by country.

**Countries are shaded according to their number of recorded incidents.**

### Technologies used

* GeoPandas
* Matplotlib
* Geographic shapefiles

**Purpose:**
**To provide a visual representation of the global geographical distribution of terrorism incidents.**

---

# 🗺️ 9. Interactive Choropleth Map

An interactive **Plotly choropleth map** is also developed.

**Countries are colored according to the number of terrorism incidents.**

The map provides:

* 🌍 Global geographical coverage
* 🖱️ Interactive country information
* 🎨 Continuous color scale
* 📊 Incident intensity visualization
* 🔎 Country-level exploration

**Country names are converted into **ISO Alpha-3 codes** to improve geographic compatibility.**

**The project also includes manual mappings for historical or differently named countries such as:**

* Soviet Union
* Yugoslavia
* Czechoslovakia
* East Germany
* West Germany
* Rhodesia
* Zaire
* South Yemen
* North Yemen

**This improves the geographical representation of historical records.**

---

# 🧊 10. 3D Terrorism Visualization

The project includes an advanced **3D scatter visualization** using Plotly.

The visualization represents:

```text
X → Year
Y → Region
Z → Casualties
```

** point represents terrorism-related observations, with casualty levels represented through marker properties.**

### Purpose

**The 3D visualization provides another perspective for examining the relationship between:**

* Time
* Geographic region
* Human casualties

**It demonstrates the use of advanced interactive visualization techniques for multidimensional datasets.**

---

# 🔥 11. Casualty Density by Country

A second geographical visualization focuses on **total casualties rather than incident frequency**.

The project aggregates casualties by country and visualizes them using a choropleth map.

This is important because a country with fewer incidents can potentially have a high casualty impact.

Therefore, comparing:

**Incident count vs. casualty count**

**provides a more complete understanding of terrorism-related impact.**

---

# 🌡️ 12. Geographical Casualty Density Heatmap

The final visualization uses geographical coordinates to create a **casualty-density heatmap**.

The visualization uses:

* Latitude
* Longitude
* Casualties
* Map-based density visualization

It identifies geographical areas where incidents with higher casualty levels are concentrated.

This provides a more detailed spatial perspective than country-level maps alone.

---

# 🧰 Technologies Used

| Technology          | Purpose                          |
| ------------------- | -------------------------------- |
| 🐍 Python           | Core programming language        |
| 🐼 Pandas           | Data manipulation and analysis   |
| 🔢 NumPy            | Numerical operations             |
| 📊 Matplotlib       | Static visualization             |
| 🎨 Seaborn          | Statistical visualization        |
| 📈 Plotly           | Interactive visualizations       |
| 🌍 GeoPandas        | Geographic data visualization    |
| 🗺️ PyCountry       | Country-to-ISO code conversion   |
| 🤖 Scikit-learn     | Label encoding for visualization |
| 📓 Jupyter Notebook | Development environment          |
| 📦 KaggleHub        | Dataset acquisition              |

---

# ⭐ Key Features

### 📊 Data Analysis

* Missing-value analysis
* Data cleaning
* Feature selection
* Data type optimization
* Casualty calculation

### 📈 Statistical Visualization

* Bar charts
* Scatter/strip plots
* Line charts
* Heatmaps

### 🌍 Geographic Visualization

* World maps
* Choropleth maps
* Casualty-density maps
* Coordinate-based heatmaps

### 🧊 Advanced Visualization

* Interactive Plotly charts
* 3D scatter visualization
* Multidimensional data exploration

---

# 📁 Project Structure

```text
Global-Terrorism-Data-Visualization/
│
├── datavis_mid2025(1).ipynb
│
├── images/
│   ├── incidents_bargraph_bycountry.png
│   ├── low_country_terrorism.png
│   ├── scatter_casualvsattack.png
│   ├── subplots_year_attype.png
│   ├── heatmap_attckvstarget.png
│   ├── incidents_country.png
│   ├── 3dplot.png
│   ├── chloropeth_country_casualties.png
│   └── contour.png
│
└── README.md
```

---

# 🚀 How to Run the Project

### 1️⃣ Clone the Repository

```bash
git clone YOUR_GITHUB_REPOSITORY_URL
```

### 2️⃣ Install Required Libraries

```bash
pip install pandas numpy matplotlib seaborn plotly geopandas pycountry kagglehub scikit-learn
```

### 3️⃣ Open the Notebook

Open:

```text
datavis_mid2025(1).ipynb
```

using:

* Jupyter Notebook
* JupyterLab
* Visual Studio Code
* Google Colab

### 4️⃣ Run the Notebook

Run the cells sequentially to reproduce the data cleaning process and visualizations.

> **Note:** Some original notebook cells use local Windows paths for shapefiles and exported images. These paths should be updated if the project is executed on another computer.

---

# 📌 Major Analytical Areas

The project investigates four major dimensions of the GTD data:

```text
                 🌍 GLOBAL TERRORISM ANALYSIS
                           │
        ┌──────────────────┼──────────────────┐
        │                  │                  │
     📅 TIME           🌍 LOCATION         ⚔️ ATTACK
        │                  │                  │
   Yearly Trends      Countries          Attack Types
   Historical         Regions            Target Types
   Patterns           Maps               Weapons
        │                  │                  │
        └──────────────────┼──────────────────┘
                           │
                      💀 CASUALTIES
                           │
                 Killed + Wounded
                           │
                 Density & Distribution
```

---

# 🎓 Learning Outcomes

Through this project, the following practical skills are demonstrated:

* Data preprocessing with Pandas
* Exploratory Data Analysis (EDA)
* Handling missing values
* Feature selection
* Data type optimization
* Statistical visualization
* Interactive visualization
* Geographic data analysis
* Choropleth mapping
* Heatmap construction
* 3D data visualization
* Time-series analysis
* Categorical data analysis
* Multidimensional data exploration

---

# 💡 Applications

The visualization techniques demonstrated in this project can be adapted for:

* 🌍 Geographic risk analysis
* 📊 Historical event analysis
* 🗺️ Geospatial intelligence dashboards
* 📈 Public safety analytics
* 🔎 Exploratory data analysis
* 🎓 Academic research
* 📊 Business intelligence
* 🌐 Interactive analytical dashboards

> **Important:** The visualizations are intended for analytical and educational purposes. They describe patterns present in the dataset and should not be interpreted as causal explanations.

---

# 🏆 Project Highlights

<p align="center">

**🌍 Global Analysis**
Analyze terrorism incidents across countries and regions.

**📊 Rich Visualizations**
Use bar charts, line charts, scatter plots, heatmaps, and maps.

**🗺️ Geospatial Analysis**
Visualize incident and casualty concentrations geographically.

**🧊 3D Exploration**
Explore the relationship between year, region, and casualties.

**⚡ Interactive Charts**
Use Plotly to explore data dynamically.

</p>

---

# 👨‍💻 Author

**Shahid Azam**

This project demonstrates practical skills in:

**Python • Data Visualization • Exploratory Data Analysis • Pandas • NumPy • Matplotlib • Seaborn • Plotly • GeoPandas • Data Analytics • Geospatial Visualization**

---

## 📜 Disclaimer

This project is an **academic data visualization and exploratory analysis project** based on the Global Terrorism Database. The visualizations are intended to demonstrate data-analysis and visualization techniques and should not be interpreted as causal conclusions about terrorism or individual countries.
