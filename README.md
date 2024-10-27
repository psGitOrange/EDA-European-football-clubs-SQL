# SQL in Action: Exploring European Clubs
European football clubs are professional teams competing in various **domestic** leagues and international tournaments across **Europe**. Some of the most famous leagues include the **Premier League (England), Serie A (Italy), Bundesliga (Germany), La Liga (Spain), and Ligue 1 (France)**. They play a crucial role in the global popularity and significantly influence global football culture, broadcasting rights, merchandising, and player transfers, making them pivotal in the sport's ecosystem.

### Problem statement:
**Performance evaluation** of teams and players in European football clubs using **SQL** and to identify top goal scorers and league winners for each season.
Focus on understanding how factors like **home vs. away** conditions and game probabilities influence team success, providing insights for strategic improvements.

### Dataset

This dataset contains football-related data covering the **Top5 leagues** in **Europe** from **2014-2020**. It is structured like a relational database, which makes it easy to work with, regardless of the problem you want so solve.

These are the following tables:
1. `Appearances`: Every appearance a player has made in one of the Top5 leagues 
2. `Games`: All games played in one of the Top5 leagues
3. `Leagues`: Top5 leagues
4. `Players`: Every player who has played in one of the Top5 leagues
5. `Shots`: All shots taken in one of the Top5 leagues
6. `Teams`: All teams who played in one of the Top5 leagues
7. `Teamstats`: Game statistics by team in one of the Top5 leagues over the specified time window

We will look at the fields below 

<img src="https://i.imgur.com/tvYKGfX.png" alt="football_clubs_db_erd" width="720"/>

In this Exploratory Data Analysis (**EDA**) project we will be doing the **following:**
1. **Window** functions for advanced analytics
2. **Indexing** to enhance query performance and efficiency
3. **Ranking** techniques to identify top performers
4. **Functions** for data manipulation
5. **Views** to simplify complex queries

### Summary
This EDA project analyzed a comprehensive football dataset, consisting of **726,906 rows** and **87 columns** across seven tables in an **SQLite database**. The dataset was connected using `sql.connect()` and populated with tables like players, leagues, and teams using `to_sql()`. Through this structured analysis, several insights emerged:

- **Home Advantage**: Home teams consistently achieved higher win rates than away teams, suggesting significant support impact.
- **Scoring Trends**: To secure a win, both home and away teams averaged around **2.4 goals**, while maintaining strong defense, limiting opponents to an average of **0.55 goals**. Draws saw each team scoring around 1 goal.
- **League Comparisons**: **Bundesliga** averaged the **highest** scoring rate at **2.95 goals per game**, while **Ligue 1** had the lowest at **2.6 goals**.
- **Top Performers**: From **2014 to 2020**, **Lionel Messi** led with **231 goals** and ranked first in assists **97**, **sharing** this position with **Kevin De Bruyne**.
- **League Champions**: In **2018**, top teams across leagues included `Bayern Munich (Bundesliga), Barcelona (La Liga), PSG (Ligue 1), Manchester City (Premier League), and Juventus (Serie A)`.
- **El Clásico Highlights**: Between **2014 and 2020**, **Barcelona** won **6** times in **El Clásico**, edging out **Real Madrid’s 5** wins. Notable matches included surprising upsets, like **Barcelona’s 3-2 away victory** with a **22% win probability** in 2017, and **Real Madrid’s 2-0 home win** in 2020 with only a **24% win probability**.

### Future Work
- Draw more insightes on players like shoot accuracy, goal score percentage, passes, etc
- Insights on each league(rework the same format) (number of players, top 5 of each league, journey of season winners through out the campaign with timeline)
