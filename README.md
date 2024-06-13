# netflix_shows_db
This repo contains solutions to the Database assigments


I did not encounter any difficulties in importing the neflix shows csv file. I noticed that the colums are well structured but there is no explicitly defined primary key column.


                #Solution To  Data Fun :
Use the imported database
     -- use Netflix;
look iside the dataframe
     -- SELECT * FROM netflix_titles;

Find out how where most movies are made
      -- SELECT country , COUNT(country)  FROM netflix_titles GROUP BY country;

         answer - Most movies and  tv shows seem to be made from the united states

Find out which genre is most preffered based how may times they are published on site
    -- SELECT listed_in , COUNT(listed_in) as popular FROM netflix_titles GROUP BY listed_in ORDER BY popular DESC;  

       answer -It would appear that action heavy shows and aimations are most popular followed by Kids and Family Shows 
