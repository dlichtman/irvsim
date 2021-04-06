# irvsim
simulation of single winner ranked choice election

Ingests csv in this format:

![image](https://user-images.githubusercontent.com/81826611/113756915-fc516c00-96df-11eb-80ad-0dd17e936344.png)


Finds lowest percent candidate from rank_1, eliminates them and shifts the other candidates in their row left. Rank_2 to rank_1, rank_3 to rank_2, rank_4 to rank_3, rank_4 to Null.  Second round also checks if new rank_1 is a previously eliminated candidate and shift that row accordingly.

Uses pd.groupby() to see total percent for each candidate in each round.

Continues until there are two candidates left.
