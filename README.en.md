# 📦 COMEXBR – Brazilian Foreign Trade Data Pipeline

This project is a Data Engineering MVP developed by Wallace Lima as part of the PUC-Rio program. Its goal is to build a complete data pipeline for ingestion, modeling, transformation, and analysis of Brazil’s foreign trade data, using **Databricks Community Edition** and modern Big Data and visualization tools.

---

## 🧠 Project Objective

To investigate trade patterns, key source and destination countries, most traded products, and temporal behaviors in Brazil’s foreign trade operations. The project answers five key business questions using official datasets.

---

## 🚀 Tech Stack

- **Databricks Community Edition**
- **Apache Spark / PySpark**
- **Delta Lake**
- **SQL (SparkSQL)**
- **Pandas & Matplotlib / Plotly**
- **Google Drive** (for temporary data storage)
- **GeoPandas and Folium** (for geospatial visualizations)
- **`gdown`** (for automated data ingestion from Google Drive)

---

## 📂 Project Structure

| Folder / File                          | Description                                                      |
|----------------------------------------|------------------------------------------------------------------|
| `COMEXBR_Wallace_Lima_MVP_Engenharia_de_dados.ipynb` | Main notebook with the full pipeline and analysis             |
| `documentacao_projeto_comercio_exterior.pdf`        | Supporting document and academic project description          |
| `README.md`                             | Portuguese version of this README                              |

---

## 🔄 Project Phases

### 1. 📥 Data Collection & Storage
- Source: CSV files extracted from official sources and stored in Google Drive
- Ingested automatically using `gdown` into Databricks DBFS

### 2. 🏗️ Data Modeling
- Star schema implemented
- Fact tables (`fato_exportacao`, `fato_importacao`) and dimension tables (`dim_pais`, `dim_uf`, `dim_ncm`, etc.)
- Explicit data dictionary and schema definitions with data types

### 3. 🧼 Data Cleaning & ETL
- Name and schema standardization, encoding conversion (`latin1`)
- Conversion of Brazilian monetary/number formats into float
- Joins, enrichment, and persistence in Delta Lake
- Permanent views: `vw_exportacao` and `vw_importacao`

### 4. 📊 Data Analysis
- Top 10 countries by FOB value (exports/imports)
- Most exported and imported products
- Brazilian states with the highest trade volume
- Historical yearly evolution of imports/exports
- Interactive visualizations with Plotly and geographic maps

---

## 📈 Visual Outputs

- Bar and pie charts
- Time series plots
- Interactive choropleth maps (Plotly)
- Comparative insights by country, product, and year

---

## 💬 Conclusions

- The pipeline is scalable, robust, and covers all essential stages of a real-world data engineering workflow
- It clearly identifies Brazil’s main trading partners over time
- The visualizations offer relevant insights for decision-making and a better understanding of Brazil’s international trade scenario

---

## 📄 License

This is an academic project. The use of its data and code is allowed only with proper attribution to the author.

---

## 👨‍💻 Author

**Wallace Lima**  
Data Engineering | Data Science | Finance | Compliance  
[LinkedIn](https://www.linkedin.com/in/wallacelima17/)
