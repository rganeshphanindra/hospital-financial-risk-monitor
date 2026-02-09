# **Hospital Financial Risk Monitor**



An end to end healthcare financial analytics project designed to identify loss making hospitals, isolate structural cost drivers, and enable leadership to prioritize targeted interventions using repeatable metrics and dashboards.



This project combines Python based analysis, executive level insights, and an interactive Tableau dashboard to simulate how a health system would monitor financial risk at scale.



### **Why this project exists**



Most healthcare analytics projects stop at reporting metrics. This one exists to answer a harder leadership question:



Where should executives intervene first to stop financial losses and how should they monitor whether those actions are working.



Hospitals fail financially for different reasons, but leadership time and capital are limited. This project reframes hospital performance analysis from descriptive reporting to decision support by narrowing focus to cost structure, revenue gaps, and early warning signals rather than surface level utilization metrics alone.



### **Business problem**



Health systems often manage hundreds of hospitals with vastly different cost structures, payer mixes, and operating models. While aggregate financial performance may appear stable, system level reporting frequently masks a small subset of hospitals that drive a disproportionate share of losses.



The core challenge for leadership is not identifying that losses exist, but determining:



Which hospitals are structurally misaligned

Why they are underperforming

Where intervention will have the highest return

How to monitor improvement before losses compound



This project addresses that challenge by shifting analysis from hospital level reporting to system wide prioritization. Instead of treating all loss making hospitals equally, it isolates facilities where losses are driven by structural cost inefficiencies rather than temporary utilization fluctuations.



The outcome is a framework that enables leadership to focus intervention efforts on the hospitals most likely to benefit from cost restructuring, revenue optimization, or service line rationalization.



### **Dataset overview**



This analysis is based on a curated hospital level financial dataset containing 435 hospitals across multiple counties and operating models.



Each record represents a single hospital and includes structural, financial, and operational metrics such as:



Facility identifiers and attributes

Bed size category and staffing levels

Teaching and rural classification

Net income and operating margin

Cost per patient

Revenue per patient

Utilization rate



The dataset was cleaned and standardized in Python to ensure consistent definitions across hospitals before analysis and visualization. No synthetic data was introduced.



Key scope decisions:



The analysis is cross sectional and represents a single financial period

Hospitals are evaluated relative to system wide medians rather than external benchmarks

Utilization is treated as a secondary signal rather than a primary driver of losses



This scope was intentionally chosen to support prioritization and intervention decisions, not forecasting or hospital specific operational planning.



### **Analytical approach**



The analysis was conducted in Python using a structured, decision driven workflow rather than exploratory charting.



The process followed four deliberate stages:



Data preparation

Raw hospital level data was cleaned, validated, and reduced to a focused set of financial and operational fields relevant to profitability and efficiency. Edge cases such as zero patient days were excluded to prevent distorted metrics.



Metric construction

Decision level metrics were created to normalize performance across hospitals, including operating margin, cost per patient, revenue per patient, and utilization rate. System wide medians were used as internal benchmarks to enable relative comparison.



Driver isolation

Hospitals were segmented based on loss status and cost structure to distinguish between losses driven by structural inefficiency versus those driven by utilization gaps. This allowed prioritization of intervention targets rather than treating all loss making hospitals equally.



Operationalization

Final outputs were designed to support ongoing monitoring rather than one time analysis. Python was used for discovery and logic validation, while Tableau was used to operationalize insights into a repeatable leadership monitoring tool.



This approach ensures that analytical rigor directly translates into actionable decision support.



### **Key findings**



Structural cost inefficiencies are the primary driver of hospital losses

Loss making hospitals consistently exhibit higher cost per patient relative to system medians, even when utilization rates are comparable to profitable peers.



Revenue gaps reinforce cost pressure

Loss making hospitals also generate lower revenue per patient, compounding the impact of elevated cost structures and limiting margin recovery through volume alone.



Losses are concentrated, not evenly distributed

A minority of hospitals account for a disproportionate share of total system losses, while highly profitable hospitals mask these issues at the aggregate level.



Small and mid sized hospitals face the greatest structural risk

Losses are most concentrated among hospitals in the small to mid bed size range, particularly those without the scale or subsidies available to large teaching institutions.



Utilization is a secondary signal, not a root cause

While low utilization exists in some loss making hospitals, it does not explain the majority of losses when compared against cost and revenue normalization.



### **Executive recommendations**



Structural cost inefficiencies are the primary driver of hospital losses

Loss making hospitals consistently exhibit higher cost per patient relative to system medians, even when utilization rates are comparable to profitable peers.



Revenue gaps reinforce cost pressure

Loss making hospitals also generate lower revenue per patient, compounding the impact of elevated cost structures and limiting margin recovery through volume alone.



Losses are concentrated, not evenly distributed

A minority of hospitals account for a disproportionate share of total system losses, while highly profitable hospitals mask these issues at the aggregate level.



Small and mid sized hospitals face the greatest structural risk

Losses are most concentrated among hospitals in the small to mid bed size range, particularly those without the scale or subsidies available to large teaching institutions.



Utilization is a secondary signal, not a root cause

While low utilization exists in some loss making hospitals, it does not explain the majority of losses when compared against cost and revenue normalization.



### **Tableau dashboard**



The Tableau dashboard translates analytical findings into a single executive monitoring view designed for prioritization and early intervention.



The dashboard is intentionally table driven, reflecting how leadership teams act on ranked lists rather than isolated visuals. It enables users to:



Identify loss making hospitals sorted by operating margin

Understand whether losses are driven by cost structure or revenue gaps

Benchmark hospital performance against system medians

Filter to priority segments by bed size, county, and teaching or rural status



The dashboard is not intended to recreate analysis performed in Python. Instead, it operationalizes validated metrics into a repeatable monitoring tool that supports ongoing decision making without re analysis.



A published Tableau Public version is included in this repository.



### **Repository structure**



├── data

│   ├── hospital\_clean\_base.csv

│   ├── df\_drivers.csv

│   ├── tableau\_hospital\_kpis.csv

│   ├── tableau\_bed\_size\_summary.csv

│   ├── tableau\_loss\_driver\_summary.csv

│   └── tableau\_teaching\_rural\_summary.csv

│

├── notebooks

│   ├── 01\_hospital\_financial\_data\_preparation.ipynb

│   ├── 02\_hospital\_margin\_driver\_analysis.ipynb

│   └── 03\_executive\_insights\_and\_recommendations.ipynb

│

├── tableau

│   ├── Tableau\_endtoend.twbx

│   └── tableau\_public\_link.txt

│

├── slides

│   └── Mitigating\_Hospital\_Losses.pptx

│

├── images

│   └── dashboard\_overview.png

│

├── docs

│

└── README.md



### **How to reproduce**



Clone this repository.



Review the notebooks in sequential order:



Data preparation and cleaning



Margin and cost driver analysis



Executive insights and recommendations



Use the cleaned datasets in the data folder to rebuild analysis if needed.



Open the Tableau workbook in the tableau folder or access the published Tableau Public link to explore the interactive dashboard.



Review the executive slide deck in the slides folder for a summary of findings and recommendations.



No proprietary software or credentials are required beyond standard Python libraries and Tableau.

