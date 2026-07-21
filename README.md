# Python Web Scraper

A step-by-step web scraping tutorial and tool built with **Requests** and **BeautifulSoup**, demonstrating the full pipeline from sending HTTP requests to extracting structured data and saving it as CSV. Uses [books.toscrape.com](https://books.toscrape.com/) — a sandbox site built for scraping practice — as the target.

## 🎯 What it does

Scrapes book listings (title, price, rating, and other details) across multiple paginated pages and saves the structured results into a CSV file.

## 📁 Notebook

[`notebooks/book_scraper_beautifulsoup.ipynb`](notebooks/book_scraper_beautifulsoup.ipynb)

## 🔍 Workflow Covered

1. **Import libraries** — `requests`, `BeautifulSoup`, `pandas`, `re`, `os`
2. **Send HTTP request** — fetch a target webpage with proper headers and error handling (`raise_for_status`)
3. **Parse HTML** — using BeautifulSoup's `html.parser` to navigate the page structure
4. **Locate elements** — selecting containers and fields using tags, classes, and CSS selectors (`select`, `select_one`, `find_all`)
5. **Extract & clean data** — pulling titles, prices, and ratings; cleaning text with regex (e.g. stripping currency symbols)
6. **Save to CSV** — converting scraped rows into a Pandas DataFrame and exporting
7. **Scale across pages** — looping through all paginated pages (1–50) to scrape the full catalogue, with directory handling via `os.makedirs`

## 🛠️ Tech Stack

- **Python 3**
- **Requests** — sending HTTP requests
- **BeautifulSoup (bs4)** — HTML parsing and element selection
- **Pandas** — structuring and exporting scraped data
- **re** — text cleaning with regular expressions

## 🚀 Getting Started

1. Clone the repository:
   ```bash
   git clone https://github.com/<your-username>/python-web-scraper.git
   cd python-web-scraper
   ```

2. Install dependencies:
   ```bash
   pip install requests beautifulsoup4 pandas jupyter
   ```

3. Launch Jupyter and open the notebook:
   ```bash
   jupyter notebook
   ```

> **Note:** This scraper targets [books.toscrape.com](https://books.toscrape.com/), a website built specifically for scraping practice. If adapting this for another site, always check that site's `robots.txt` and terms of service before scraping.

## ⚠️ Disclaimer

Web scraping should always respect a website's `robots.txt`, terms of service, and applicable laws. This project is for educational purposes, using a site explicitly designed for scraping practice.

## 📄 License

This project is open source and available under the [MIT License](LICENSE).
