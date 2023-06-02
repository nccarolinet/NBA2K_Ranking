## Overview

I created this analysis for the final project in my first Data Science class.


## Problem Statement and Initial Analysis Plan:

Problem Statement: NBA2k is a popular video game for basketball fans to play virtual basketball as their favorite players. There has been some controversy regarding the NBA2k ranking system. Some basketball fans believe that the system is biased to the reputation of specific players, over pure skill. Some fans also believe some skills are valued higher than others in NBA2k. Through the exploration of this dataset, I will analyze how NBA salary correlates to NBA2k ranking to determine if the NBA values (or "ranks") the players similarly to NBA2k. I will also analyze if certain positions are valued higher in the NBA and in NBA2k by looking at the player position, their salary, and their NBA2k ranking. 


### Five Questions:

1. What positions make the most money in the NBA? 
2. Does 2k rating correlate with the round drafted?
3. Does the NBA2k player ranking correlate with the NBA salary of the player?
4. What team has the most players with high NBA2k ratings?
5. Who is the “best” player in NBA2k based on NBA salary and NBA2k ranking?


### Approach to Answer Questions:

The following data fields will be used to answer the questions:

- Categorical data: full_name, team, position, country
- Numerical data: rating, jersey, b_day, height, weight, salary 

I used the following approach to clean and analyze the data:

1. I will first need to convert the money column from a string to a float or an integer. This is because the money column has dollar signs and commas in it. Then I will need to group the data by position and calculate the mean salary for each position. 
2. To figure out if 2k rating correlates with round drafted, I will first ensure the draft_round column is all integers by replacing the “undrafted” with “0”. Converting to integer format will allow me to find the correlation coefficient. Then I will calculate the correlation coefficient. To better visualize the correlation I will create a scatter plot with Draft Round on the x-axis and Salary on the y-axis.
3. To figure out if 2k rating correlates with the salary of the player I first will create a scatterplot with a line best fit to visualize the correlation, I will have Salary on the x-axis and 2k Rating on the y-axis. Then I will calculate the correlation coefficient for extra data. 
4. To figure out what team has the most players with high 2k rankings I will create a new dataset, only including above average players. Then I will group the dataset by team and calculate the number of above average players in each team. I will display my data in a barchart.
5. To determine the best NBA player I will add a column to my dataframe that multiplies the player salary by their 2k stats and I will name it ‘Super_Score”, then I will sort the dataframe by the Super_Score in descending order. 


## Analysis: Is the NBA2k Rating System Accurate?

NBA2k is a popular video game where basketball fans can play virtual basketball as their favorite players. 2k is probably the most realistic basketball simulation game on the market, and player rankings are updated yearly to reflect the real life performance of the players. Overall 2k rankings are determined in the game by factors such as shooting, ball handling, defense, and athleticism. 2k has been criticized by players such as Lebron James, Steph Curry, and Tyler Herro who have all tweeted about how they believe their scores are too low. Basketball fans also question if 2k is biased towards player reputation and legacy as opposed to the pure skills of the players. Others believe that 2k values some skills such as shooting ability, both from the field and behind the arc, the players ability to create and finish scoring opportunities, and their ball handling and court vision skills higher over other skills such as defense. While there will never be a completely fair ranking system because most skills in basketball are subjective and impossible to measure, this project analyzed the 2k ranking system using data from the 2k video game as well as other factors from the NBA such as drafting round and salary of the players to determine if there is a correlation between 2k and the NBA using a Jupyter notebook. 

To begin, I first created a bar chart visualizing the positions that get paid the most money by the NBA. I wanted this data in order to get a general idea of the skills valued most in the NBA so I could compare those skills to the skills valued most in 2k. I concluded that centers get paid the most money, second to forwards and guards. Next, I wanted to see if 2k rating correlated with the round the player was drafted by calculating the correlation coefficient and visualizing it in a scatterplot. There was a small positive correlation (0.0073) although it is probably not significant enough to draw conclusions, this could be because some of the players entered the NBA undrafted. Then I calculated the correlation coefficient between player salary and 2k rank and saw a much stronger positive correlation (0.832) and I visualized this data with another scatter plot. 

To determine if there is possible team bias in the ranking system within 2k, I decided to create a bar chart where the NBA team was on the x-axis and the number of players on the team with above average players was on the y-axis. From this data I could determine that the Boston Celtics had the most above average players second to the Brooklyn Nets. This data does not really line up with the reputation of these teams. For example, the Boston Celtics made it to the playoffs in the 2020-2021 season, but were eliminated in the first round by the Brooklyn Nets. That being said this is not necessarily a reflection of the 2k rating system because the 2k rating system rates players individually, not as teams, and more data would be needed to rate individual players. Lastly, I decided to try to determine the overall best current player in the NBA by multiplying the NBA salary by the overall 2k ranking of all the players in my dataset and sorting the data in descending order. By using this data I was able to conclude that Steph Curry is the best current player in the NBA. Based on this data and analysis, I conclude that the 2k ranking system is a pretty accurate representation of players overall ability, especially when it is compared to the value that the NBA puts on the players. Further research will need to be conducted in order to determine if there is team bias within the ranking system. 
