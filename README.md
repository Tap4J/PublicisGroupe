# PublicisGroupe
Assignment for PublicisGroupe

## Guidelines
**Install Libraries from Requirements Using pip**
1. Open your terminal (macOS/Linux) or command prompt (Windows).
2. Navigate to the directory where you have downloaded/cloned the repository.
    ```sh
    cd path/to/your/project
    ```
3. (Optional) Create and activate a virtual environment:
      ```sh
      python3 -m venv env
      source venv/bin/activate
      ```
5. Install the required libraries using `pip`:

    ```sh
    pip install -r requirements.txt
    ```
**Run Jupyter Lab with the Notebook and Data**

To run the Jupyter Notebook with all the data in the GitHub repository, follow these steps:

1. Ensure you are still in the project directory.
2. Start Jupyter Lab:

    ```sh
    jupyter lab
    ```
3. A new tab will open in your default web browser, displaying the Jupyter Lab interface.
4. In Jupyter Lab, navigate to the directory where the notebook file (`.ipynb`) is located.
5. Open the notebook file to begin working with it.


## Assignment explanation

- **Data extraction**: First I needed to download the data from Azure blob storage. For that purpose, I used requests library. I stored dataframes and sas tokens in variables. For plan_data I used plan_df and for post_buy data I used postbuy_df.
- **Data exploration**: Then I explored the data in postbuy_df, check the NaN values, unique values, and missing values.- **Data exploration**: Then I explored the data in postbuy_df, check the NaN values, unique values, and missing values.
- **Data cleaning**: After data exploration, I started to drop the columns. First I needed to remove columns, that have either no use like TagCodes column, or contain too much missing data (Source). Also, I wanted to rid of the data, that have no additional filtering value as they all contained only a single value. I also wanted to remove rows with missing data if there was not much data missing.
-  **Downloading cleaned data**: I stored cleaned data in csv format.
-  **Budget calculation**: The first task was to calculate how much of the budget was spent. 
-  **Performing visualisations**: Using my cleaned dataframe I started to visualise the dataframes. The first visualisation task was to represent the planned budget and realised investments by day. The second task was to represent these values cumulatively and the last task was to calculate ratio between the cumulative planned budget and cumulative realised investments to the last data from postbuy_df
- **Suggestion**: In the last section I tried to suggest other metrics to calculate and visualise interesting data.



