- SELECT * FROM employee ORDER BY salary;
- SELECT * FROM employee ORDER BY salary DESC;
- SELECT COUNT(dno), dno FROM employee GROUP BY dno;
- ALTER TABLE employee MODIFY COLUMN addr VARCHAR(255);
- ALTER TABLE employee CHANGE addr address VARCHAR(255)
- ALTER TABLE employee ADD password VARCHAR(10);
- ALTER TABLE employee DROP COLUMN password;
- ALTER TABLE employee MODIFY dno INT, ADD CONSTRAINT fk_dept_dno FOREIGN KEY (dno) REFERENCES dept (dno);


