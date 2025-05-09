# Car Brand Analysis in Forums

## Project Overview
This project scrapes and analyzes car-related discussions from online forums to understand brand relationships, mentions, and associated attributes. It focuses on entry-level luxury performance sedans, extracting meaningful insights about how different car brands are discussed in relation to each other and what attributes are commonly associated with top brands.

## Features
- Web scraping of car forum discussions
- Brand and model identification in forum messages
- Co-occurrence analysis of car brands
- Brand relationship visualization using Multidimensional Scaling (MDS)
- Attribute analysis for top car brands

## Technologies Used
- Python 3.x
- BeautifulSoup4 for web scraping
- Pandas for data manipulation
- Scikit-learn for MDS analysis
- Matplotlib for visualization
- Requests for HTTP requests
- Numpy for numerical operations

## Installation

```bash
# Clone this repository
git clone https://github.com/yourusername/car-brand-analysis.git
cd car-brand-analysis

# Install dependencies
pip install -r requirements.txt
```

## Usage

### 1. Web Scraping
The script scrapes car forum discussions from Edmunds.com:

```python
python scrape_forums.py
```

This will:
- Collect author information, dates, and message content
- Save the data to `comments.csv`
- Implement polite scraping with retry logic and delays

### 2. Data Analysis
Run the analysis script to process the scraped data:

```python
python analyze_brands.py
```

This will:
- Identify car brands and models mentioned in each message
- Calculate brand mention frequencies
- Generate co-occurrence matrices
- Calculate lift ratios between brands
- Create MDS visualizations of brand relationships
- Analyze attributes associated with top brands

## Data Files
- `Car_Models_Assignment_1_Data.csv`: Contains mapping of car models to their brands
- `comments.csv`: Scraped forum data with user IDs, dates, and messages

## Key Insights

### Brand Co-occurrence
The project analyzes which brands are frequently mentioned together in discussions, calculating lift ratios to understand the strength of these relationships.

### Brand Positioning Map
Using MDS (Multidimensional Scaling), the project creates a visual representation of how brands relate to each other in the forum discussions.

### Brand Attributes
For the top 5 most mentioned brands, the project identifies commonly associated attributes such as:
- Performance (acceleration, speed, horsepower)
- Comfort (seating, interior, ride quality)
- Reliability (durability, maintenance issues)
- Price (cost, value, affordability)
- Fuel efficiency (mpg, gas mileage)

## Output Examples

### Frequency Analysis
```
Top 10 Brands by Frequency:
brand1    XXX
brand2    XXX
...
```

### Attribute-Brand Association
```
Brand to Attribute Frequency Table:
             performance  comfort  reliability  price  fuel efficiency
brand1              XXX      XXX          XXX    XXX              XXX
brand2              XXX      XXX          XXX    XXX              XXX
...
```

## Executive Summary
From analyzing the forum, we see high association between Honda and Toyota (and Nissan). In comments where Toyota is mentioned with another brand, it is most likely to be Honda (or Nissan) and vice versa. As these brands are Japanese, this relationship is intuitive and is visualized in the MDS map with Toyota and Honda positioned close to each other. Both brands rank highly in terms of brands most discussed, with Honda in the top 5. This frequent mention in discussions about entry-level luxury performance sedans indicates strong brand relevancy.

## License
[Insert your chosen license here]

## Contact
[Your contact information]
