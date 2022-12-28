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
![1](https://github.com/salvamike/Election_Analysis/blob/main/1.png)

2. Initialize variables: incuding our total_votes counter, lists (candidate_options and county_options), dictionaries (candidate_votes and county_votes), and our winning candidate/county variables (see below).
![2](https://github.com/salvamike/Election_Analysis/blob/main/2.png)

3. Set for candidate loop: To add candidate_names to candidate_options and track candidate votes (see below).
![3](https://github.com/salvamike/Election_Analysis/blob/main/3.png)

4. Repeat step 3 for county loop: To add county_names to county_options and track county votes (see below).
![4](https://github.com/salvamike/Election_Analysis/blob/main/4.png)

5. Set for loop to calculate winning county: Calculates the total count and percentage for each county (see below).
![5](https://github.com/salvamike/Election_Analysis/blob/main/5.png)

6. Repeat step 5 for winning candidate: Calculates the total count and percentage for each candidate (see below).
![6](https://github.com/salvamike/Election_Analysis/blob/main/6.png)

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

## Election-Audit Summary ##

### Business Proposal ###
The data analytics team wanted to provide the Colorado Board of Elections team and the Election Commission members with a business proposal for how to use this Python script in future elections. In its current state, this Python script is written for this specific election, reviewing candidates and counties. It is likely that in future elections the board and commision members may want to view the election results in different formats. For example, viewing the data by city instead of county and identifying the county with the lowest turnout. For this reason, the data anlytics team provided two additional snipets of Python script that can be used in lieu of the current script or on its own for future election audits:

> ***Example One - Adding a Floating-Decimal Value to the candidate_name Dictionary:***
>> The purpose of this Python script is to allow those who audit the election data to identify the floating-decimal format of total votes each candidate received from the total votes of 369,711. This will allow the team to use an additional format of the calculated election data.

***Modified Python Script Steps:***

* Establish a new variable called vote_floating_decimal under the canddiate vote count for loop:
   * vote_floating_decimal = float(votes)/float(total_votes)
* Calculate candidate_results dictionary:
   * candidate_results = (
f"{candidate_name}: {vote_percentage:.1f}% ({votes:,}) (vote_floating_decimal:.})\n"
)

> ***Example Two - Lowest County Turnout***
>> The purpose of this Python script is to allow those who audit the election data to view which county had the lowest amount of turnout. These findings can help the state deploy marketing tactics to encourage these individuals to show up for elections. This will allow the voice of smaller or low turnout counties have a voice in the election and its respective results.

***Modified Python Script Steps:***

* Establish a loosing_county variable:
   * loosing_county = ""
   * loosing_county_count = 0
   * loosing_county_percentage = 0

* Write an if statement for the loosing county:
   * if (votes2 < loosing_county_count) and (votes2_percentage < loosing_county_percentage):
      * loosing_county = county_name
      * loosing_county_count = votes2
      * loosing_county_percentage = votes2_percentage
* Print the county with the smallest turnout to the terminal:
   * loosing_smallest_county_turnout_summary = (
   * f"\n---------------------]n"
   * f"Smallest County Turnout: {loosing_county}\n"
   * f"----------------------\n"
   * )
