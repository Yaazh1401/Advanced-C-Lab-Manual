EXP NO:1 C PROGRAM FOR ARRAY OF STRUCTURE TO CHECK ELIGIBILITY FOR THE VACCINE.

Aim:
To write a C program for array of structure to check eligibility for the vaccine person age above 6 years of age.

Algorithm:
1.	Declare structure eligible with age (integer) and n (character array)
2.	Declare variable e of type eligible
3.	Input age and name using scanf, store in e
4.	If e.age <= 6
-	Print "Vaccine Eligibility: No"
Else
-	Print "Vaccine Eligibility: Yes"
5.	Print details (e.age, e.n)
6.	Return 0
 
Program:

```
#include <stdio.h>

struct Person {
    int age;
    char name[50];
};

int main() {
    struct Person p;

    scanf("%d", &p.age);

    scanf("%s", p.name);

    printf("Age:%d\n", p.age);
    printf("Name:%s", p.name);
    printf("vaccine:%d\n", p.age);
    if(p.age > 18) {
        printf("eligibility:yes\n");
    } else {
        printf("eligibility:no\n");
    }

    return 0;
}


```


Output:

<img width="1204" height="338" alt="image" src="https://github.com/user-attachments/assets/ad1561ed-153f-45ac-bc6c-b101fdbc000c" />



Result:
Thus, the program is verified successfully. 



EXP NO:2 C Program to add two distances in the feet system using pointer to structure
Aim:
to Write a C Program to add two distances in the feet system using pointer to structure

Algorithm:
1. Define structure Distance with member feet
2. Declare d1, d2, dist as Distance variables
3. Declare result as pointer to Distance
4. Set result = address of dist
5. Input d1.feet
6. Input d2.feet
7. Set result->feet = d1.feet + d2.feet
8. Print "Sum of distances = ", result->feet
9. Stop
 
Program:

```
#include <stdio.h>

struct Distance {
    int feet;
} d1, d2, dist, *result;

int main() {
    result = &dist; 
    scanf("%d", &d1.feet);
    scanf("%d", &d2.feet);
    result->feet = d1.feet + d2.feet;
    printf("Sum of distances = %d'\n", result->feet);

    return 0;
}

```



Output:


<img width="1170" height="382" alt="image" src="https://github.com/user-attachments/assets/a926d3cd-ec47-49fb-ac9a-219910b56219" />




Result:
Thus, the program is verified successfully


 
EXP.NO:3 C PROGRAM TO READ A FILE NAME FROM USER AND WRITE THAT FILE USING FOPEN()

Aim:
To write a C program to read a file name from user

Algorithm:
1.	Include the necessary header file stdio.h.
2.	Begin the main function.
3.	Declare a file pointer p.
Declare a character array name to store the file name.
4.	Prompt the user to enter a file name.
Use scanf to input the file name into the name array.
5.	Print a message indicating that the file with the specified name has been created successfully.
6.	Use fopen to open a file with the name provided by the user in write mode ("w").
-	If successful, continue to the next step.
-	If unsuccessful, print an error message and exit the program with a non-zero status.
1.	Print a message indicating that the file has been opened successfully.
2.	Use fclose to close the file.
3.	Print a message indicating that the file has been closed.
4.	End the main function.
5.	Return 0 to indicate successful program execution.
 
Program:

```
#include <stdio.h>

int main() {
    char filename[100];
    FILE *fp;

    scanf("%s", filename);

    fp = fopen(filename, "w");

    if (fp == NULL) {
        printf("Error creating file.\n");
        return 1;
    }

    printf("%s File Created Successfully\n", filename);
    printf("%s File Opened\n", filename);

    fclose(fp);
    printf("%s File Closed\n", filename);

    return 0;
}

```



Output:


<img width="1054" height="473" alt="image" src="https://github.com/user-attachments/assets/8a115770-d666-4575-ab2e-10844932f2f8" />







Result:
Thus, the program is verified successfully
 


