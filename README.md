# Valorant Agent Analytics Pipeline

A full-stack data engineering and analytics pipeline designed to extract, process, and visualize competitive Valorant gameplay data. 

This project bypasses static datasets by utilizing a custom multi-threaded web scraper to pull live player and agent statistics from [vlr.gg](https://www.vlr.gg/) and [blitz.gg](https://blitz.gg/). The data is then cleaned, transformed, and visualized to uncover statistical disparities in agent performance across different competitive tiers (e.g., Gold vs. Radiant).

## 🚀 Technical Architecture
* **Data Extraction (Scraping):** Built a custom Python scraper using `Requests`, `BeautifulSoup`, and `lxml` to parse unstructured HTML tables.
* **Concurrency:** Implemented `concurrent.futures.ThreadPoolExecutor` to allow for multi-threaded data collection, drastically reducing scraping time while utilizing randomized time delays to respect server rate limits.
* **Data Transformation:** Utilized `Pandas` to clean scraped data, handle missing values, cast data types (e.g., converting percentage strings to floats), and merge distinct datasets.
* **Data Visualization:** Designed comparative analytical dashboards using `Matplotlib` to visualize complex metrics like ACS (Average Combat Score), K/D ratios, and win rates across competitive ranks.

## 📊 Key Analytics & Features
* **Tier-Based Meta Analysis:** Comparative visualizations highlighting how agent pick rates and win rates shift between mid-tier (Gold) and elite-tier (Radiant) lobbies.
* **Professional Roster Scraping:** Automated aggregation of professional player statistics (e.g., Sentinels roster) to analyze professional-level agent utilization and combat scores.
* **Automated CSV Generation:** Dynamically generates and appends structured datasets (`gold.csv`, `radiant.csv`, `sentinels.csv`) directly from web sources.

## 🛠️ Tech Stack
* **Language:** Python 3
* **Libraries:** `pandas`, `requests`, `beautifulsoup4`, `lxml`, `matplotlib`, `concurrent.futures`, `logging`

## ⚙️ How to Run Locally
1. Clone the repository:
   ```bash
   git clone [https://github.com/khfong26/Valorant-Agent-Analysis.git](https://github.com/khfong26/Valorant-Agent-Analysis.git)
   cd Valorant-Agent-Analysis
