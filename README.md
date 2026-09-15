# 🌊 CalCOFI Climate Change Tracker: 70-Year Ocean Temperature Analysis

> An exploratory data analysis investigating seven decades of oceanographic observations off the coast of California (1949–2021).

---

## 🌱 Project Background

I first discovered this dataset during one of my university subject assessments. While the original assignment gave me a first look at the data, it sparked my genuine curiosity about how the Pacific Ocean has actually changed over the decades. 

This repository is my independent self-continuation of that university project, taking the analysis much further with custom regional filtering, continuous monthly time-series resampling, interactive geographic mapping, and a focused investigation into 70+ years of ocean climate signals.

---

## 📖 The Story Behind the Data

In the late 1940s, the bustling sardine canning industry along California's coast—immortalized in John Steinbeck's novel *Cannery Row*—suddenly collapsed. Millions of fish vanished almost overnight, devastating local coastal communities. 

Desperate for answers, fisheries scientists and oceanographers banded together in **1949** to launch the **California Cooperative Oceanic Fisheries Investigations (CalCOFI)**. Their mission was simple: sail out into the Pacific on research vessels, stop at predetermined coordinates ("stations"), and lower specialized brass water-sampling bottles hundreds of meters down into the ocean.

Scientists measured the water temperature, salinity, oxygen levels, and chemistry at every stop. 

**They never stopped collecting data.**

More than **70 years later**, CalCOFI has become the longest continuous ocean observation program on the planet. While scientists originally set out looking for sardines, they inadvertently created an irreplaceable historical record of our changing planet.

---

## 🎯 What I Wanted to Find Out

The world's oceans absorb more than **90% of the excess heat** trapped by greenhouse gases. If our climate is changing, the oceans will show it first.

Using over **895,000 water samples** collected across **35,000+ research stations**, I wanted to answer four fundamental questions in plain, practical terms:

1. **Is the ocean surface actually warming?** If so, by how much over seven decades?
2. **What does the natural seasonal cycle look like?** When is the Pacific coldest, and when does it reach peak warmth?
3. **How deep does ocean warmth go?** How quickly does surface warmth disappear as you dive into the deep sea?
4. **Which years were the most extreme?** What were the warmest and coldest years ever recorded in California waters?

---

## 🔍 Key Findings

### 1. The Ocean Has Consistently Warmed (+0.69°C / +1.25°F)
By calculating the annual average surface temperature across every full calendar year from 1949 to 2020, I found a steady upward trend:
* Surface waters off Southern California have warmed at an average rate of **+0.10°C per decade**.
* In total, the surface ocean has warmed by approximately **+0.69°C (+1.25°F)** since Harry Truman was president.
* While one degree might sound small for air temperature on land, heating millions of cubic miles of dense seawater takes an astronomical amount of energy.

### 2. February is Coldest, September is Warmest
Ocean temperatures do not peak in July when the sun is highest in the sky:
* 🔵 **Coldest Month:** **February (~14.7°C / 58.4°F)**, reaching its seasonal low in late winter.
* 🔴 **Warmest Month:** **September (~17.8°C / 64.0°F)**. Because water has a very high heat capacity, it takes months of summer sunlight to warm up the ocean surface—a phenomenon known as *seasonal thermal lag*.

### 3. Surface Heat is Only Skin-Deep
Analyzing water samples down to 500 meters reveals how ocean depth acts as a natural buffer:
* **Surface (0–10m):** Averages ~16°C (61°F).
* **100 meters down:** Temperatures drop steeply to ~10°C (50°F).
* **500 meters down:** Sunlight cannot penetrate, and water hovers near a chilly **6°C (43°F)** year-round, unaffected by summer heat or winter cold.

### 4. Marine Heatwaves Leave Huge Fingerprints
The warmest years in the 70-year record correspond directly to major climate anomalies:
* **1977, 1973, 2015, 1983, and 2014** were the warmest on record, averaging between **17.2°C and 18.2°C**.
* The 2014–2015 spike corresponds to the notorious **Pacific "Blob"**, an unprecedented marine heatwave that disrupted California kelp forests and shifted marine life hundreds of miles north.

---

## 🗺️ Interactive Station Map

To understand where the data came from, I plotted the coordinates of research stations off Southern California. The notebook includes an interactive map created with `plotly` that allows you to zoom in, pan, and hover over individual research stops to view historical dates and temperatures.

---

## 📂 Project Structure

```text
calcofi-climate-change-tracker/
├── data/
│   ├── 194903-202105_Bottle.csv                     # 895,000+ water sample measurements
│   ├── 194903-202105_Cast.csv                       # 35,000+ research vessel station locations & dates
│   └── CalCOFI Database Tables Description...pdf   # Official data dictionary & code manual
├── notebooks/
│   └── calcofi_climate_change_tracker.ipynb         # Main step-by-step analysis notebook
├── output.png                                       # Exported seasonal temperature chart
├── requirements.txt                                 # Pinned Python dependencies
└── README.md                                        # Project overview & story
```

---

## 🚀 How to Run the Project Locally

### 1. Clone the repository
```bash
git clone https://github.com/linnthantsoewai/calcofi-climate-change-tracker.git
cd calcofi-climate-change-tracker
```

### 2. Set up a virtual environment
```bash
python3 -m venv .venv
source .venv/bin/activate
```

### 3. Install required libraries
```bash
pip install -r requirements.txt
```

### 4. Launch the notebook
```bash
jupyter notebook notebooks/calcofi_climate_change_tracker.ipynb
```

---

## 🛠️ Tools Used
* **Python 3**
* **Pandas:** Tabular data cleaning, merging, and monthly time-series resampling.
* **NumPy:** Numerical modeling and linear trendline calculation.
* **Matplotlib & Seaborn:** Statistical visualizations and seasonal profiles.
* **Plotly Express:** Interactive geographic mapping of offshore research stations.
