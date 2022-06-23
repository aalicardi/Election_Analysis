# Election_Analysis
## Overview of Election Audit
Tom, an employee for the board of elections in Colorado, is performing an election audit of the tabulated results for a Congressional precinct in Colorado that includes the following counties: Jefferson, Denver, and Arapahoe. Although we could use excel for the audit, using Python would help automate the process for future audits. 

### Purpose
For this challenge, we are to help Tom with writing a code that analyzes the election vote data and generates a report using python. This report needs to include the follow: 
- total number of votes 
- total number of votes for each candidate
- winning candidate by popular vote
## Election Audit Results

- How many votes were cast in this congressional election?
  
   There were **369,711** votes cast in this congressional election. 
   In our code, we determine the total vote county by creating a total_votes variable, setting it equal to 0, and creating a for loop that reads each row in the .csv file of the election data after the header. As it loops through each row of the data file, the total_votes variable is increased by 1, so that once it finished the loop, the total_votes variable is equal to the total number of votes cast. 
   
   ![image](https://user-images.githubusercontent.com/105028515/175388018-07521b67-e125-4177-addb-b50d285a086c.png)

- Provide a breakdown of the number of votes and the percentage of total votes for each county in the precinct.
  
   Of the 369,711 total votes in the precinct, 38,855 (10.5%) of votes were in Jefferson County, 306,055 (82.8%) in Denver County, and 24,801 (6.7%) were in Arapahoe County. 
   In our code, we determine this information by first creating a county_options list and a county_votes dictionary. Using an if-statements in our for loop, we are able to add counties to the county_options list while making sure not to repeat counties in this list. We start tracking the votes for each county in our county_votes dictionary. As our for loop continues through each row of data, it adds a vote to the appropriate counties vote count. 
   
   ![image](https://user-images.githubusercontent.com/105028515/175393996-5c740df4-280b-4907-8c89-fb9143c3c41d.png)
   ![image](https://user-images.githubusercontent.com/105028515/175394355-4536e70c-17a1-4c76-9c58-93620ce4cfc1.png)
   
   To determine the percentage of votes for each county, we create a for loop that loops through the county_name variables in the county_vote dictionary. Within this loop, we defined a c_votes variable that reflects the total votes for each county, and a c_votes_percentage variable that reflects percentage of votes for each county. The percentage is determined by diviving the v_votes variable by the total_votese and multiplying by 100. 
   
- Which county had the largest number of votes?
  -
- Provide a breakdown of the number of votes and the percentage of the total votes each candidate received.
  -
- Which candidate won the election, what was their vote count, and what was their percentage of the total votes?
  -

## Election Audit Summary


Helping Tom analyze election data with Python
