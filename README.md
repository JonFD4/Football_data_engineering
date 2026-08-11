# Football_data_engineering

## What is the problem?
A sport bar in london is popular for hosting footbal games.
Once the game is over, everyone wants to check wear the teams rank which leads to:
- wi-fi overload: causes latency issues
- staff are forced to context switch: due to people asking staff about league table when wi-fi goes down. Disrupts bar service. Atmosphere and vibe dips
- Atmosphere change causes people to leave bar early.

## What is the solution? What do we want?
- Display the league standings on:
    * A second screen next to the main big one
    * small table-top screens and tablets around the bar having the same data

## Why this projects?
- Alternative to webscraping, bots to collect data from websites which can overload website and break
- hurts the experience of companies' target audience, hence APIs in JSON format.
- APIs allows access to website information without access to raw database.

## Skills
- pull data from Rest API
-  Clean it with python
- Store it in a database

## Stages
1. Extract : fetch data from API
2. Transform: parse JSON response into Pandas Dataframe
3. Load: upload clean data into MySQL. Ensure data in SQL is similafr to what is on the actual premier league website.


# Design
1. What information do the fans want to see?
    - where is my team on the league table? 
    - A table showimg all 20 premier league teams + their rankings
2. What data do we need to generate that information?
    - Table standing include:
        - each team's name
        - where they are positioned
        - how many games they've played 
        - how many games won, drawn, and lost
        - number of goals scored, conceded, goal difference

3. What does good data quality look like- and how do we check it?
    1. There must be 20 teams
    2. All cells must be populated
    3. Numeric fields must be integers

# Installing dependencies
## Kernel
```
python -m ensurepip --upgrade
```
```
python -m pip install  --upgrade pip
```
```
python -m pip install  ipykernel
```
## Python libraries
```
python -m pip install pandas mysql-connector-python python-dotenv requests
```