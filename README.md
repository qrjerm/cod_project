# cod_project
Showcasing use of webscraping, Excel and PowerBI


# [Completed COD Project Dashboard (Pdf)](https://github.com/qrjerm/cod_project/blob/main/GameStatsDashboard.pdf)

## COD Dashboard: Project Overview
* Call of Duty: Modern Warfare is a First Person Shooter game for PC, Xbox and Playstation
* Statistics from the game are free and accessible on https://cod.tracker.gg/modern-warfare
* In this project we use python to scrape data from the website to create our own dashboard for visualization and insights
* [Click here to see completed Dashboard (Pdf)](https://github.com/qrjerm/cod_project/blob/main/GameStatsDashboard.pdf)
# [Click here to see the Jupyter Notebook with all the code used in this project!](https://github.com/qrjerm/cod_project/blob/main/FinalVersionCCT.ipynb)

## Resources Used
* Python
* Microsoft Excel
* Microsoft PowerBI
* Data from [cod.tracker.gg/modern-warfare](https://cod.tracker.gg/modern-warfare/profile/battlenet/ChefRoy%2311358/mp/matches)

# [Click here to see the Jupyter Notebook with all the code used in this project!](https://github.com/qrjerm/cod_project/blob/main/FinalVersionCCT.ipynb)
## Using Python to scrape data from the codtracker website
* Using Selenium and Chromedriver I was able to load the codtracker website, go to my account and scrape the stats for each game
* codtracker loads the last 20 games played by any player so keeping that in mind I cleaned the data using python
* After converting the web elements into a list form there was some further cleaning to do so I converted all elements into a string
* Once the data was cleaned I ran into an issue where the gamemode and time were recognized as one element so left them as is to clean later in Excel using powerquery

## Creating a Dataframe in Python with Pandas for visibility and accessibility in Excel
* After cleaning up the data I created a dataframe of the last 20 games using Pandas and NumPy
* From there I change the numerical values from strings to numbers and exported the dataframe to a new sheet in excel in table form

## Editing in excel using powerquery
* I loaded the new file with game data from the last 20 games in excel
* From there I used powerquery to split the Gamemode & Time column by splitting each column by 8 characters from the left since time is always in the format: 'HH:MM ##'

## Building Dashboard in PowerBI
* Lastly I opened the finished table in PowerBI to create a [dashboard](https://github.com/qrjerm/cod_project/blob/main/GameStatsDashboard.pdf)
* Blue Segment includes:
  * Title
  * My game ID
  * Game Logo
* Green Segment includes:
  * Total Kills
  * Average Kills per game
  * Highest K/D out of 20 matches
  * Lowest K/D out of 20 matches
  * Average K/D out of 20 matches
* Line plots include:
  * Kills per game by map
  * Kills per game by gamemode

[Click here to see completed Dashboard (Pdf)](https://github.com/qrjerm/cod_project/blob/main/GameStatsDashboard.pdf)