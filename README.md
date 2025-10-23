# MODULE-6
# Program-6-a
## C-Module 6
## EX_NO-06)a)-Pointers
### Date: 19-10-2025
### Name: SYEAD JASLIN S
### Register Number:25017223
## AIM:
Write a C program to find character 'R' is vowel or consonant using pointer.
## ALGORITHM:
1. Start the program.
2. Declare a character variable to store the input character.
3. Read a character from the user using scanf.
4. Declare a character pointer and assign it the address of the input character.
5. Check if the value pointed to by the pointer is a vowel (A, E, I, O, U in uppercase or lowercase):

    a. If true, print "<character> is vowel."

   b. Otherwise, print "<character> is consonant."

6. End the program.

## PROGRAM:
```
#include<stdio.h>
int main()
{
    char ch;
    scanf("%c",&ch);
    char *p1=&ch;
    if(*p1=='A'||*p1=='a'||*p1=='E'||*p1=='e'||*p1=='i'||*p1=='I'||*p1=='o'||*p1=='O'||*p1=='U'||*p1=='u')
    printf("%c is vowel.",*p1);
    else 
    printf("%c is consonant.",*p1);
}
```
## OUTPUT:
<img width="842" height="287" alt="image" src="https://github.com/user-attachments/assets/aba2fbe3-e79f-45ae-aec1-ea8034a8d7af" />

## RESULT:
Thus the program to find character 'R' is vowel or consonant using pointer has been executed successfully
# Program-6-b
## C-Module 6
## EX_NO-06)b)-Dynamic Memory Allocation
### Date: 19-10-2025
### Name: SYEAD JASLIN S
### Register Number:25017223
## AIM:
Write a C program to Print 'Printer' using malloc() and free()
## ALGORITHM:
1. Start the program.
2. Declare a character pointer to store a dynamically allocated string.
3. Allocate memory for 10 characters using malloc and assign it to the pointer.
4. Copy the string "Printer" into the allocated memory using strcpy.
5. Print the string using printf.
6. Free the allocated memory using free.
7. End the program.

## PROGRAM:
```
#include<stdio.h>
#include<stdlib.h>
#include<string.h>
int main()
{
    char *str;
    str=(char*)malloc(10*sizeof(char));
    strcpy(str,"Printer");
    printf("%s",str);
    free(str);
}
```
## OUTPUT:
<img width="851" height="235" alt="Screenshot 2025-10-20 093735" src="https://github.com/user-attachments/assets/d8e21347-bf62-4097-8c7a-23f0caf30e97" />

## RESULT:
Thus the program to Print 'Printer' using malloc() and free() has been executed successfully
# Program-6-c
## C-Module 6
## EX_NO-06)c)-User Defined Datatype
### Date: 19-10-2025
### Name: SYEAD JASLIN S
### Register Number:25017223
## AIM:
C program to read and print an employee's detail using structure
## ALGORITHM:
1. Start the program.
2. Define a structure named employee with three members: 

    a. name (character array of size 20)  

    b. id (integer)  

    c. salary (float)  

3. Declare a variable of type struct employee.
4. Read the employee details (name, id, salary) from the user using scanf.
5. Print the entered details using printf in a formatted manner.
6. End the program.

## PROGRAM:
```
#include<stdio.h>
    struct employee
    {
        char name[20];
        int id;
        float salary;
    };
    int main()
    {
        struct employee e1;
        scanf("%s %d %f",e1.name,&e1.id,&e1.salary);
        printf("Entered detail is:\nName: %s\nId: %d\nSalary: %.2f",e1.name,e1.id,e1.salary);
    }
```
## OUTPUT:
<img width="841" height="259" alt="Screenshot 2025-10-20 094133" src="https://github.com/user-attachments/assets/b0f39204-1fc6-4965-8181-47027eda4994" />

## RESULT:
Thus the program to read and print an employee's detail using structure has been executed successfully
# Program-6-d
## C-Module 6
## EX_NO-06)d)-User Defined datatype
### Date: 19-10-2025
### Name: SYEAD JASLIN S
### Register Number:25017223
## AIM:
create a nested structure to read(customer no,name & unit consumption) and store the details of gas customer and calculate the gas bill.
## ALGORITHM:
1. Start the program.
2. Define a structure named gas with three members: 

    a. cno (integer for customer number)  

    b. name (character array of size 20)  

   c. units (integer for units consumed)  
