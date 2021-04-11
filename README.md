# irvsim
simulation of single winner ranked choice election

Ingests csv in this format:

![image](https://user-images.githubusercontent.com/81826611/113756915-fc516c00-96df-11eb-80ad-0dd17e936344.png)

For initial values (to fill out csv): Find first rank percents for each candidate in race.  Then find all likely possibilities of rankings of other candidates for supporters of that candidate.  Multiply the percent of that candidates supporters you think are likely to vote that way (Group Modifier) by the first rank percent to give the first rank percent to put in the csv.  Initial step in code gets you back to first rank percent table as sanity check.

![image](https://user-images.githubusercontent.com/81826611/114291977-6445e080-9a59-11eb-8d37-4ad774017d87.png)

![image](https://user-images.githubusercontent.com/81826611/114291995-91928e80-9a59-11eb-9050-fb0954b2cd78.png)

Finds lowest percent candidate from rank_1, eliminates them and shifts the other candidates in their row left. Rank_2 to rank_1, rank_3 to rank_2, rank_4 to rank_3, rank_4 to Null.  Second round also checks if new rank_1 is a previously eliminated candidate and shift that row accordingly.

Uses groupby() to see total percent for each candidate in each round.

Continues until there are two candidates left.
