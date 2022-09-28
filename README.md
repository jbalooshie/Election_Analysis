# Election_Analysis
This repository was created as part of a 6 month Data Analystics Bootcamp administed by George Washington University. This is the repository for the Module 3 Challenge. This challenge served as an introduction to Python. Topics covered including writing if else statements, loading csvs, saving outputs to text files, and writing code that can be re-purposed. Final project work is in PyPoll_Challenge.py. 

27 SEP 2022 - Updated repo to better organize files.  

## Project Overview
The purpose of this project was to provide a summary of the results of a congressional election in a specific district. This summary will provide the total number of votes cast, the total number of votes received by each candidate, the percentage of the total vote each candidate received, the number of votes cast in each county, which candidate won the election, and which county cast the most votes. This information can be gathered by analyzing the data in Excel, but by writing a Python script we can provide an easy way to analyze results from other elections. The goal of this project is to deliver a functioning script that can analyze this specific election's results, and be re-purposed to analyze the results of other elections. 

## Election-Audit Results
- How many votes were cast in this congressional election?
  - There were 369,711 votes were cast in this congressional election.
  
![Total Votes](https://github.com/jbalooshie/Election_Analysis/blob/main/images/total_votes.PNG)

- Provide a breakdown of the number of votes and the percentage of total votes for each county in the precinct.
  - In Jefferson county, 38,855 votes were cast, which was 10.5% of the total votes. 
  - In Denver county, 306,055 votes were cast, which was 82.8% of the total votes. 
  - In Arapahoe county, 24,801 votes were cast, which was 6.7% of the total votes.
  
![County Votes](https://github.com/jbalooshie/Election_Analysis/blob/main/images/count_votes.PNG)

- Which county had the largest number of votes?
  - Denver county had the largest number of votes. 
  
![Largest Turnout](https://github.com/jbalooshie/Election_Analysis/blob/main/images/largest_turnout.PNG)

- Provide a breakdown of the number of votes and the percentage of the total votes each candidate received.
  - Charles Casper Stockham received 85,213 votes, which was 23.0% of the total votes. 
  - Diana DeGette received 272,892 votes, which was 73.8% of the total votes. 
  - Raymon Anthony Doane received 11,606 votes, which was 3.1% of the total votes.
  
![Candidate Votes](https://github.com/jbalooshie/Election_Analysis/blob/main/images/candidate_votes.PNG)

- Which candidate won the election, what was their vote count, and what was their percentage of the total votes?
  - Diana DeGette won the election with 272,892 votes, which was 73.8% of the total votes cast.
  
![Winner](https://github.com/jbalooshie/Election_Analysis/blob/main/images/winner.PNG)

## Election-Audit Summary
The Python script that was designed for this project can be re-purposed and used to audit the results of any election. Although the script was designed for this specific set of election results, making modifications is easy. First, the results of the election should be saved as a CSV file. Once saved, the code can be changed to have it read the results of that file. In snippet below, we would want to replace "election_results.csv" with the name of the new results file we would like to read. 

`file_to_load = os.path.join("Resources", "election_results.csv")`

The variables are zeroed out at the start every time the script is run, so the script pulls the name and votes associated with each candidate as it runs through the document. If the CSV file for the next election is set up differently, we just must modify where the script looks for these values. In the example below, we would just need to update the range value in brackets to the column where the candidate's name is written in the next set of data. 

`candidate_name = row[2]`

The script creates a dictionary of the candidates in the file and keeps track of how many votes each candidate receives. In this case, it also tracks the county where the vote was cast. This can be modified if another value is needed. For example, if we wanted to use this for a smaller local election, we could remove this variable. We could also change it so it shows another piece of data that might be in the results file, like a zip code. 

This is a simple script that is incredibly versatile. It can be quickly edited and used to audit the results of other elections. The most important factor is understanding how the data is formatted in the CSV file, and then updating the code to work with it.
