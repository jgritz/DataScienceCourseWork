1. 
head chipotle.tsv
tail chipotle.tsv
looks like there's intro and conclusion data and a bunch or orders. Or perhaps a bunch of potential permutations of orders.


2.
How many orders do there appear to be?
1834
cut -f1 chipotle.tsv | uniq | wc
subtract 1 for the header

3.
How many lines are in this file?
4623
wc chipotle.tsv



4.
Which burrito is more popular, steak or chicken?
Chicken
grep -i -c 'chicken burrito' chipotle.tsv
grep -i -c 'steak burrito' chipotle.tsv


5.
Do chicken burritos more often have black beans or pinto beans?
Black
grep -i'chicken burrito' chipotle.tsv | grep -ic 'black'
grep -i'chicken burrito' chipotle.tsv | grep -ic 'pinto'


6.
Make a list of all of the CSV or TSV files in the DAT8 repo (using a single command). 
Think about how wildcard characters can help you with this task.
List here



7.
Count the approximate number of occurrences of the word "dictionary" (regardless of case) across all files in the DAT8 repo.
12