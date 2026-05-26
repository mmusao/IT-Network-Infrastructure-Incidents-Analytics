<div align="center">

# 📊 IT Infrastructure Incident Analytics

### Exploratory & Inferential Analysis of IT Network Infrastructure Incidents

[![Quarto](https://img.shields.io/badge/Built%20with-Quarto-blue?logo=quarto&logoColor=white)](https://quarto.org)
[![R](https://img.shields.io/badge/R-4.5.2-276DC3?logo=r&logoColor=white)](https://www.r-project.org/)
[![Python](https://img.shields.io/badge/Python-3.12-3776AB?logo=python&logoColor=white)](https://www.python.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-gold.svg)](LICENSE)
[![RPubs](https://img.shields.io/badge/Live%20Report-RPubs-orange)](https://rpubs.com/mmusao/1435887)

---

*A capstone case study applying five exploratory and inferential analytics techniques to real-world IT incident data from company x.*

**Data Analytics II — MBA Programme — Lagos Business School**

</div>

---

## 📑 Table of Contents

- [Project Overview](#-project-overview)
- [Key Findings](#-key-findings)
- [Repository Structure](#-repository-structure)
- [Tech Stack](#-tech-stack)
- [How to Reproduce](#-how-to-reproduce)
- [Author](#-author)
- [Citation](#-citation)
- [License](#-license)

---

## 🔍 Project Overview

| Attribute | Detail |
|:---|:---|
| **Course** | Data Analytics II (MMBA-8-DA-II) |
| **Institution** | Lagos Business School, Pan-Atlantic University |
| **Professor** | Prof Bongo Adi |
| **Case Study** | CS 1 — Exploratory & Inferential Analytics |
| **Author** | Muhammad O. Musa |
| **Role** | Manager, Global IT Network Infrastructure — Company X |
| **Data Source** | SysAid ITSM (Cloud instance) |
| **Observations** | 146 closed IT incidents |
| **Time Period** | March 2025 – April 2026 (13 months) |

This study analyses **146 closed IT incident tickets** extracted from the SysAid IT Service Management platform at Company X. The dataset covers incidents managed by the Global IT Network Infrastructure team, including connectivity outages, VPN failures, application downtimes, and workspace enablement issues.

Five analytical techniques are applied in sequence:

| # | Technique | Purpose |
|---|---|---|
| 1 | **Exploratory Data Analysis** | Profile data quality, distributions, and outliers |
| 2 | **Data Visualisation** | Communicate patterns through 6 publication-quality plots |
| 3 | **Hypothesis Testing** | Test whether urgency drives resolution outcomes |
| 4 | **Correlation Analysis** | Identify redundant variables and factor relationships |
| 5 | **Multiple Regression** | Model resolution time from ticket metadata |

---

## 💡 Key Findings

### 1. Resolution Windows Are Highly Skewed
> Mean = **217 hours** vs. Median = **74 hours** — average-based SLA targets are misleading.

### 2. Urgency Does Not Drive Resolution Speed
> Kruskal-Wallis test: *H* = 2.76, ***p* = 0.251** — no significant difference across urgency levels.

### 3. Urgency and Priority Are Redundant
> Spearman **ρ = 0.883** (*p* < 0.001) — these two fields capture nearly identical information.

### 4. Ticket Metadata Cannot Predict Resolution Time
> OLS regression **R² = 0.04** (*F*-test *p* = 0.452) — only 4% of variance explained by ticket-level data.

### 5. Recommendation
> **Dual-track improvement:** Reform SLA targets to percentile-based metrics (P50/P80/P95) **+** enrich SysAid data capture with vendor dependency, root cause, and escalation count fields.

---

## 📁 Repository Structure

```
IT-Network-Infrastructure-Incidents-Analytics/
│
├── index.qmd    							   # Quarto source document
├── Exported_Service_Records.csv               # Anonymised SysAid data
├── index.html							  	   # Rendered HTML report
├── README.md                                  # This file
└── LICENSE                                    # MIT License
```

---

## 🛠️ Tech Stack

<table>
<tr>
<td align="center"><strong>Document</strong></td>
<td align="center"><strong>R Packages</strong></td>
<td align="center"><strong>Python Packages</strong></td>
</tr>
<tr>
<td>

- Quarto 1.4+
- HTML (self-contained)
- Custom CSS theming

</td>
<td>

- `tidyverse` (dplyr, ggplot2, readr)
- `lubridate`
- `ggcorrplot`
- `knitr` / `kableExtra`
- `car` (VIF)
- `broom`
- `e1071` (skewness/kurtosis)

</td>
<td>

- `pandas`
- `numpy`
- `matplotlib`
- `seaborn`
- `scipy`
- `statsmodels`
- `patsy`

</td>
</tr>
</table>

---

## 🔄 How to Reproduce

### Prerequisites

- [R 4.4+](https://cran.r-project.org/) with RStudio
- [Python 3.10+](https://www.python.org/)
- [Quarto CLI 1.4+](https://quarto.org/docs/get-started/)

### Steps

```bash
# 1. Clone this repository
git clone https://github.com/mmusao/IT-Network-Infrastructure-Incidents-Analytics.git
cd IT-Network-Infrastructure-Incidents-Analytics

# 2. Install R packages
Rscript -e 'install.packages(c("tidyverse", "lubridate", "scales", "ggcorrplot",
              "knitr", "kableExtra", "car", "broom", "e1071"))'

# 3. Install Python packages
pip install pandas numpy matplotlib seaborn scipy statsmodels patsy

# 4. Render the document
quarto render index.qmd
```

The rendered HTML will appear in the same directory.

---

## 👤 Author

**Muhammad O. Musa**
- **Role:** Manager, Global IT Network Infrastructure
- **Organisation:** Company X
- **Location:** Lagos, Nigeria
- **Programme:** MBA, Lagos Business School, Pan-Atlantic University

---

## 📖 Citation

If you reference this work, please cite:

```
Musa, M. O. (2026). Exploratory & inferential analysis of IT network
infrastructure incidents [Capstone case study]. Data Analytics II,
MBA Programme, Lagos Business School, Pan-Atlantic University.
```

---

## 📄 License

This project is licensed under the **MIT License** — see the [LICENSE](LICENSE) file for details.

The dataset has been anonymised and is shared for academic purposes only.

---

<div align="center">

**Built with ❤️ using [Quarto](https://quarto.org) • [R](https://www.r-project.org/) • [Python](https://www.python.org/)**

*Lagos Business School — Data Analytics II — May 2026*

</div>
