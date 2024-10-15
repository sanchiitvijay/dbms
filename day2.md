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
