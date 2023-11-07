# Ex. No: 4 Creating Procedures using PL/SQL

### DATE : 25/9/23
### AIM: To create a procedure using PL/SQL.

### Steps:
1. Create employee table with following attributes (empid NUMBER, empname VARCHAR(10), dept VARCHAR(10),salary NUMBER);
2. Create a procedure named as insert_employee data.
3. Inside the procdure block, write the query for inserting the values into the employee table.
4. End the procedure.
5. Call the insert_employee data procedure to insert the values into the employee table.
6. Display the employee table

### Program:
```python


CREATE TABLE s4(
     empid NUMBER,
     empname VARCHAR(10),
     dept VARCHAR(10),
     salary NUMBER
    );
CREATE OR REPLACE PROCEDURE s4_data AS
    BEGIN
    INSERT INTO s4(empid,empname,dept,salary)
    values(1,'mukesh','CEO',10000000);
    INSERT INTO s4(empid,empname,dept,salary)
    values(2,'sree ram','HR',500000);
    INSERT INTO s4(empid,empname,dept,salary)
    values(3,'mukil','MD',200000);
    COMMIT;
   FOR s4_rec IN (SELECT * FROM s4)LOOP
   DBMS_OUTPUT.PUT_LINE('EMPLOYEE ID:'||s4_rec.empid||',EMPLOYEE NAME:'|| s4_rec.empname||
   ',DEPARTMENT:'||s4_rec.dept||',SALARY:'||s4_rec.salary);
   END LOOP;
   END;
  /
Begin
    s4_data; end;
    /


```
### Output:
![image](https://github.com/SAKTHISWAR/Ex-No-4-Creating-Procedures-using-PL-SQL/blob/main/ou1.jpeg)

### Result:
Thus the program to create a procedure using sql has been succesfully verified.

