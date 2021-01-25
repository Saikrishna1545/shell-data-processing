# shell-data-processing

## Gitbash cheatsheet
* Curl to the file
curl "http://shakespeare.mit.edu/julius_caesar/full.html" -O "data.txt" 

* Transform each space ' ' into a return character '\12'

 tr ' ' '\12' < data.txt
 
* Pipe the output to sort

tr ' ' '\12' < data.txt | sort

* Pipe the sorted output to uniq -c to count

tr ' ' '\12' < data.txt | sort | uniq -c

* Pipe the reduced output to sort with -nr flag

tr ' ' '\12' < data.txt | sort | uniq -c | sort -nr

* output to result.txt

tr ' ' '\12' < data.txt | sort | uniq -c | sort -nr > result.txt

