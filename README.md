# nosql-challenge

## Instructions
> The UK Food Standards Agency evaluates various establishments across the United Kingdom, and gives them a food hygiene rating. You've been contracted by the editors of a food magazine, Eat Safe, Love, to evaluate some of the ratings data in order to help their journalists and food critics decide where to focus future articles.
### Part 1: Database and Jupyter Notebook Set Up
> Use `NoSQL_setup_starter.ipynb` for this section of the challenge.
1. Import the data provided in the `establishments.json` file from your Terminal. Name the database `uk_food` and the collection `establishments`.
2. Within your notebook, import the libraries you need: PyMongo and Pretty Print (`pprint`).
3. Create an instance of the Mongo Client.
4. Confirm that you created the database and loaded the data properly:
5. Assign the `establishments` collection to a variable to prepare the collection for use.
### Part 2: Update the Database
> Use `NoSQL_setup_starter.ipynb` for this section of the challenge.
Make the following changes to the `establishments` collection:
1. Add the following information to the database:
   ```
   {
    "BusinessName":"Penang Flavours",
    "BusinessType":"Restaurant/Cafe/Canteen",
    "BusinessTypeID":"",
    "AddressLine1":"Penang Flavours",
    "AddressLine2":"146A Plumstead Rd",
    "AddressLine3":"London",
    "AddressLine4":"",
    "PostCode":"SE18 7DY",
    "Phone":"",
    "LocalAuthorityCode":"511",
    "LocalAuthorityName":"Greenwich",
    "LocalAuthorityWebSite":"http://www.royalgreenwich.gov.uk",
    "LocalAuthorityEmailAddress":"health@royalgreenwich.gov.uk",
    "scores":{
        "Hygiene":"",
        "Structural":"",
        "ConfidenceInManagement":""
    },
    "SchemeType":"FHRS",
    "geocode":{
        "longitude":"0.08384000",
        "latitude":"51.49014200"
    },
    "RightToReply":"",
    "Distance":4623.9723280747176,
    "NewRatingPending":True
   }
3. Find the BusinessTypeID for "Restaurant/Cafe/Canteen" and return only the `BusinessTypeID` and `BusinessType` fields.
4. Update the new restaurant with the `BusinessTypeID` you found.
5. The magazine is not interested in any establishments in Dover, so check how many documents contain the Dover Local Authority. Then, remove any establishments within the Dover Local Authority from the database, and check the number of documents to ensure they were deleted.
6. Use `update_many` to convert `latitude` and `longitude` to decimal numbers. Use `update_many` to convert `RatingValue` to integer numbers.
### Part 3: Exploratory Analysis
> Use `NoSQL_analysis_starter.ipynb` for this section of the challenge.
Use the following questions to explore the database, and find the answers, so you can provide them to the magazine editors.
1. Which establishments have a hygiene score equal to 20?
2. Which establishments in London have a `RatingValue` greater than or equal to 4?
3. What are the top 5 establishments with a `RatingValue` of 5, sorted by lowest hygiene score, nearest to the new restaurant added, "Penang Flavours"?
4. How many establishments in each Local Authority area have a hygiene score of 0? Sort the results from highest to lowest, and print out the top ten local authority areas.

## Files
- NoSQL_analysis_starter.ipynb
- NoSQL_setup_starter.ipynb
- README.md
### Resources (folder)
- establishments.json

## Additional Resources
- 12.2 PyMongo and Advanced Queries Slides
- [db.collection.deleteMany()](https://www.mongodb.com/docs/rapid/reference/method/db.collection.deleteMany/)
- [Python MongoDB – Update_many Query](https://www.geeksforgeeks.org/python-mongodb-update_many-query/#)
