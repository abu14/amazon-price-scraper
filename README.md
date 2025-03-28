# 📦 🕷️ **Amazon Product Scraper**
![GitHub contributors](https://img.shields.io/github/contributors/abu14/amazon-price-scraper)
![GitHub forks](https://img.shields.io/github/forks/abu14/amazon-price-scraper)
![GitHub stars](https://img.shields.io/github/stars/abu14/amazon-price-scraper)
![GitHub issues](https://img.shields.io/github/issues/abu14/amazon-price-scraper)
![GitHub license](https://img.shields.io/github/license/abu14/amazon-price-scraper)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue)](https://www.linkedin.com/in/abenezer-tesfaye-191579214/)


This project contains a Scrapy spider (`amazonspider.py`) designed to scrape product information from Amazon based on a specified keyword. By default, it is configured to scrape data for 'pendrive', collecting details such as name, price, brand, memory, hardware interface, special features, and read speed from product pages. The spider uses the ScrapeOps proxy service to manage requests and avoid being blocked by Amazon.

### 📋 **Prerequisites**

Before You begin, ensure you have the following set-up:

  - **Python 3.6+**
  - **virtualenv** 
  - **Scrapy 2.5+**
  - **ScrapeOps API key** :- sign up at [ScrapeOps](https://scrapeops.io/)


### ⚙️ **Setup Instructions**

Follow these steps to set up the project on your local machine:

1. **Clone the repository:**
   ```bash
   git clone https://github.com/abu14/amazon-price-scraper.git
   cd amazon-price-scraper
   ```
2. **Create and activate a virtual environment:**
    ```bash
    python -m venv .amzenv
    .amzenv\Scripts\activate  # On Windows
    source .amzenv/bin/activate  # On macOS/Linux
    ```
3. **Install dependencies:**
   ```bash
     pip install scrapy python-dotenv
   ```
4. **Configure the ScrapeOps API key:**
    ```bash
    API_KEY=your_scrapeops_api_key
    ```

6. **Verify the project structure:**
  - Ensure that ```amazonspider.py``` is placed inside ```amazon_scraper/amazon_scraper/spiders/```

### 🗂️ **Project Structure**
  ```bash
    amazon-product-scraper/
    │
    ├── spiders/
    │   └── amazon_spider.py
    ├── items.py
    ├── pipelines.py
    ├── settings.py
    │
    ├── .env
    ├── scrapy.cfg
    └── README.md
  ```

### 🕷️ **Running the Spider**
To run the spider, navigate to the amazon_scraper directory and execute:
  ```bash
    scrapy crawl amazonspider
  ```
  **Sample Output:**
  ```json
    [
  {
    "name": "SanDisk 128GB Ultra Flair USB 3.0 Flash Drive",
    "price": "15.99",
    "brand": "SanDisk",
    "memory": "128 GB",
    "hard_interface": "USB 3.0",
    "special_feature": "High Speed",
    "read_speed": "150 Megabytes Per Second"
  },
  ]
  ```

### ⚠️ **Disclaimer**
This project is for educational purposes only. Scraping Amazon may violate their terms of service. Use at your own risk and ensure compliance with applicable laws and policies.

### 📜 **License**
This project is licensed under the MIT License. See [LICENSE](./LICENSE) file for more details.


### **Contact**

##### Abenezer Tesfaye

⭐️ Email - tesfayeabenezer64@gmail.com
