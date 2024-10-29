## Creating table
- CREATE TABLE sailor (sid INT PRIMARY KEY, sname VARCHAR(10), rate INT, age INT);
- CREATE TABLE boats (bid INT PRIMARY KEY, bname VARCHAR(10), color VARCHAR(10));
- CREATE TABLE reserves (sid INT, bid INT, day INT, FOREIGN KEY (sid) REFERENCES sailor (sid), FOREIGN KEY (bid) REFERENCES boats (bid));

## Inserting into table
- INSERT INTO sailor (sid, sname, rate, age) VALUES (1, 'alpha', 11, 12), (2, 'beta', 12, 13), (3, 'gamma', 13, 14), (4, 'delta', 14, 15), (5, 'epsilon', 15, 16);
- INSERT INTO boats (bid, bname, color) VALUES (1, 'alpha', 'green'), (2, 'beta', 'red'), (3, 'gamma', 'blue'), (4, 'delta', 'green'), (5, 'epsilon', 'red');
- INSERT INTO reserves (sid, bid, day) VALUES (1, 2, 1), (2, 3, 2), (3, 1, 3), (4, 2, 4), (5, 1, 5);

## Deleting the whole table
- DELETE FROM reserves

