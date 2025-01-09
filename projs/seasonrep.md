# Season Report - An interactive Python chart generator. 

## Program Requirements 

1. (Year Selection) Prompt user to enter a year from 1970 to the last year in the database. 
2. (Scope Selection) Based on the year, give them a numbered menu that lets them pick a specific league, division, or all of the MLB teams from that year. 
3. (Report Generation) Once the year and all/league/division is chosen, then generate the following:
    * Scatter plot of team Wins vs. team average batting average 
    * Scatter plot of team Wins vs. team average slugging 
    * Scatter plot of team Wins vs. team average on-base percentage
    * Scatter plot of team Wins vs. team average runs created
    * A table giving the name, wins, and team min,max, and avg of each of the batting stats used in the scatter plots. 

## Specifications

* When computing batting stats, exclude any player with fewer than 100 plate appearances.
* When computing stats, do not include a player's stint that was not for the team in question. We're interested in team-specific statistics. 
* Users should be told the actual max year in the database when prompted for (1). This value should be determined at run-time. 
* Similarly, team and divisions for prompt (2) should be determined at run-time
* All data collection and statistic computation should be done by SQL. Python and its assorted libraries are merely there to provide a UI and interface with the DB. 
* Your program should carry out three queries: (1) get the max year for year selection (2) get the divisions for scope selection, and (3) get all the data needed for report generation.
* Scatter plots should either give each team a different color or ensure team names can be found in the mouse-over text. 


## Plotly 

Plotly produces great, interactive graphics for the web.  You can also use it to generate static graphics for posters other print mediums. For this project you just need two plots: scatter and table.
    * [Scatter](https://plotly.com/python/line-and-scatter/)
    * [Table](https://plotly.com/python/table/)

If Plotly figures are not displaying for you, then you might need to [check out this documentation](https://plotly.com/python/renderers/). For the sake of uniformity, we want the figure to pop-up in your web browser. 