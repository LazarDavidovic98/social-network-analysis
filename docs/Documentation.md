# Project: Social Network Analysis of Scientific Collaboration

This documentation covers all technical and analytical aspects of the project developed as part of the *Social Network Analysis* course. The project's focus is the analysis of scientific collaboration among staff members at the Faculty of Medicine, University of Belgrade, using methods from the field of network analysis.

---

## Dataset

**Files used:**
- `autori.xlsx` – list of relevant authors (department employees)
- `epidemiologija.xlsx`, `imunologija.xlsx`, `infektivne_bolesti.xlsx`, `mikrobiologija.xlsx` – raw publication data requiring preprocessing
- `mreza_casopisa.gml` – journal network graph

**Columns in the .xlsx files:**
- `Author`, `Authors`, `Title`, `Year`, `Source title`, `Volume`, `Issue`, `Art. No.`, `Page start`, `Page end`, `Page count`, `Cited by`, `Link`, `Document Type`, `Source`

**Filtering criteria:**
- Only the following types of documents were included: Article, Article in Press, Review, Book Chapter, Letter, Note
- Only authors from `autori.xlsx` were included

---

## Libraries and Tools Used

- `pandas` – table/data manipulation
- `networkX` – network creation and analysis
- `matplotlib`, `graphviz` – visualization
- `Gephi` – advanced visual analysis and Louvain community detection

---

## 🧾 Key Analyses

### Statistical Analysis
- Number of publications per author (full and fractional counting)
- Average number of co-authors
- Computation of H-index per author and comparison with given values
- Productivity analysis by year and department
- Journal publication frequency

### Network Modeling
- Construction of an undirected weighted co-authorship network
- Construction of the journal network from the `mreza_casopisa.gml` file

### Network Metrics
- Network density
- Diameter and average path length
- Clustering coefficients (global and local)
- Degree assortativity
- Rich-club phenomenon analysis (comparison with Havel-Hakimi graph)
- Power-law degree distribution analysis

### Centrality
- Degree, closeness, betweenness, eigenvector
- Construction of a composite centrality score (heuristic)
- Identification of key authors and inter-departmental brokers

### Community Detection
- **Louvain method** (via Gephi) – visualization and resolution sensitivity analysis
- **Spectral clustering** – with comparison to the Girvan–Newman algorithm
- Analysis of community validity and identification of bridges between groups

---

## Conclusions and Recommendations

- Identified key network actors can serve as candidates for strengthening scientific team connections
- The network exhibits small-world and assortative properties
- Composite centrality helps rank authors with the most significant influence

---

## Technical Details

- Project developed in Python 3.9
- `.ipynb` files executed in Jupyter Notebook environment
- Network visualizations performed partly in Gephi and partly in Python
- The analyzed graphs are undirected and weighted (by the number of joint publications)

---

<p style="color:#999999;">© 2024 Lazar Davidović — School of Electrical Engineering, University of Belgrade<br/>
© 2024 Luka Simić — School of Electrical Engineering, University of Belgrade</p>
