# netflix_shows_db
This repo contains solutions to the Database assigments

link to my pitch deck ---  

https://www.canva.com/design/DAGIYfmmEhk/iZm6TPwkrTOJgWWmqbsn_w/edit?utm_content=DAGIYfmmEhk&utm_campaign=designshare&utm_medium=link2&utm_source=sharebutton


I did not encounter any difficulties in importing the neflix shows csv file. I noticed that the colums are well structured but there is no explicitly defined primary key column.


                #Solution To  Data Fun :
Use the imported database.

     USE Netflix;
     
Look iside the dataframe.

     SELECT * FROM netflix_titles;

Find out how where most movies are made

      SELECT country , COUNT(country)  FROM netflix_titles GROUP BY country;

         answer - Most movies and  tv shows seem to be made from the united states

Find out which genre is most preffered based how may times they are published on site

    SELECT listed_in , COUNT(listed_in) as popular FROM netflix_titles GROUP BY listed_in ORDER BY popular DESC;  

       answer -It would appear that action heavy shows and aimations are most popular followed by Kids and Family Shows
       

 Which are the most popular shows in different countries
 
    
SELECT country, GROUP_CONCAT(title SEPARATOR ", ") AS titles, COUNT(country)
FROM netflix_titles 
GROUP BY country
LIMIT 0, 1000;


	answer- The above code showcases the popular shows in each country, for example in finlad Angry Birds is the most popular.In South Africa it is Blood and Water. 


How many movies / shows are longer than 1hour?

SELECT show_id,type , duration FROM netflix_titles WHERE duration > "60min" ORDER BY duration DESC;

answer--    The result shows that 30 movies and tv shows have a duration greater that 60 min and the highest being as long as 99min!

How many shows are rated R in the database 

SELECT type, title, rating FROM netflix_titles WHERE rating ='R';

	answer -- The results show that only 3 movies are rated R
    
How many shows were released in 1997 

SELECT type, title, release_year FROM netflix_titles WHERE release_year ='1997';

   answer  -- The data shows that only one movie  -Minsara Kanavu was released in 1997
    
