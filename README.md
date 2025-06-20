# 📊 Scientific Collaboration Network – Faculty of Medicine, University of Belgrade

This project presents a comprehensive analysis of scientific output and collaboration among staff members from four departments of the Faculty of Medicine, University of Belgrade: **Immunology, Epidemiology, Infectious Diseases, and Microbiology**. The project was completed as part of the *Social Network Analysis* course at the School of Electrical Engineering, University of Belgrade.

The goal of the analysis is to model and analyze **co-authorship networks** and **journal networks** through graph metrics, centrality measures, community detection, and visualization, using real-world data collected from the **Scopus database** and institutional sources.

## Project Overview

The project includes the following steps:
- Cleaning and merging raw data from multiple Excel files (`epidemiology.xlsx`, `immunology.xlsx`, etc.)
- Filtering authors based on the official staff list (`authors.xlsx`)
- Constructing co-authorship and journal graphs using `NetworkX`
- Analyzing centrality (degree, closeness, eigenvector, betweenness)
- Community detection (Louvain method, spectral clustering)
- Comparing with random networks and measuring characteristics such as density, clustering, assortativity, etc.
- Visualizing networks and interpreting the results

## Project Structure

<pre style="font-size: 14px; line-height: 1.4;">
├── <span style="color:#2aa198;">data/                           </span> # Raw data files (e.g., CSV, JSON)
├── <span style="color:#2aa198;">docs/                           </span> # Project documentation
├── <span style="color:#2aa198;">images/                         </span> # Visualizations and plots
├── <span style="color:#2aa198;">magazine/                       </span> # Additional materials or articles
├── <span style="color:#2aa198;">models/                         </span> # Graph models and processed data
├── <span style="color:#2aa198;">.gitignore                      </span> # Git ignore rules
├── <span style="color:#2aa198;">README.md                       </span> # Project overview and instructions
├── <span style="color:#2aa198;">co-authorship-networks.ipynb    </span> # Jupyter notebook for co-authorship analysis
└── <span style="color:#2aa198;">journal-networks.ipynb          </span> # Jupyter notebook for journal network analysis
</pre>


## Technologies Used

- `Python` (v3.9+)
- `pandas` – for data manipulation
- `networkX` – for network modeling and analysis
- `matplotlib` / `graphviz` – for visualization
- `Gephi` – for advanced visual analysis and Louvain community detection

## Key Analyses

- Number of publications per author (full and fractional counting)
- Author H-index
- Distribution by years and journals
- Network metrics: clustering, centrality, assortativity, diameter
- Detection of key individuals and communities within the scientific network

## Objective

Using social network analysis tools, the aim is to identify:
- the most influential scientific actors,
- the level of collaboration among authors and across departments,
- structural patterns of scientific production,
- potential recommendations for connecting isolated groups or individuals.

---

**Detailed documentation is available here**: [Documentation](docs/Documentation.md)

**You can also view the project presentation**: [Presentation](docs/Presentation.pdf)
