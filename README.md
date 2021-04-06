# irvsim
simulation of single winner ranked choice election

Ingests csv in this format:

![image](https://user-images.githubusercontent.com/81826611/113756915-fc516c00-96df-11eb-80ad-0dd17e936344.png)


Finds lowest percent candidate from rank_1, eliminates them and shifts the other candidates in their row to rank_1 to be counted in the next round.

Continues until there are two candidates left.
