# Web-Scraping-using-Python

This guide demonstrates how to scrape data from a webpage using Python, BeautifulSoup, and requests. We will be scraping the “List of Asian countries by area” from Wikipedia.

Prerequisites

Before you start, ensure you have the following Python libraries installed:
	1.	BeautifulSoup (for parsing HTML)
	2.	requests (for making HTTP requests)
	3.	lxml (for faster parsing with BeautifulSoup)

Install these libraries using pip if you don’t have them already:

pip install beautifulsoup4 requests lxml

Steps Followed 🛠️

1. Imported Required Libraries

from bs4 import BeautifulSoup
import requests



⸻

2. Fetched the Webpage Content

link = 'https://en.wikipedia.org/wiki/List_of_Asian_countries_by_area'
response = requests.get(link)



⸻

3. Parsed the Webpage using BeautifulSoup

soup = BeautifulSoup(response.content, 'lxml')



⸻

4. Printed the Beautiful Soup Object (Prettified)

print(soup.prettify())



⸻

5. Printed the Webpage Title

print(soup.title)
print(soup.title.string)



⸻

6. Found the Required Table

right_table = soup.find('table', class_='wikitable sortable')
right_table



