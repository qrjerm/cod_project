# cod_project
Showcasing use of webscraping, Excel and PowerBI
![SampleDB](https://user-images.githubusercontent.com/82239548/171299155-c5de119c-54cf-4a8c-9238-e0301f9286ae.jpg)

# [Completed COD Project Dashboard (Pdf) - See above image](https://github.com/qrjerm/cod_project/blob/main/GameStatsDashboard.pdf)

## COD Dashboard: Project Overview
* Call of Duty: Modern Warfare is a First Person Shooter game for PC, Xbox and Playstation
* Statistics from the game are free and accessible on https://cod.tracker.gg/modern-warfare
* In this project we use python to scrape data from the website to create our own dashboard for visualization and insights

# [Click here to see the Jupyter Notebook with all the code used in this project!](https://github.com/qrjerm/cod_project/blob/main/FinalVersionCCT.ipynb)

## Resources Used
* Python
* Microsoft Excel
* Microsoft PowerBI
* Data from [cod.tracker.gg/modern-warfare](https://cod.tracker.gg/modern-warfare/profile/battlenet/ChefRoy%2311358/mp/matches)

## Using Python to scrape data from the codtracker website
* Using Selenium and Chromedriver I was able to load the codtracker website, go to my account and scrape the stats for each game
* codtracker loads the last 20 games played by any player so keeping that in mind I cleaned the data using python
* After converting the web elements into a list form there was some further cleaning to do so I converted all elements into a string
* Once the data was cleaned I ran into an issue where the gamemode and time were recognized as one element so left them as is to clean later in Excel using powerquery (see image below)
![Game Time](https://user-images.githubusercontent.com/82239548/171301733-0b3b7578-bf13-4946-85a4-3a88275ab627.jpg)

## Creating a Dataframe in Python with Pandas for visibility and accessibility in Excel
* After cleaning up the data I created a dataframe of the last 20 games using Pandas and NumPy
* From there I change the numerical values from strings to numbers and exported the dataframe to a new sheet in excel in table form
![Dataframe](https://user-images.githubusercontent.com/82239548/171301898-ff3ae36c-30ff-4982-89c6-b5dd3205cd20.jpg)

## Editing in excel using powerquery
* I loaded the new file with game data from the last 20 games in excel
* From there I used powerquery to split the Gamemode & Time column by splitting each column by 8 characters from the left since time is always in the format: 'HH:MM ##'
![PowerQueryEditor](https://user-images.githubusercontent.com/82239548/171301952-34b3e2de-2d7c-4a3e-b658-c713901219bd.jpg)

## Gamemode and Time columns now neatly separated
![FinalTable](https://user-images.githubusercontent.com/82239548/171302016-8841f88d-8616-40a6-ad55-5568b5da8d4e.jpg)

## Building Dashboard in PowerBI
* Lastly I opened the finished table in PowerBI to create a dashboard (See image below or at the very top of this page)
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
 
 ![SampleDB](https://user-images.githubusercontent.com/82239548/171299155-c5de119c-54cf-4a8c-9238-e0301f9286ae.jpg)


[Click here to see the Jupyter Notebook with all the code used in this project!](https://github.com/qrjerm/cod_project/blob/main/FinalVersionCCT.ipynb)
