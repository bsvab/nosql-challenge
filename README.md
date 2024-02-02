# Module 12 Challenge

## <p style="color:#CC6600">Background / Scenario</p> 

The UK Food Standards Agency evaluates various establishments across the United Kingdom, and gives them a food hygiene rating. You've been contracted by the editors of a food magazine, Eat Safe, Love, to evaluate some of the ratings data in order to help their journalists and food critics decide where to focus future articles.

## <p style="color:#CC6600">Part 1: Database Setup</p> 

- Using Terminal commands, a MongoDB database called `uk_food` and a collection called `establishments` were created.
- The data provided in the establishments.json file was then imported via Terminal.
- Within a Jupyter notebook, dependencies are imported, then an instance of the Mongo Client is established.
- The establishments collection was assigned to a variable to prepare the collection for use.
<br>

## <p style="color:#CC6600">Part 2: Update the Database</p> 

The magazine editors have some requested modifications for the database before you can perform any queries or analysis for them. The following changes to the establishments collection were incorporated:
- A new restaurant called 'Penang Flavours' is added to the database, and its business type ID is corrected.
- The magazine is not interested in any establishments in Dover, so all documents that contain the Dover Local Authority were removed.
- Corrections were made on number values that were stored as strings to update them to the correct data types.
<br>

## <p style="color:#CC6600">Part 2: Exploratory Analysis</p> 

Eat Safe, Love has specific questions they want you to answer, which will help them find the locations they wish to visit and avoid.

The following qustions are answered via providing filtered dataframes displaying the relevant information:
- Which establishments have a hygiene score equal to 20?
- Which establishments in London have a RatingValue greater than or equal to 4?
- What are the top 5 establishments with a RatingValue of 5, sorted by lowest hygiene score, nearest to the new restaurant added, "Penang Flavours"?
- How many establishments in each Local Authority area have a hygiene score of 0? Sort the results from highest to lowest, and print out the top ten local authority areas.
<br>

## <p style="color:#CC6600">References</p>

[UK Food Standards Agency](https://www.food.gov.uk/) (2022). UK food hygiene rating data API. https://ratings.food.gov.uk/open-data/en-GB. Contains public sector information licensed under the [Open Government Licence v3.0](https://www.nationalarchives.gov.uk/doc/open-government-licence/version/3/).  
Accessed Sept 9, 2022 and Sept 12, 2022 with the establishment settings as follows: longitude=51.5072, latitude=-0.1276, maxdistancelimit=4567, pagesize=10000, sortoptionkey=distance, pagenumber=(1,2,3,4,5,6,7,8). 
<br>
<br>
<br>
![UTlogo](images/utaustin-mccombs.png)      <img src="images/edx-logo-elm.svg" width="200" height="80"> 