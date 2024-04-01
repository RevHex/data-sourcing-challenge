# Data Sourcing Challenge
 <b><font size="+1"><font color="#1F5AF5"> Merging NYT and TMBD Data
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
<Summary> <b><font size="+2">  Financial Landscape </font></b> </summary>

<ul>
<li> In general this fintech aims to disrupt and ultimately supplant conventional financial service providers by demonstrating greater agility, catering to an overlooked segment of the population, and delivering swifter/superior service.</li>

<li> Currently, the three most highly valued finanace companies utilizing a.i. are Ant Group, Stripe, and Revolut.</li>
</ul>
</details>

<details> 
<Summary> <b><font size="+2"> Results </font></b> </summary>

<ul>
<li> Providing access to congressioanl investments, exposing trends of insider trading, government contract statements, and providing data sets and api that normally would not be available to the leyman. </li>

<li>Customer acquisition cost, customer lifetime value, and monthly recurring revenue are some of the core metrics used to mesaure companies in this branch of fintech. </li>

<li>Based on the limited resources available for comparison with other competitors in fintech, it appears they rank somewhere in the middle. Keeping in mind that they are a small business with only 15 employees and are not publicly traded. </li>
</ul>
</details>


<details> 
<Summary> <b><font size="+2"> Recommendations </font></b> </summary>

<ul>
<li>If their aim was to attract a broader audience, I would recommend providing their back testing program for free or at an entry-level price, albeit with limited access.</li>

<li>This avenue has the potential to assist individuals with minimal or no investment background in becoming more accustomed to the concept. Expanding the consumer base would directly influence profitability, along with other fundamental metrics in the fintech industry.</li>

<li>There wouldn't be a necessity for new software or hardware as it would leverage existing resources under their ownership and control. My proposal would merely alter the utilization and accessibility of their current programs.</li>
</ul>
</details>

<details> 
<Summary> <b><font size="+2"> Resources </font></b> </summary>

<ul>
<li> https://github.com/kefranabg/readme-md-generator </li>
<li> https://chat.openai.com/ </li>
<li> https://github.com/Babi-B/git-readme-tips?tab=readme-ov-file#styling-text </li>
<li> https://shields.io/ </li>
<li> https://www.quiverquant.com/blog/ </li>
<li> https://bullishbears.com/quiver-quantitative-review/ </li>
</ul>
</details>