EXP NO:4   PROGRAM TO READ A FILE NAME FROM USER, WRITE THAT FILE AND INSERT TEXT IN TO THAT FILE
Aim:
To write a C program to read, a file and insert text in that file
Algorithm:
1.	Include the necessary header file stdio.h.
2.	Begin the main function.
3.	Declare a file pointer p.
Declare character arrays name and text. Declare an integer variable num.
4.	Prompt the user to enter a file name and the number of strings.
Use scanf to input the file name into the name array and the number of strings into the num variable.
5.	Use fopen to open a file with the name provided by the user in write mode ("w").
-	If successful, continue to the next step.
-	If unsuccessful, print an error message and exit the program with a non-zero status.
6.	Print a message indicating that the file has been opened successfully.
1.	Use a loop to input strings from the user and write them to the file using fputs.
2.	Use fclose to close the file.
3.	Print a message indicating that data has been added successfully.
4.	End the main function.
5.	Return 0 to indicate successful program execution.
 
Program:

```
#include <stdio.h>

int main() {
    char filename[100], text[100];
    int n;
    FILE *fp;

    scanf("%s", filename);
    scanf("%d", &n);

    fp = fopen(filename, "w");

    if (fp == NULL) {
        printf("Error opening file.\n");
        return 1;
    }

    printf("%s Opened\n", filename);

    for (int i = 0; i < n; i++) {
        scanf(" %[^\n]", text);
        fprintf(fp, "%s\n", text);
    }

    fclose(fp);
    printf("Data added Successfully\n");

    return 0;
}

```




Output:


<img width="1094" height="501" alt="image" src="https://github.com/user-attachments/assets/3c143cdc-2b30-4fc9-ac52-db2ac178026a" />






Result:
Thus, the program is verified successfully



Ex No 5 : C PROGRAM TO DISPLAY STUDENT DETAILS USING STRUCTURE

Aim:
The aim of this program is to dynamically allocate memory to store information about multiple subjects (name and marks), input the details for each subject, and then display the stored information. Finally, it frees the allocated memory to prevent memory leaks.

Algorithm:
1.Input the number of subjects.

2.Read the integer value n from the user, which represents the number of subjects.

3.Dynamically allocate memory:

4.Use malloc to allocate memory for n subjects. Each subject has a name (array of characters) and marks (integer).

5.If memory allocation fails (i.e., the pointer s is NULL), display an error message and exit the program.

6.Input the details of each subject

7.Use a for loop to read the name and marks of each subject using scanf. For each subject, store the name as a string and marks as an integer in the dynamically allocated memory.

8.Display the details of each subject

9.Use another for loop to print the name and marks of each subject.

10.Free the allocated memory

11.After all operations are done, call free(s) to release the dynamically allocated memory.

12.Return from the main function

13.End the program by returning 0.

Program:

```
#include <stdio.h>

struct Student {
    int reg_no;
    char name[50];
    int jun, july, aug, sep; 
};

int main() {
    struct Student s;
    int total_present;
    float attendance_percentage;

    scanf("%d", &s.reg_no);
    scanf("%s", s.name);
    scanf("%d", &s.jun);
    scanf("%d", &s.july);
    scanf("%d", &s.aug);
    scanf("%d", &s.sep);

    if (s.jun > 21 || s.july > 21 || s.aug > 21 || s.sep > 21) {
        printf("Error: Working days in any month should be <= 21\n");
        return 0;
    }

    total_present = s.jun + s.july + s.aug + s.sep;
    attendance_percentage = (total_present / 84.0) * 100;

    printf("Reg.no:%d\n", s.reg_no);
    printf("Name:%s\n", s.name);
    printf("Total.No.of.present days:%d\n", total_present);
    printf("Attendence:%.2f\n", attendance_percentage);

    if (attendance_percentage > 75.0)
        printf("eligibility:yes\n");
    else
        printf("eligibility:no\n");

    return 0;
}

```




Output:


<img width="963" height="547" alt="image" src="https://github.com/user-attachments/assets/58ad1c43-dede-48c0-9fd4-1023d3799b83" />







Result:
Thus, the program is verified successfully
