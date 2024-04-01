# Data Sourcing Challenge
 <b><font size="+1"><font color="#1F5AF5"> Merging New York Times and The Movie Database
 </font></b>

![Static Badge](https://img.shields.io/badge/Merge%20-%20%23FFD150?style=plastic&label=Data&labelColor=%23000000)


<details> 
<Summary> <b><font size="+2"> Access the New York Times API </font></b> </summary>
<ul>
<li> query_url is correctly constructed </li>
<li> An empty list reviews_list is created </li>
<li> A for loop is created to loop through 20 times</li>
<li> The query_url is extended to include a page</li>
<li> A GET request is made to retrieve results and the JSON data is stored in a variable called reviews</li>
<li> A 12-second interval is used between queries</li>
<li> A try-except clause is used</li>
<li> Inside the try clause, there is a loop to loop through the reviews["response"]["docs"] list</li>
<li> The reviews results are correctly appended to reviews_list</li>
<li> The query page number is printed</li>
<li> The except clause prints out the page number that had no results, then breaks from the loop</li>
<li> json.dumps with the argument indent=4 is used to preview the first five results</li>
<li> reviews_list is converted to a Pandas DataFrame using json_normalize()</li>
<li> The title is extracted from the "headline.main" column and is saved in a new column "title"</li>
<li> The "keywords" column is correctly converted to string data using the supplied extract_keywords function</li>
<li>  list called titles is created from the "title" column using to_list()</li>

</ul>
</details>

<details> 
<Summary> <b><font size="+2"> Access The Movie Database API </font></b> </summary>

<ul>
<li> An empty list called tmdb_movies_list is created</li>
<li> A variable called request_counter is created and assigned the value of 1</li>
<li> A for loop is created to loop through the titles list</li>
<li> request_counter is incremented by 1 </li>
<li> time.sleep(1) when request_counter reaches a multiple of 50</li>
<li> A GET request that sends the title to The Movie Database search is performed, and the JSON results are retrieved</li>
<li> A try-except clause is used</li>
<li> The except clause prints out a statement if a movie is not found</li>
<li> The movie ID is collected from the first result and saved as a variable</li>
<li> A GET request is made using the movie query URL and movie ID to retrieve the full movie details in JSON format</li>
<li> The genre names are extracted from the results into a list called genres</li>
<li> The spoken_languages' English names are extracted from the results into a list called spoken_languages</li>
<li> The production_countries' names are extracted from the results into a list called production_countries</li>
<li> A dictionary is created with the specified 15 fields</li>
<li> The results dictionary is appended to the tmdb_movies_list list</li>
<li> A message is printed with the name of the movie to indicate that the title was found</li>
<li> The first five results are previewed using json.dumps with the argument indent=4</li>
<li> The results are converted to a DataFrame called tmdb_df with pd.DataFrame()</li>
</ul>
</details>

<details> 
<Summary> <b><font size="+2">  Merge and Clean the Data for Export </font></b> </summary>

<ul>
<li> The New York Times reviews and TMDB DataFrames are merged on the title column </li>
<li> A list called columns_to_fix is created to store the names of the genres, spoken_languages, and production_countries columns </li>
<li> A list is created called characters_to_remove containing [, ], and ' </li>
<li> A for loop is created to loop through columns_to_fix </li>
<li> The columns to fix are converted to the string data type</li>
<li> characters_to_remove is looped through to remove the characters from the string using the Pandas str.replace() method</li>
<li> The head of the updated DataFrame is displayed to confirm the list characters were removed</li>
<li> The byline.person column is dropped</li>
<li> Duplicate rows are deleted </li>
<li> The DataFrame index is reset</li>
<li> The DataFrame is exported to a CSV file without the index </li>
</ul>
</details>

