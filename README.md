# Company URL Scraper

This script scrapes URLs for a list of company names from DuckDuckGo search results. It reads a CSV file containing company names, processes them, and outputs the first URL found for each company. The script uses the `requests` library for HTTP requests and `BeautifulSoup` for HTML parsing.

## Features

- **Cleans** and processes company names to remove unwanted symbols.
- **Randomizes User-Agent headers** to mimic human-like requests and avoid getting blocked.
- **Adds delay between requests** to avoid being flagged by DuckDuckGo.
- Outputs the URLs directly to the console.

## Prerequisites

- **Python 3.x**
- Required Python libraries:
  - `pandas`
  - `requests`
  - `beautifulsoup4`

## Usage

- Modify the File Path:
- Update the file path in the code:
df = pd.read_csv('path to your csv file')
- Run the Script:
python scraper.py
- Check the Output: The script will print each company name along with the first URL found from DuckDuckGo. Example output:
- Company: Facebook
 URL: https://www.facebook.com
- Company: Google
 URL: https://www.google.com

## Code Explanation

- Data Loading: The script reads the CSV file containing company names.
- Data Cleaning: It removes any special characters and non-UTF8 symbols from company names using regex.
- Web Scraping: A scrape function is defined to make HTTP requests to DuckDuckGo’s HTML interface.
- A random User-Agent header is selected for each request to reduce the risk of being blocked.
- BeautifulSoup parses the HTML response, extracting the first link that matches the result__a class, which represents search result links.
- Delay Between Requests: The script introduces a random delay between 5-12 seconds after each request to avoid overwhelming the search engine.

## Disclaimer

- This is just a project to explore the limitations of the anti scrapinng mechanisms of most search engines, ethically and legally webscraping can have consequences, I don't encourage webscraping in any form, this whole respository is simply for information purposes only.

