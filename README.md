# EEP 153 Spring 2024 - Project 02 (Team Casimir Funk)

## Team Members
Jordan Taqi-Eddin - jgte29@berkeley.edu

Khadija Arslan - khadija2002@berkeley.edu

Xiang Wu - xiangwu@berkeley.edu

Yingyin Li - yingyinli2001@berkeley.edu

Marc Bonnot - mpb0614@berkeley.edu

Jane Wang - janeyjwang@berkeley.edu

## Welcome

Welcome to the Project 02 GitHub Repository for Team Casimir Funk. Our code for the project is organized in the following format:
- master_notebook.ipynb: In this notebook, we compile all of the finished products of code for this project and have interactive widgets that allow a user to use various functions we developed for the project.
- dietary_references.ipynb: In this notebook, we create our dietary reference intakes functions.
- nutritional_content.ipynb: In this notebook, we create our nutritional content functions. Moreover, we add the nutritional data to our food prices dataset.
- food_prices.ipynb: This is a supplementary notebook that has select visualizations of price data at different stores.
- food_price_vs_stores.ipynb: This is a supplementary notebook that has select visualizations comparing price data across stores in our analysis.

## How to Use

1. Clone the repository:

   ```bash
   git clone https://github.com/jgte29/team-casimir-funk-proj02.git

2. Enter API Key:
In order to access the USDA's database, you will need to sign up for an API Key, which you can do using this [link](https://fdc.nal.usda.gov/api-key-signup.html). Once you have one, replace the elipses below with your key. Alternatively, you can use `DEMO_KEY` for your API key, however, the rate limits are much lower when using this strategy (Hourly Limit: 30 requests per IP address per hour;
Daily Limit: 50 requests per IP address per day). Your can learn more about rate limits [here](https://api.data.gov/docs/developer-manual/).
   ```python
   print('Hello World')
