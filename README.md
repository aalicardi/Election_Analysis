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
   
   ![image](https://user-images.githubusercontent.com/105028515/175394704-6cbe617c-0aae-4d1c-b7b1-5e3246862468.png)

- Which county had the largest number of votes?
   The county with the largest number of votes was **Denver County.** 
   
   This was determined in our code by using a decision statement comparing the number of votes each county received within our for loop that loops through the county_name variables in the county_vote dictionary. An if statement looks at if the first vote count for a county, c_votes, is greater than the winning_county_count variable which we previously set equal to zero, and if so, it changes the value of the winning_county_county = to the v_votes variable for that county and set the winining_county variable equal to the appropriate county. By the end of the loop, the winning_county_count will be equal to the most number of votes received by a county and the winning_county variable will be equal to the county with the most votes.
   
   ![image](https://user-images.githubusercontent.com/105028515/175399798-f2a1811f-1d60-4636-96f8-c1f4cd0f2224.png)
   ![image](https://user-images.githubusercontent.com/105028515/175399667-88ad97f5-1c18-44ef-8ae2-ff86f7fdca90.png)

- Provide a breakdown of the number of votes and the percentage of the total votes each candidate received.
  There were three total candidates in this election and their results are as follows:
   - Charles Casper Stockham: 85,213 (23.0%)
   - Diana DeGette: 272,892 (73.8%)
   - Ratmon Anthony Doane: 11,606 (3.1%)
  
  The vote count and percentage of votes received for each candidate was determined in our code similarly to how the county results were determmined. See below. 
  
  ![image](https://user-images.githubusercontent.com/105028515/175404474-839a50bd-b075-4bb6-bfc8-160cbe41b040.png)
  ![image](https://user-images.githubusercontent.com/105028515/175404599-e92b54e4-d818-44cc-9e7a-fef3f87031e5.png)

- Which candidate won the election, what was their vote count, and what was their percentage of the total votes?
  The winner of the election was **Diana Degette** with **272,892** total votes. This represents **73.8%** of the total votes.
  
  The winning candidate, their vote count, and their vote percentage was determined in our code similarly to how the winning county results were determined. See below. 
  
  ![image](https://user-images.githubusercontent.com/105028515/175404959-0287c7a7-bb81-4ce2-a7f1-32832c1ea4f8.png)
  ![image](https://user-images.githubusercontent.com/105028515/175404755-7eb487e6-8300-4b2e-90cd-a9ce444b8476.png)

## Election Audit Summary


Helping Tom analyze election data with Python
