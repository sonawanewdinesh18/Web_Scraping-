# 🏢 AmbitionBox Company Data Scraper

An end-to-end, high-performance web scraping pipeline built in Python to extract structured company information, employee ratings, review counts, salary insights, and location data from **AmbitionBox**, exporting clean datasets directly to CSV.

---

## 🌟 Key Features

- **Modern DOM Parsing**: Fully updated selectors compatible with AmbitionBox's updated BEM class architecture (`companyCardWrapper`, `rating_text`, `companyCardWrapper__ActionWrapper`).
- **Anti-Bot & HTTP 403 Prevention**: Configured with custom browser headers (`User-Agent`, `Accept`, `Referer`) for reliable fetching.
- **High-Performance Scraping**:
  - Utilizes `requests.Session()` for TCP connection pooling.
  - Efficient in-memory list-of-dictionaries data accumulation.
  - Polite scraping delay (`time.sleep`) to prevent IP throttling and rate limits.
- **Fault-Tolerant Extraction**: Safe `try-except` parsing handles missing company fields gracefully.
- **Automated CSV Export**: Exports ready-to-analyze datasets with UTF-8 encoding.

---

## 📊 Extracted Data Schema

| Column Name | Description | Example |
| :--- | :--- | :--- |
| `Company_Name` | Short brand name | `TCS` |
| `Full_Name` | Full registered company name | `Tata Consultancy Services` |
| `Rating` | Overall employee rating (out of 5.0) | `3.2` |
| `Reviews` | Total number of employee reviews | `1.2L` |
| `Salaries` | Total salary entries reported | `10.4L` |
| `Interviews` | Interview experience submissions | `11.4k` |
| `Jobs` | Open job openings listed | `5.3k` |
| `Benefits` | Reported company perks & benefits | `11.1k` |
| `Industry` | Primary industry domain | `IT Services & Consulting` |
| `Headquarters_Locations` | HQ and total location count | `Bengaluru +479 other locations` |
| `Rated_For` | Key highlights (Positive / Critical) | `Promotions, Salary, Work Satisfaction` |
| `Profile_URL` | Direct URL to AmbitionBox company profile | `https://www.ambitionbox.com/overview/tcs-overview` |

---

## 🛠️ Tech Stack & Requirements

- **Language**: Python 3.8+
- **Libraries**:
  - `requests` — HTTP request handling
  - `beautifulsoup4` & `lxml` — HTML parsing
  - `pandas` & `numpy` — Data transformation and CSV export

---

## 🚀 Quick Start & Installation

### 1. Clone the repository
```bash
git clone https://github.com/<your-username>/ambitionbox-web-scraper.git
cd ambitionbox-web-scraper
# Web_Scraping-
