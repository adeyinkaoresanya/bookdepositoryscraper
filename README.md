# Book Depository Scraper

## Description

The Book Depository Scraper is a Python package application for scraping the Book Depository [website](https://www.bookdepository.com/) based on a specific genre and number of items.

## Tools/Libraries required

* [Python 3.9](https://python.org) : Base programming language for development. The latest version of python.
* sklearn
* pickle
* requests
* flask
  
## Installation

Use the package installer pip to install book scraper.

Install directly from github repository

## Usage

The scraper takes in two arguments---genre and number of items--- returns a dataframe which can be cleaned and converted to CSV.

To collect data without cleaning:

```python
from src.scraper import Scraper

scraper = Scraper("thriller", 300)
df= scraper.scrape_data()
scraper.create_csv(df, "books")
```

To collect clean data:

```python
from src.scraper import Scraper
from src.preprocess import ProcessData

scraper = Scraper("thriller", 300)
df= scraper.scrape_data()
s= ProcessData() 
clean_df= s.clean_dataframe(df_total)
scraper.create_csv(clean_df, "books")

```

## Contribution

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

## License

The MIT License - Copyright (c) 2021 - Adeyinka J. Oresanya
