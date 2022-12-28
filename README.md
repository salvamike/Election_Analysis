# Election Analysis #

## Project Overview ##

Seth, Tom's manager has assigned me the job of completing an election audit from a recent local congressional election.
The overall goals for the data analytics team include:

1. Calculate total number of votes cast.
2. Get a complete list of candidates who received votes
3. Calculate the total number of votes each candidate received
4. Calculate the percentage of votes each candidate won
5. Determine the winner of the election based on popular vote


## Election-Audit Results ##

The purpose of this election audit was to find additional information like the voter turnout for each county, the percentage of votes from each county out of the total count, and find the county with the highest turnout.

### Python Script ###

Once the data analytics team was provided a task list, the team developed Python script to automate the election audit. You can find the full Python script at PyPoll_Challenge.py. Below are the major psuedocoding steps the data analytics team had to perform to automate this process:

1. Import "csv" and "os" dependencies: This allows us to view the file election_results.csv that is the final vote count report and join our files using the teams Microsoft operating system (see below).


2. Initialize variables: incuding our total_votes counter, lists (candidate_options and county_options), dictionaries (candidate_votes and county_votes), and our winning candidate/county variables (see below).


3. Set for candidate loop: To add candidate_names to candidate_options and track candidate votes (see below).


4. Repeat step 3 for county loop: To add county_names to county_options and track county votes (see below).


5. Set for loop to calculate winning county: Calculates the total count and percentage for each county (see below).


6. Repeat step 5 for winning candidate: Calculates the total count and percentage for each candidate (see below).


7. Print all necessary data to text file: View text file at: election_analysis.txt


### Results ###

The purpose of this election audit was to find additional information like the voter turnout for each county, the percentage of votes from each county out of the total count, and find the county with the highest turnout.
Below is a screenshot of the election_analysis.txt file for the Colorado congressional election and a breakdown of the findings:
![Election Analysis](https://github.com/salvamike/Election_Analysis/blob/main/election%20result%20txt%20image.png)

* How many votes were cast in this congressional election?
    * There was a total of 369,711 total votes for this congressional election.
* Provide a breakdown of the number of votes and percentage of total votes for each county in the precinct.
    * In Jefferson county 38,855 individuals chose to vote in this congressional election and accounted for 10.5% of the 369,711 total votes.
    * In Denver county 306,055 individuals chose to vote in this congressional election and accounted for 73.8% of the 369,711 total votes.
    * In Arapahoe county 24,801 individuals chose to vote in this congressional election and accounted for 6.7% of the 369,711 total votes.
* Which county had the largest number of votes?
    * The county with the largest number of votes was Denver, which accounted for 73.8% of all total votes for this congressional election.
* Provide a breakdown of the number of votes and the percentage of total votes each candidate received.
    * Charles Casper Stockham received 85,213 total votes which accounted for 23.0% of all 369,711 total votes.
    * Diana DeGette received 272,892 total votes which accountded for 73.8% of all 369,711 total votes.
    * Raymon Anthony Doane received 11,606 total votes which accounted for 3.1% of all 369,711 total votes.
* Which candidate won the election, what was their vote count, and what was their pecentage of total votes?
    * The winning candidate for the Colorado congressional election was Diana DeGette, as she obtained a majority of total votes.
