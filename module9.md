EXP NO:11 C PROGRAM TO DISPLAY STACK ELEMENTS USING AN ARRAY.

Aim:
To write a C program to display stack elements using an array.
Algorithm:
1.	Include Necessary Header Files
2.	Declare Global Variables
3.	Define the Display Function
4.	Main Function (or Other Relevant Code)
5.	Initialize the stack and top as needed.
6.	Perform stack operations (push, pop, etc.).
7.	Use the display function to visualize the stack's contents
 
Program:

```
float stack[100];
int top,i;
void display()
{
    for(i=top;i>=0;i--){
        printf("%.1f\n",stack[i]);
    }
}

```
Output:

<img width="862" height="608" alt="image" src="https://github.com/user-attachments/assets/14a53ec1-5045-42c1-a8cd-64b6979697ec" />




Result:
Thus, the program to display stack elements using an array is verified successfully.
 

EXP NO:12  PROGRAM TO PUSH THE GIVEN ELEMENT IN TO A STACK USING ARRAY.
Aim:
To create a C program to push the given element in to a stack using array.
Algorithm:
1.	Declare global variables for the stack size, top index, and the stack itself.
2.	Define the push function to add a floating-point number to the stack.
3.	Initialize the stack size, top index, and the stack itself.
4.	Call the push function as needed.
 
Program:

```
int size=3,top=-1,stack[100];
void push (int data)
{
    if (top == size-1 )
    {
    printf("stack is full\n");
    }
    else
    {
        top = top +1;
        stack[top] = data;
    }
}
```
Output:

<img width="938" height="552" alt="image" src="https://github.com/user-attachments/assets/ec4ac069-6715-4298-95cf-a18642757599" />




Result:
Thus, the program to push the given element in to a stack using array is verified successfully


 
EXP NO:13 C PROGRAM TO DISPLAY QUEUE ELEMENTS USING ARRAY.
Aim:
To write a C program to display queue elements using array

Algorithm:
1.	Declare global variables for the queue, rear, front, and iteration.
2.	Define the display function to print the elements of the queue.
3.	Initialize the queue, rear, and front as needed.
4.	Call the display function and perform other queue operations as needed.
 
Program:

```
int queue[50];
int rear=-1, front=-1;
void display()
{
    int i=0;
    if(front==-1)
    {
    printf("No elements to display\n");
    }
    else
    {
        for(i=front;i<=rear;i++)
        {
            printf("%c ", queue[i]);
        }
    }
}
```
Output:

<img width="832" height="541" alt="image" src="https://github.com/user-attachments/assets/0620ab55-8381-4783-9fbb-641e8b3ad80d" />



Result:
Thus, the program to display queue elements using array is verified successfully.


 
EXP NO:14 C PROGRAM TO INSERT ELEMENTS IN QUEUE USING ARRAY.
Aim:
To write a C program to insert elements in queue using array.

Algorithm:
1.	Declare global variables for the size, rear, front, and the queue itself.
2.	Define the enqueue function to add a float to the queue.
3.	Initialize the rear, front, and size of the queue as needed.
4.	Call the enqueue function as needed.

Program:

```
float queue[50];
int front,rear,size=5;
void enqueue(float data)
{
        if(front==1||front<size)
        {
            front=0;
            rear++;
            queue[rear]=data;
    }
}

```

Output:

<img width="856" height="488" alt="image" src="https://github.com/user-attachments/assets/f0ec1b9f-d78f-440e-a9a7-b96d726f3efe" />

Result:
Thus, the program to insert elements in queue using array is verified successfully.



 
EXP NO:15 C FUNCTION TO DELETE ELEMENTS IN QUEUE USING ARRAY



Aim:

To create a function in C that deletes an element from a queue implemented using an array.

Algorithm:

1.	Check if the Queue is Empty
o	If the front pointer is -1, it means the queue is empty, and there are no elements to delete. Print a message indicating that the queue is empty.
2.	Delete the Front Element
o	If the queue is not empty, the element at the front index is deleted.
o	Increment the front pointer by 1 to remove the element and point to the next element in the queue.
3.	Check if the Queue Becomes Empty After Deletion:
o	After deletion, check if the front pointer has passed the rear pointer (front > rear). If this is true, reset both front and rear to -1, indicating that the queue is now empty.
4.	End the Function.



Program:

```
int front, rear;
void dequeue()
{
    if(front==-1||front>rear)
    {
        printf("Queue Underflow.\n");
        return;
    }
    else
    {
        front=front+1;
    }
}
```

Output:

<img width="959" height="668" alt="image" src="https://github.com/user-attachments/assets/d14b1a18-1ce4-499a-a68c-ccaae6274201" />



Result:
Thus, the function that deletes an element from a queue implemented using an array is verified successfully.
