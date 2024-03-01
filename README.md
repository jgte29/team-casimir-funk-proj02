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

2. Enter API Key: <br>
In order to access the USDA's database, you will need to sign up for an API Key, which you can do using this [link](https://fdc.nal.usda.gov/api-key-signup.html). Once you have one, you will need to enter it when prompted. *See below for example* Alternatively, you can use `DEMO_KEY` for your API key, however, the rate limits are much lower when using this strategy (Hourly Limit: 30 requests per IP address per hour;
Daily Limit: 50 requests per IP address per day). Your can learn more about rate limits [here](https://api.data.gov/docs/developer-manual/).
   ```python
   api_key = 'my_USDA_API_Key_1234' # Enter your API key here

### Notebook Specific Usage Notes:
- nutritional_content.ipynb: <br>
1. `fooddatacentral` & `pint` Packages:
   - If you have never used the `fooddatacentral` & `pint` Packages, you will likely have to `pip` install them. We have provided the code to do so in the notebook. All you have to do is uncomment the code to download such packages. *Recommended* Alternatively, you can download the packages by copying the code below in a terminal.
     - For `fooddatacentral`:
        ```bash
        pip install fooddatacentral
     - For `pint`:
        ```bash
        pip install pint
2.`price_master` Dataset:
- When originally going about our research, we utilized the functions `handle_query_nc_calc` & `compile_ncs` to query the USDA FoodData Central API and pull the requisite nutritional contents for our food products. However, doing so takes a considerable amount of time. Therefore, in order to speed up and faciliate the usage of this notebook, especially when using the widgets in the master notebook, we have provided and read in a `.csv` file called `price_master.csv` that contains all of the information we compiled from the API. If you wish, feel free to run the code that we used to create `price_master.csv` by uncommenting the code in the cell that reads in file. <br>
**Warning:** The code may take up to a couple of minutes to run, so re-comment the code after running it in order to avoid unintentionally re-running it.
   ```python
   price_master = pd.read_csv('./data/price_master.csv', dtype=str)
   
   ### Only uncomment if using, otherwise, DO NOT UNCOMMENT! 
   ### Code takes a lot of time to run and do not want to 
   ### exceed API call rate limits
   # ncs_master = pd.DataFrame()
   # search_col = 'GTIN/UPC'
   # API_KEY = config.API_KEY # Enter your own API Key
   # fp_arr = price_rf[search_col]
   
   # for i in range(len(fp_arr)):
   #     ncs_master = compile_ncs(ncs_master, fp_arr, i, API_KEY)
   
   # price_master = pd.concat([price_rf, ncs_master], axis = 1)
   # price_master = price_master.dropna().reset_index(drop = True)
   # price_master['Vitamin A, RAE'] = price_master['Vitamin A, RAE'] + price_master['Vitamin A, IU']*0.3
   # price_master = price_master.drop(columns = ['Vitamin A, IU'])
