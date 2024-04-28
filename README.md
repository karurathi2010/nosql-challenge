# nosql-challenge
Mainly 3 parts for this challenge:

* Part 1: Database and Jupyter Notebook Set Up:
  In this part the following steps are performed:
    * Imported the provided data using  Terminal with 'uk_food' as database name and establishments as the collection name.
    * Imported required libraries.
    * Created an instance of the Mongo Client.
    * listed the database names.
    * Assigned the 'uk_food' database to a variable name 'db'.
    * Listed the collection name.
    * Reviewed a document in the establishments collection using 'find_one'.
    * Assigned the collection to a variable named 'establishments'.
 
* Part 2: Update the Database:

   * Added the provided document to the collection using 'insert_one'.
   * Checked the document inserted with the help of 'find'.
   * Found the BusinessTypeID for "Restaurant/Cafe/Canteen" and returned only the BusinessTypeID and BusinessType fields.
   * Updated the BusinessTypeID of the new restaurant with the  BusinessTypeID obtained from the above step.
   * Found how many documents have LocalAuthorityName as "Dover" using 'count_documents'.
   * Deleted the 'Dover' documents form the collection using 'delete_many'.
   * Changed the datatype of longitude and latitude of all documents in the collection using 'update_many'.
   * Changed the data type from String to Integer for RatingValue using 'update_many'.
   * Finally checked that the coordinates and rating value are now numbers using 'find_one'.
 
* Part 3: Exploratory Analysis:
This part has 4 sub parts:
* 1. Which establishments have a hygiene score equal to 20?
     To answer this question the following steps are performed:
       * Found the establishments with a hygiene score of 20 using find.
       * Found the number of documents using 'count_documents'.
       * Displayed the result using pprint.
       * Converted the result into dataframe.

* 2. Which establishments in London have a RatingValue greater than or equal to 4?
         * Found the establishments with London as the Local Authority and has a RatingValue greater than or equal to 4.
         * Found the number of documents using 'count_documents'.
         * Displayed the result using pprint.
         * Converted the result into dataframe.

* 3. What are the top 5 establishments with a RatingValue rating value of 5, sorted by lowest hygiene score, nearest to the new restaurant added, "Penang Flavours"?
        * Found the restaurant details  within 0.01 degree on either side of the latitude and longitude.
        * sorted the data in the ascending order of hygine score.
        * set the limit as 5 to get the first 5 results.
        * Displayed the result.
        * Converted the result into dataframe.
    

* 4. How many establishments in each Local Authority area have a hygiene score of 0?
     Pipeline method is used to resolve this question.
     * Created match with a hygiene score of 0.
     * Grouped the matches by Local Authority.
     * Sorted the matches from highest to lowest.
     * Used aggregation to get the result.
     * converted the result into dataframe.
 










