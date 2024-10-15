## Answers for 3 ques from prev class
1.  select sname from sailor where sid in (select sid from reserves where bid is not NULL);
2.  select sid from reserves where sid in (select bid from boats where color = 'red' or color = 'green');
3.  select sname from sailor where sid in (select sid from reserves where bid is NULL);

## Employee ques

- CREATE TABLE employee(fname VARCHAR(20), lname VARCHAR(20), ssn INT PRIMARY KEY, addr VARCHAR(20), sex VARCHAR(1), salary FLOAT, superssn INT, dno INT);
- CREATE TABLE dept(dname VARCHAR(15), dno INT PRIMARY KEY, mgrssn INT, mgrstartdate INT); 
 CREATE TABLE project(pno INT PRIMARY KEY, pname VARCHAR(20), dno INT, FOREIGN KEY (dno) references dept(dno));
- CREATE TABLE workson(essn varchar (20) PRIMARY KEY,  pno INT, hours FLOAT, FOREIGN KEY (pno) references project(pno));
- ALTER TABLE employee   MODIFY dno INT, ADD CONSTRAINT fk_dept_dno  FOREIGN KEY (dno) REFERENCES dept (dno);


### Data for the table

- INSERT INTO dept (dname, dno, mgrssn, mgrstartdate) VALUES
('Human Resources', 1, 123456789, 20200101),
('Engineering', 2, 987654321, 20200201);
- INSERT INTO employee (fname, lname, ssn, addr, sex, salary, superssn, dno) VALUES
('John', 'Doe', 123456789, '123 Elm St', 'M', 60000, NULL, 1),
('Jane', 'Smith', 987654321, '456 Oak St', 'F', 65000, 123456789, 1),
('Emily', 'Jones', 456123789, '789 Pine St', 'F', 70000, 123456789, 2),
('Michael', 'Brown', 321654987, '321 Maple St', 'M', 55000, NULL, 2);
- INSERT INTO project (pno, pname, dno) VALUES
(1, 'Project Alpha', 1),
(2, 'Project Beta', 2),
(3, 'Project Gamma', 2);
- INSERT INTO workson (essn, pno, hours) VALUES
('123456789', 1, 15.5),
('987654321', 1, 20.0),
('456123789', 2, 30.0),
('321654987', 3, 25.0);