3. Declare a variable of type struct gas.
4. Declare an integer variable amt to store the bill amount and initialize it to 0.
5. Read the customer number, name, and units consumed from the user using scanf.
6. Calculate the bill amount based on the units consumed:
 
    a. If units ≤ 50, amt = units * 10.

    b. If units > 50 and ≤ 100, amt = (50*10) + ((units-50)*20).

    c. If units > 100, amt = (50*10) + (50*20) + ((units-100)*30).
7. Add a fixed charge of 50 to amt.
8. Deduct a 10% discount from amt.
9. Print the final bill amount using printf.
10. End the program.

## PROGRAM:
```
#include<stdio.h>
struct gas
{
    int cno,units;
    char name[20];
};

int main()
{
    int amt=0;
    struct gas g;
    scanf("%d%s%d",&g.cno,g.name,&g.units);
    if(g.units<=50)
    amt=g.units*10;
    else if(g.units<=100&&g.units>50)
    amt=(50*10)+((g.units-50)*20);
    else if(g.units>100)
    amt=(50*10)+(50*20)+((g.units-100)*30);
    amt+=50;
    amt=amt-(amt/10);
    printf("Bill_amount=%d",amt);
    
}
```
## OUTPUT:
<img width="831" height="401" alt="Screenshot 2025-10-20 094529" src="https://github.com/user-attachments/assets/d17416d4-5a76-439c-90a9-7343b03aa42d" />

## RESULT:
Thus the program to read(customer no,name & unit consumption) and store the details of gas customer and calculate the gas bill. has been executed successfully
# Program-6-e
## C-Module 6
## EX_NO-06)e)-User Defined Datatype
### Date: 19-10-2025
### Name: SYEAD JASLIN S
### Register Number:25017223
## AIM:
Create a structure for Electricity Bill calculation using function-Passing structure to a function by address(reference)(use service no, name, previous reading, current reading, unit consumption & amount as data members).
## ALGORITHM:
1. Start the program.
2. Define a structure named eb with four members: 

     a. no (integer for service number)  

     b. name (character array of size 20)  

    c. unit1 (integer for previous reading)  

    d. unit2 (integer for current reading)  

3. Declare a variable of type struct eb.
4. Read the service number, name, previous reading, and current reading from the user using scanf.
5. Calculate the units consumed: un = unit1 - unit2.
6. Declare an integer variable amt to store the bill amount and initialize it to 0.
7. Calculate the amount based on units consumed:

   a. If un ≤ 100, amt = un * 2.  
 
    b. If un > 100 and ≤ 300, amt = (100*2) + ((un-100)*3).  

   c. If un > 300, amt = (100*2) + (200*3) + ((un-300)*5).  
8. Print the service number, service name, unit consumption, and amount in a formatted manner using printf.
9. End the program.
## PROGRAM:
```
#include<stdio.h>
struct eb
{
    int no,unit1,unit2;
    char name[20];
};
int main()
{
    struct eb s;
    scanf("%d%s%d%d",&s.no,s.name,&s.unit1,&s.unit2);
    int un=s.unit1-s.unit2;
    int amt=0;
    if(un<=100)
    amt=un*20;
    else if(un<=300)
    amt=(100*2)+((un-100)*3);
    else
    amt=(100*2)+(200*3)+((un-300)*5);
    printf("service number:%d\nservice name:%s\nunit consumption:%d\namount:%d.00",s.no,s.name,un,amt);
}
```
## OUTPUT:
<img width="834" height="481" alt="Screenshot 2025-10-20 095113" src="https://github.com/user-attachments/assets/7198b42d-6c01-4ba6-b182-094e4dc4868b" />

## RESULT:
Thus the program to structure for Electricity Bill calculation using function-Passing structure to a function by address(reference)(use service no, name, previous reading, current reading, unit consumption & amount as data members) has been executed successfully
