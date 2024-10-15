## Creating table
create table sailor (sid int primary key, sname varchar(10), rate int, age int);
create table boats (bid int primary key, bname varchar(10), color varchar(10) );
create table reserves(sid int, bid int, day int, foreign key (sid) references sailor (sid), foreign key (bid) references boats (bid));
## Inserting into table
insert into sailor (sid, sname, rate, age) values (1, 'alpha', 11, 12), (2, 'beta', 12,13), (3, 'gamma', 13,14), (4, 'delta', 14,15), (5, 'epsilon', 15,16);
insert into boats (bid, bname, color) values (1, 'alpha', 'green'), (2, 'beta', 'red'), (3, 'gamma', 'blue'), (4, 'delta', 'green'), (5, 'epsilon','red');
insert into reserves (sid, bid, day) values (1, 2, 1), (2, 3, 2), (3, 1, 3), (4, 2, 4), (5, 1, 5);
## Deleting the whole table
delete from reserves

