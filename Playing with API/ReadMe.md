# Goal of the project :
The goal of this project is to interact with an API to collect historical data on cryptocurrencies, specifically focusing on the top coins by market cap, and to convert this data into a structured, human-readable format that includes daily open, high, low, and close prices. The final processed data is then stored locally in a JSON file, 
which could be used for further financial analysis, reporting, or integration into other systems.<br>
<b>Fetching Initial Data:</b><br>

The script makes an HTTP GET request to CoinGecko's API to fetch the top 250 cryptocurrencies by market capitalization, priced in USD.<br>
It prints the status of the request and the response data to verify the connection and data retrieval.<br>
The response is parsed to JSON, and the first ten cryptocurrencies are selected for further processing.<br>
<br>
<b>Processing Specific Cryptocurrency Data:</b><br>

The code identifies the 'id' of the first cryptocurrency (Bitcoin) from the fetched list and requests its historical OHLC data for the past 365 days.<br>
This data is then processed to convert Unix timestamps into human-readable dates.<br>
<br>
<b>Generalizing the Process for Multiple Coins:</b><br>

The code iterates over the list of the first ten cryptocurrencies.<br>
For each cryptocurrency, it fetches the historical OHLC data from the past year.<br>
Each data point (Unix timestamp) is converted into a human-readable date format.<br>
The processed data for each coin is organized in a dictionary where each key is a date, and the value is a list of OHLC prices.<br>
<br>
<b>Error Handling:</b><br>

The script includes error handling to manage potential issues with the API requests, such as connection errors or data fetching issues, and prints a message if an error occurs.<br>
<br>
<b>Saving Data Locally:</b><br>

After processing the data for all selected coins, the script saves the structured data into a local JSON file (crypto_data.json). This file organizes the data by cryptocurrency and date, making it easily accessible for future use.<br>
<br>
<b>Data Structure and Output:</b><br>

The output crypto_data dictionary is structured so that each cryptocurrency's historical data can be accessed by its ID, with each date pointing to the corresponding OHLC values.<br>
The script finally writes this structured dictionary to a JSON file, ensuring the data is persistent for future analysis or reporting.<br>
