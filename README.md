# Network Analysis of AIMS Ghana Students

This repository contains Python code for performing **social network analysis** on a dataset of students from AIMS Ghana. The analysis includes constructing a friendship network, computing centrality measures, visualizing node importance, and evaluating community structure.

## Table of Contents

- [Dataset](#dataset)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Analysis Performed](#analysis-performed)
- [Results](#results)
- [Insights & Discussion](#insights--discussion)
- [License](#license)

---

## Dataset

The dataset used in this analysis is `AIMS-GHANA-NET2425.csv`. It contains the following columns:

- `First_Name`: Name of the student
- `Friend1`, `Friend2`, `Friend3`: Names of the student's friends

The data is **tab-delimited** (`\t`).

---

## Features

The code performs the following tasks:

1. Loads the dataset using **Pandas**.
2. Constructs a **network graph** using **NetworkX** where nodes represent students and edges represent friendships.
3. Computes and visualizes centrality measures:
   - **Degree Centrality**: Measures node connectivity
   - **Closeness Centrality**: Measures node proximity to others
   - **Eigenvector Centrality**: Measures influence of a node in the network
4. Plots **degree distribution** of the network.
5. Detects **communities** using the **Louvain method** and computes **modularity score** to evaluate community structure.

---

## Installation

To run this code, you need Python 3.x and the following packages installed:

```bash
pip install pandas numpy matplotlib networkx python-louvain

## Analysis Performed

### 1. Graph Construction
- **Nodes:** Students
- **Edges:** Friend connections

### 2. Centrality Measures
- **Degree Centrality:** Highlights students with the most connections.
- **Closeness Centrality:** Identifies students closest to everyone in the network.
- **Eigenvector Centrality:** Detects influential students connected to other well-connected students.

### 3. Visualization
- Bar plots for each centrality measure.
- Degree distribution histogram to understand network connectivity.

### 4. Community Detection
- Louvain method for identifying communities.
- Modularity score to evaluate the strength of community structure.

---

## Results
- Nodes with the **highest centrality measures** are highlighted in the outputs.
- Graph visualizations provide insights into influential students and network structure.
- **Modularity Score** indicates a strong community structure with minor overlaps.

---

## Insights & Discussion

**Q13. Can we predict friendships based on common connections?**  
- **Answer:** Yes, students who share many common friends are more likely to form new friendships. This aligns with social network theory, where mutual connections increase the likelihood of interaction.

**Q14. What role do isolated students play, and should they be integrated more?**  
- **Answer:** Isolated students have limited influence in the network and may miss out on opportunities for collaboration and social support. Integrating them into existing communities can enhance their experience and strengthen the overall network cohesion.
