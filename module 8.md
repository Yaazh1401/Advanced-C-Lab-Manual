EXP NO:6 C PROGRAM PRINT THE LOWERCASE ENGLISH WORD CORRESPONDING TO THE NUMBER
Aim:
To write a C program print the lowercase English word corresponding to the number
Algorithm:
1.	Start
- Initialize an integer variable n.
2.	Input Validation
3.	Switch Statement cases.
-	case 41: printf("forty one\n"); break;
-case 42: printf("forty two\n")
-case 43: printf("forty three\n")
-...
-case 48: printf("forty eight\n"); break;
-case 49: printf("forty nine\n"); break;
4.	Exit the program.
 
Program:

```
#include <stdio.h>

int main() {
    int n;
    scanf("%d", &n);

    if (n >= 41 && n <= 49) {
        switch (n) {
            case 41: printf("forty one\n"); break;
            case 42: printf("forty two\n"); break;
            case 43: printf("forty three\n"); break;
            case 44: printf("forty four\n"); break;
            case 45: printf("forty five\n"); break;
            case 46: printf("forty six\n"); break;
            case 47: printf("forty seven\n"); break;
            case 48: printf("forty eight\n"); break;
            case 49: printf("forty nine\n"); break;
        }
    } 
    else if (n > 49) {
        printf("Greater than 49\n");
    }

    return 0;
}
```




Output:


<img width="802" height="353" alt="image" src="https://github.com/user-attachments/assets/b7254952-b353-47af-b1f6-28c90edd1b94" />






Result:
Thus, the program is verified successfully
 
EXP NO:7 C PROGRAM TO PRINT TEN SPACE-SEPARATED INTEGERS     IN A SINGLE  LINE DENOTING THE FREQUENCY OF EACH DIGIT FROM 0 TO 9.
Aim:
To write a C program to print ten space-separated integers in a single line denoting the frequency of each digit from 0 to 9.
Algorithm:
1.	Start
2.	Declare char array a[50] outer loop for each digit from 0 to 9
3.	Initialize counter c to 0
4.	For each character in the string print count c for current digit, followed by a space
5.	Increment h to move to the next digit
6.	End
 
Program:

```
#include <stdio.h>

int main() {
    char str[1000];
    int freq[10] = {0};

    scanf("%s", str);

    for (int i = 0; str[i] != '\0'; i++) {
        if (str[i] >= '0' && str[i] <= '9')
            freq[str[i] - '0']++;
    }

    for (int i = 0; i < 10; i++)
        printf("%d ", freq[i]);

    return 0;
}


```




Output:


<img width="937" height="306" alt="image" src="https://github.com/user-attachments/assets/1332f090-de55-4665-8d03-e2bd99fd45b0" />







Result:
Thus, the program is verified successfully

EXP NO:8 C PROGRAM TO PRINT ALL OF ITS PERMUTATIONS IN STRICT LEXICOGRAPHICAL ORDER.
Aim:
To write a C program to print all of its permutations in strict lexicographical order.

Algorithm:
1.	Start
2.	Declare variables s (pointer to an array of strings) and n (number of strings)

3.	Memory Allocation
Dynamically allocate memory for s to store an array of strings
4.	Input
Read the number of strings n from the user Dynamically allocate memory for each string in s
5.	Permutation Generation Loop
6.	Memory Deallocation
Free the memory allocated for each string in s Free the memory allocated for s
7.	End
 
Program:

```
#include <stdio.h>
#include <string.h>
#include <stdlib.h>
void swap(char **a, char **b) {
    char *temp = *a;
    *a = *b;
    *b = temp;
}

int next_permutation(char *arr[], int n) {
    int i = n - 2;
    while (i >= 0 && strcmp(arr[i], arr[i + 1]) >= 0)
        i--;
    if (i < 0)
        return 0;
    int j = n - 1;
    while (strcmp(arr[i], arr[j]) >= 0)
        j--;
    swap(&arr[i], &arr[j]);
    for (int l = i + 1, r = n - 1; l < r; l++, r--)
        swap(&arr[l], &arr[r]);
    return 1;
}

int compare(const void *a, const void *b) {
    return strcmp(*(const char **)a, *(const char **)b);
}

int main() {
    int n;
    scanf("%d", &n);
    char **arr = (char **)malloc(n * sizeof(char *));
    for (int i = 0; i < n; i++) {
        arr[i] = (char *)malloc(101 * sizeof(char)); 
        scanf("%s", arr[i]);
    }
        qsort(arr, n, sizeof(char *), compare);
    
    do {
        for (int i = 0; i < n; i++)
            printf("%s%c", arr[i], i == n - 1 ? '\n' : ' ');
    } while (next_permutation(arr, n));
    for (int i = 0; i < n; i++)
        free(arr[i]);
    free(arr);
    
    return 0;
}
```




Output:


<img width="1176" height="468" alt="image" src="https://github.com/user-attachments/assets/229a4ce9-0f32-4fc7-9d22-759de6d3a26f" />







Result:
Thus, the program is verified successfully
 
EXP NO:9 C PROGRAM PRINT A PATTERN OF NUMBERS FROM 1 TO N AS
SHOWN BELOW.
Aim:
To write a C program to print a pattern of numbers from 1 to n as shown below.
Algorithm:
1.	Start
2.	Declare integer variables n, i, j, min
3.	Read the value of n from the user
4.	Calculate the length of the side of the square matrix: len = n * 2 - 1
5.	Matrix Generation Loop
6.	Calculate min as the minimum distance to the borders
7.	End
 
Program:

```
#include <stdio.h>

void printPattern(int n) {
    int size = 2 * n - 1;
    for (int i = 0; i < size; i++) 
    {

        for (int j = 0; j < size; j++) 
        {
            int value = n - (i < j ? (i < size - j - 1 ? i : size - j - 1) : (j < size - i - 1 ? j : size - i - 1));
            printf("%d ", value);
        }
        printf("\n");
    }
}

int main() {
    int n;
    scanf("%d", &n);
    printPattern(n);
    return 0;
}
```




Output:


<img width="1109" height="691" alt="image" src="https://github.com/user-attachments/assets/8e874eb9-a826-4b3a-a9a9-c8fbe8c4a32b" />







Result:
Thus, the program is verified successfully

EXP NO:10 Given a five digit integer, print the sum of its digits.

Aim:

to Given a five digit integer, print the sum of its digits.
Algorithm:

1. Start the program and read the 5-digit number n.
2.Extract each digit using division and modulus operations.
3.Add all five digits together and store in sum.
4.Display the value of sum.
5.Stop the program.

Program:

```
#include <stdio.h>

int main() {
    int n;
    scanf("%d", &n);
    int d1, d2, d3, d4, d5, sum;
    d1 = n / 10000;          
    d2 = (n / 1000) % 10;   
    d3 = (n / 100) % 10;   
    d4 = (n / 10) % 10;    
    d5 = n % 10;            
    sum = d1 + d2 + d3 + d4 + d5;
    printf("%d\n", sum);
    return 0;
}

```




Output:


<img width="1189" height="360" alt="image" src="https://github.com/user-attachments/assets/91c62c25-c8f4-404d-980e-e5354370bdae" />







Result:
Thus, the program is verified successfully



























