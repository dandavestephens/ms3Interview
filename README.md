
First I installed and turned on the GUI for SQLitei. The schema was text for every line which turned out to be fine as there were no numeric columns in the table. To look for empty cells I used the following SQL:
	
Select count(A),count(B),count(C), count(D), caount(E), count(F), count(G),count(H), count(I) from ms3Interview

Next I got the number of rows with a null value and subtracted that from the row counts to get the the number of good rows.

Select A from ms3Interview Where
A="" 
By repeating that for each column I got the real rowcounts.
The rows that were missing a value were the bad rows. I used Excel to sort the table by each row and pull out the missing ones into ms3Interview and saved it as ms3Interview-bad.csv