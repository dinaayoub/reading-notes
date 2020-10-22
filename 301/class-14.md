# Read: 14a - DB Normalization

[Essential: Database Normalization Explained in Simple English](https://www.essentialsql.com/get-ready-to-learn-sql-database-normalization-explained-in-simple-english/)

## Reasons to normalize

1- minimize duplicate data
2- avoid data modification issues
3- simplify queries
4- making search and sort easier

## Anomalies

1- Insert Anomaly - we can't record data until we know info for the entire row.
2- Update Anomaly - if we don't update all rows, then data inconsistencies appear.
3- Deletion Anomaly - Deleting a row causes removal of more than one set of facts.

## Database normalizatin forms

Each form requires those before it.
1- First Normal Form (1NF): info is stored in a relational table with each column containing atomic values. No repeating groups of columns
2- Second Normal Form (2NF): 1NF and all the columns depend on the table's primary key.
3- Third Normal Form (3NF): 2 NF and all of the columns are not transitively dependent on the primary key.

## Project Ideas

What ideas do you have for projects? What would your model be that you can control and update the view with? What API(s) could you use to make this a reality?
[Take a look at this repo for inspiration about APIs you could use.](https://github.com/public-apis/public-apis)
