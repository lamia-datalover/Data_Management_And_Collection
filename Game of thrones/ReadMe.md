# Goal of this mini-project :
The provided code demonstrates how to fetch and manipulate data from an external API, specifically the "An API of Ice and Fire" which provides data related to the "Game of Thrones" series. 
Here's a breakdown of what each segment of the code does:<br>
<b>Import Libraries:</b><br>

<b>requests:</b> Used for making HTTP requests to the API.<br>
<b>pandas:</b> Used for data manipulation and analysis.<br>
<b>json:</b> Used for encoding and decoding JSON data, although it's not explicitly used in the snippets shown because requests handles JSON.<br>
<br>
<b>Fetch Data:</b><br>

A HTTP GET request is made to fetch data for a specific character (character ID 2) from the API.<br>
The content of the response is printed (r.content), which shows the raw JSON response.<br>
The JSON data is then extracted using r.json() which parses the JSON response into a Python dictionary.<br>
<br>
<b>Extract and Print JSON Keys:</b><br>

Another request is made to the same character endpoint to ensure fresh data.<br>
The keys of the JSON response are extracted and printed. This step is essential for understanding the structure of the data, which informs how to structure the DataFrame.<br>
<br>
<b>Create DataFrame:</b><br>

A pandas DataFrame data is created with columns corresponding to the keys extracted from the JSON data of character ID 2. This prepares a structured format to store similar data from subsequent API calls.<br>
<br>
<b>Iterate Over Multiple Characters:</b><br>

A loop runs from 1 to 150, making a separate API request for each character ID.<br>
Each character's data is fetched, converted into JSON, and appended to the DataFrame data.<br>
A print statement confirms the completion of data fetching for each character.<br>
<br>
<b>Final Data Inspection:</b><br>

After all characters (1 to 150) are processed, the first few rows of the DataFrame are displayed using data.head() to inspect the collected data.<br>


# Big thanks to Jedha for this project .
