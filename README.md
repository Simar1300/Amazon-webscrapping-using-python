
Amazon Product Web Scraper
-Overview -This Python-based web scraper extracts product information from Amazon product pages using BeautifulSoup. It gathers key details such as product title, price, rating, number of reviews, and availability, and saves this information into a CSV file for further analysis.

-Features
Scrapes the following product details:
Product Title
Price
Rating
Number of Reviews
Availability
Handles missing data by setting defaults or skipping entries.
Outputs the scraped data into a CSV file (amazon_data.csv).

-Technologies Used
Python 3.x
Libraries:
BeautifulSoup4
requests
pandas
numpy

-Prerequisites
Before you begin, ensure you have met the following requirements:

Python 3.x installed on your machine.
All the required Python libraries. You can install them using the following command:
pip install beautifulsoup4 requests pandas numpy

1)Setup Instructions
Clone the repository:
git clone https://github.com/your-username/amazon-web-scraper.git

2)Navigate to the project directory:
cd amazon-web-scraper

3)Open the Python script or Jupyter notebook to run the scraper.

4)Update your User-Agent:
Modify the HEADERS dictionary in the script with your actual browser's User-Agent string to avoid getting blocked by Amazon's anti-bot mechanisms.
Example- HEADERS = ({
   'User-Agent': 'your-user-agent-string',
   'Accept-Language': 'en-US, en;q=0.5'
})
5)Run the script: Execute the Python script or the Jupyter notebook. It will scrape Amazon product details and save them in a CSV file named amazon_data.csv.

-How It Works
The scraper sends an HTTP GET request to Amazon's website using the requests library, and then parses the returned HTML content using BeautifulSoup. The script extracts links to individual product pages from a search results page. For each product, it fetches and stores data such as the product title, price, rating, number of reviews, and availability in a Pandas DataFrame, which is later exported to a CSV file.

-Functions
get_title(soup): Extracts and returns the product title.
get_price(soup): Extracts and returns the product price. If the price is not available, it tries to find a deal price.
get_rating(soup): Extracts and returns the product rating.
get_review_count(soup): Extracts and returns the number of user reviews.
get_availability(soup): Extracts and returns the availability status of the product.
Output
The scraper saves the extracted data in a CSV file called amazon_data.csv. This CSV file contains the following columns:
title: The title of the product.
price: The price of the product.
rating: The average rating of the product.
reviews: The number of user reviews.
availability: The availability status of the product (e.g., "In stock" or "Not Available").
Example of Extracted Data
title	price	rating	reviews	availability
Sony PlayStation 4	$299.99	4.5	12000	In stock
PS4 Controller	$59.99	4.7	8500	In stock

-Usage
Modify the URL: You can modify the URL variable in the script to target a different product category or specific product search results on Amazon.

Run the script: Execute the script, and it will automatically scrape the data and save it to the amazon_data.csv file.

Analyze the data: Once the data is scraped, you can analyze it using any tool of your choice (e.g., Excel, Pandas, or any data visualization tool).

Disclaimer
This project is for educational purposes only. Scraping Amazon or any other website without permission may violate the terms of service of the website. Please ensure that you comply with the website's robots.txt file and use this scraper responsibly. Use of this tool is at your own risk.



