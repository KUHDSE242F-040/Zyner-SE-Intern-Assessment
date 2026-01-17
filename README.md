# Zyner-SE-Intern-Assessment
Zyner | SE Intern Assessment python 
README: Y Combinator Startup Directory Scraper
Project Overview
This project scrapes approximately 500 startups from the Y Combinator (YC) startup directory (https://www.ycombinator.com/companies) to extract key information for analysis. The scraper collects company names, batch information, descriptions, founder names, and founder LinkedIn URLs.

How It Works
The scraper operates in four main phases:

Initial Loading: Opens the YC companies directory and scrolls dynamically to load enough companies until reaching the target count of 500.
List Parsing: Extracts basic information from the company cards on the main directory page, including company names, URLs, and short descriptions.
Detailed Scraping: Visits each company's individual profile page to collect additional details:
Batch information (e.g., "W24", "S23")
Founder names
Founder LinkedIn URLs
Data Export: Saves all collected data to a CSV file named "yc_startups_500.csv".
Dependencies
Python 3.7+
Playwright (async version)
Pandas
Asyncio
Setup Instructions
Clone or download this repository
Install the required dependencies:

pip install playwright pandas
Install Playwright browsers:

playwright install
Running the Scraper
Execute the script with:


python yc_scraper.py
The script will:

Launch a Chromium browser (visible by default)
Scroll through the YC directory to load companies
Scrape detailed information for each company
Save the results to "yc_startups_500.csv"
Data Collected
For each startup, the following data points are collected:

Company Name
URL
Short Description
Batch (YC batch, e.g., "Winter 2024")
Founder Name(s)
Founder LinkedIn URL(s)
Challenges & Limitations
YC uses dynamic loading with hashed class names, requiring structural/attribute-based selectors
Founder information extraction is complex due to varying page layouts
Rate limiting was implemented to avoid overloading the YC servers
Some data fields may be incomplete if the structure changes
Submission Package
For this assignment, you should submit:

CSV File: "yc_startups_500.csv" containing the scraped data
Python Script: The scraper code file (yc_scraper.py)
Brief Summary: A 2-3 sentence explanation of your approach (can be included in a separate text file or as a comment in the code)

