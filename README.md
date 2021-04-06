# irvsim
simulation of single winner ranked choice election

Ingests csv in this format:

Percent	rank_1	rank_2	rank_3	rank_4
15	Democrat	Murkowski	Libertarian	Right R
7.5	Democrat	Libertarian	Murkowski	Right R
7.5	Democrat	Libertarian	Right R	Murkowski
11	Murkowski	Right R	Libertarian	Democrat
5.5	Murkowski	Libertarian	Right R	Democrat
5.5	Murkowski	Democrat	Libertarian	Right R
5.25	Libertarian	Democrat	Murkowski	Right R
5.25	Libertarian	Murkowski	Democrat	Right R
5.25	Libertarian	Right R	Murkowski	Democrat
5.25	Libertarian	Right R	Democrat	Murkowski
13.5	Right R	Murkowski	Libertarian	Democrat
6.75	Right R	Libertarian	Murkowski	Democrat
6.75	Right R	Murkowski	Democrat	Libertarian

Finds lowest percent candidate from rank_1, eliminates them and shifts the other candidates in their row to rank_1 to be counted in the next round.

Continues until there are two candidates left.
