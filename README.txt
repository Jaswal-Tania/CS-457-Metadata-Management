Tania Jaswal
CS-457-Metadata-Management


To run this program, run these instructions in your terminal-

g++ main.cpp -o main
./main < PA1_test.sql


Design document-

1 - How your program organizes multiple databases?
2 - How your program manages multiple tables?
3 - At a very high level, how you implement those required functionalities?

Each database is implemented as a folder via system call and each table 
is implemeted as a txt/csv file that will contain the appropriate data. 
The USE keyword tells which database is being used and therefore only 
tables in that directory can be altered or selected. There is a vector
that holds an abstract data type instance of each table. The table data 
type contains values such as "name", "attributes", and "Database Associated".
There are many error checks associated with databases and tables like making
sure the database in use actually holds the table you want to select or alter.


IMPLEMENTATIONS:
---------------

Database creation = system call to create folder if the folder does not already exist.
Database deletion = system call to delete folder if it does exist.
Table creation = system call to create txt/csv file inside of the database denoted by the "USE" command.
Table deletion = system call to delete txt/csv file inside of the database in use if the file exists.
Table update = Add attributes to the abstract data type Table. The variable updated is the attrs.
Table query = print out the table if and only if the table exists inside the database in use.