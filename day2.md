## Answers for 3 ques from prev class
1.  select sname from sailor where sid in (select sid from reserves where bid is not NULL);
2.  select sid from reserves where sid in (select bid from boats where color = 'red' or color = 'green');
3.  select sname from sailor where sid in (select sid from reserves where bid is NULL);
