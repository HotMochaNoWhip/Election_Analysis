# Election_Analysis
---
## Project Overview
A Colorado Board of Elections employee has given you the following task to complete the election audit of a recent local congressional election.

1. Calculate the total number of votes cast.
2. Get a complete list of candidates who recieved votes.
3. Calculate the total number of votes each candidate received.
4. Calculate the percentage of votes each caniddate won.
5. Determine the winnder of the election based on popular vote.
---
## Resources
- Data Source: election_results.csv
- Software: Python 3.7.6, Visual Studio Code 1.60.0
---
## Summary
The analysis of the election show that:
- There were 369,711 votes cast in the election.
- Denver had the largest voter turnout.
- The candidates were:
    - Charles Casper Stockham
    - Diana DeGette
    - Raymon Anthony Doane
- The candidate results were:
    - Charles Casper Stockham received 23.0% of the vote and 85,213 number of votes.
    - Diana DeGette received 73.8% of the vote and 272,892 number of votes.
    - Candidate 3 received 3.1% of the vote and 11,606 number of votes.
- The winner of the election was:
    - Diana DeGette, who receieved 73.8% of the vote and 272,892 number of votes.
---
## Challenge Overview
In this we added to the code we worked over in our module. We had already determined the total number of votes, cadidate results, and winner of the election with statistics to back it up. What we wanted to add was a count for each county, and then a printed result that gave us the county with the highest turnout.

---
## Challenge Summary
This scrpit should be usable for any election that has results listed in the same csv format. The Board of Elections could use this for any election and the code could be ammended easily to account for any additional variables you would like to meassure. 
  
Say we wanted to measure which political party each vote was registered with. We might need to adust our for loops if any of the csv columns were moved. Say we added the political party to column 2 that had the voter registered party. We would need to adjust our `canidate_name` row reader to `canidate_name = row[3]` and our `county_name` to `county_name = row[2]` since everything is shifted by 1 column.

We would also need to calcuate the affliated party and add new variables defining them, for example:
```
party_options = []
party_votes = {}
majority_party = ""
winning_party_votes = 0
winning_party_percentage = 0
```

Using these variables we could add in a nested conditional in the for loop that calls each row that would add a vote to the party's vote count. Then we could write a similar block for printing and writing something like `party_results` to our text file, giving total votes and percentage for that party!