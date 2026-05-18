# Experiment 7: PL/SQL – Variables, Control Structures and Loops

## AIM
To write and execute simple PL/SQL programs using variables, loops, and conditional statements.


## THEORY

PL/SQL, which stands for Procedural Language extensions to the Structured Query Language (SQL). It is a combination of SQL along with the procedural features of programming languages.

**Syntax:**
```sql
DECLARE 
   <declarations section> 
BEGIN 
   <executable command(s)>
EXCEPTION 
   <exception handling> 
END;
```

### Basic Components of PL/SQL Block:
- DECLARE: Section to declare variables and constants.
- BEGIN: The execution section that contains PL/SQL statements.
- EXCEPTION: Handles errors or exceptions that occur in the program.
- END: Marks the end of the PL/SQL block.

# PL/SQL Programs – Steps and Expected Output

## 1. Write a PL/SQL program to find the Greatest of Two Numbers

### Steps:
- Declare two numeric variables and initialize them.
- Use an `IF` statement to compare the values.
- Display the greater number using `DBMS_OUTPUT.PUT_LINE`.

**Expected Output:**  
Greater number is: 80

Program:

      SET SERVEROUTPUT ON;
      
      DECLARE
          a NUMBER := 80;
          b NUMBER := 50;
      BEGIN
          IF a > b  THEN
              DBMS_OUTPUT.PUT_LINE('Greater number is: ' || a);
          ELSE
              DBMS_OUTPUT.PUT_LINE('Greater number is: ' || b);
          END IF;
      END;

<img width="1913" height="1103" alt="image" src="https://github.com/user-attachments/assets/f38507c7-4e57-4f66-842a-a9bdb1a08242" />


---

## 2. Write a PL/SQL program to Calculate Sum of First N Natural Numbers

### Steps:
- Declare a variable `n` and assign a value (e.g., 10).
- Initialize a `sum` variable to 0.
- Use a `WHILE` loop to iterate from 1 to `n`, adding each number to the sum.
- Display the result using `DBMS_OUTPUT.PUT_LINE`.

**Expected Output:**  
Sum of first 10 natural numbers is: 55

Program:

      SET SERVEROUTPUT ON;
      
      DECLARE
          n NUMBER := 1;
          sum NUMBER := 0;
      
      BEGIN
          WHILE n <= 10 LOOP
              sum := sum + n;
              n := n + 1;
          END LOOP;
      
          DBMS_OUTPUT.PUT_LINE('Sum is: ' || sum);
      END;
      /


<img width="1918" height="1096" alt="image" src="https://github.com/user-attachments/assets/cb33bcc7-d81f-4338-bd53-e7472350bd60" />


---

## 3. Write a PL/SQL program to generate Fibonacci series

### Steps:
- Declare the variable `n` to indicate how many terms to generate.
- Initialize the first two Fibonacci numbers (0 and 1).
- Use a loop to generate the next terms using the formula `c = a + b`.
- Print each term in the series.

**Expected Output:**  
n = 7  
Fibonacci sequence: 0, 1, 1, 2, 3, 5, 8

Program:

      SET SERVEROUTPUT ON;
      
      DECLARE
          n NUMBER := 7;
          a NUMBER := 0;
          b NUMBER := 1;
          c NUMBER;
          i NUMBER := 1;
      
      BEGIN
          DBMS_OUTPUT.PUT(a || ', ' || b);
      
          WHILE i <= n-2 LOOP
              c := a + b;
              DBMS_OUTPUT.PUT(', ' || c);
      
              a := b;
              b := c;
      
              i := i + 1;
          END LOOP;
      END;
      /

<img width="1907" height="1100" alt="image" src="https://github.com/user-attachments/assets/7a6929c5-5f2a-4169-95f8-4a4651fa0b50" />


---

## 4. Write a PL/SQL Program to display the number in Reverse Order

### Steps:
- Declare a variable `n` and assign a value (e.g., 1535).
- Use a loop to extract each digit using modulo and reverse the number.
- Display the reversed number.

**Expected Output:**  
n = 1535  
Reversed number is 5351

Program:

      SET SERVEROUTPUT ON;
      
      DECLARE
          n NUMBER := 1535;
          rev NUMBER := 0;
          rem NUMBER;
      
      BEGIN
          WHILE n > 0 LOOP
              rem := MOD(n, 10);
      
              rev := rev * 10 + rem;
      
              n := TRUNC(n / 10);
          END LOOP;
      
          DBMS_OUTPUT.PUT_LINE('Reversed number is ' || rev);
      END;
      /


<img width="1916" height="1096" alt="image" src="https://github.com/user-attachments/assets/d2420848-26c9-4bbb-a18d-d082dc3139b2" />


---

## 5. Write a PL/SQL program to find the largest of three numbers

### Steps:
- Declare three numeric variables `a`, `b`, and `c`.
- Use nested `IF-ELSIF-ELSE` conditions to find the largest among the three.
- Display the largest number.

**Expected Output:**  
a = 10, b = 9, c = 15  
Largest of three number is 15

Program:

         SET SERVEROUTPUT ON;
         
         DECLARE
             a NUMBER := 80;
             b NUMBER := 50;
             c NUMBER := 95;
         
         BEGIN
             IF a > b AND a > c THEN
                 DBMS_OUTPUT.PUT_LINE('Greater number is: ' || a);
         
             ELSIF b > c THEN
                 DBMS_OUTPUT.PUT_LINE('Greater number is: ' || b);
         
             ELSE
                 DBMS_OUTPUT.PUT_LINE('Greater number is: ' || c);
         
             END IF;
         END;
         /

<img width="1915" height="1105" alt="image" src="https://github.com/user-attachments/assets/0fc00445-4cb0-42b0-bd49-754c780ebe5b" />


## RESULT
Thus, the PL/SQL programs using variables, conditionals, and loops were executed successfully.
