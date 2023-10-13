# nosql-challenge
Module 12 challenge
# Background of the Analysis:

This project included 3 parts:

**Part 1: Database and Jupyter Notebook Set Up**
1. Import the data provided in the establishments.json file from your Terminal. Name the database uk_food and the collection establishments.
2. Import relevant libraries.
3. Create an instance of the Mongo Client.
4. To ensure the database has been created and data has been loaded correctly,\
       - List the database and confirm that "uk_food" is listed.\
       - List the collection(s) and confirm that "establishments" exist.\
       - Display one document.
6. Assign the collection(s) to a variable.

**Part 2: Update the Database**
1. Adding a new restaurant to the database.
2. Find the "BusinessTypeID" for "Restaurant/Cafe/Canteen" and return only the "BusinessTypeID" and "BusinessType" fields.
3. Update the new restaurant with the "BusinessTypeID" found.
4. The magazine is not interested in any establishments in Dover, so check how many documents contain the Dover Local Authority. Then, remove any establishments within the Dover Local Authority from the database, and check the number of documents to ensure they were deleted.
5. In the data, there are some number values that are currently stored as strings and change datatype:\
       - Convert latitude and longitude to decimal numbers.\
       - Convert RatingValue to integer numbers.

**Part 3: Exploratory Analysis**
1. Which establishments have a hygiene score equal to 20?
2. Which establishments in London have a RatingValue greater than or equal to 4?
      - **_Note_**: The London Local Authority has a longer name than "London" so need to use $regex as part of search.
4. What are the top 5 establishments with a RatingValue of 5, sorted by lowest hygiene score, nearest to the new restaurant added, "Penang Flavours"?
      - **_Note_**: Need to compare the geocode to find the nearest locations. Search within 0.01 degree on either side of the latitude and longitude.
5. How many establishments in each Local Authority area have a hygiene score of 0? Sort the results from highest to lowest, and print out the top ten local authority areas.
      - **_Note_**: Need to use the aggregation method to answer this. 
        
**The first 5 rows of the resulting DataFrame look like this:**\
![image](https://github.com/lakigit/nosql-challenge/assets/138610916/9b3e184a-7389-431d-9aa0-b292df44260e)

# Code Files:
- [NoSQL_setup.ipynb](https://github.com/lakigit/nosql-challenge/blob/main/NoSQL_setup.ipynb)
- [NoSQL_analysis.ipynb](https://github.com/lakigit/nosql-challenge/blob/main/NoSQL_analysis.ipynb)
       
