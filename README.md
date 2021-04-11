# irvsim
simulation of single winner ranked choice election

Ingests csv in this format:

![image](https://user-images.githubusercontent.com/81826611/113756915-fc516c00-96df-11eb-80ad-0dd17e936344.png)

For initial values (to fill out csv): Find first rank percents for each candidate in race.  Then find all likely possibilities of rankings of other candidates for supporters of that candidate.  Multiply the percent of that candidates supporters you think are likely to vote that way (Group Modifier) by the first rank percent to give the first rank percent to put in the csv.  Group modifiers for each individual candidate should add up to 100.  Initial step in code gets you back to first rank percent table as sanity check.

![image](https://user-images.githubusercontent.com/81826611/114292190-ae7b9180-9a5a-11eb-8a67-5f56ce217834.png)

![image](https://user-images.githubusercontent.com/81826611/114292163-8c820f00-9a5a-11eb-8ad7-08d1fb6cf332.png)

Finds lowest percent candidate from rank_1, eliminates them and shifts the other candidates in their row left. Rank_2 to rank_1, rank_3 to rank_2, rank_4 to rank_3, rank_4 to Null.  Second round also checks if new rank_1 is a previously eliminated candidate and shift that row accordingly.

![image](https://user-images.githubusercontent.com/81826611/114320001-dcf07f80-9ae1-11eb-868a-bb44b634a6b9.png)

Uses groupby function to see total percent for each candidate in each round.

Continues until there are two candidates left.
