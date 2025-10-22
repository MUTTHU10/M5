EX-21-POINTERS
# AIM:
Write a C program to check whether the given number is even number or odd number using pointers. 

## ALGORITHM:
1.	Declare a variable to hold the floating-point number (23.65).
2.	Declare a pointer to integer to point to the address of the variable.
3.	Use the pointer to check whether the given number is even.
4.	If the condition is true, then print the given number is even.
5.	Otherwise, print the given number is odd.
6.	End the program.

## PROGRAM:
```
#include <stdio.h>
int main()
{
    int num;
    int *ptr=&num;
    scanf("%d",ptr);
    if (*ptr%2==0)
    {
        printf("%d is even.",*ptr);
    }
    else
    printf("%d is odd.",*ptr);
}
```

## OUTPUT:
 	

<img width="663" height="296" alt="Screenshot 2025-10-22 073434" src="https://github.com/user-attachments/assets/9417da20-5940-4aef-a7dd-ca49b1b8aed5" />



## RESULT:
Thus the program to check whether the given number is even or odd using pointer has been executed successfully.
 
 


# EX-22-FUNCTIONS AND STORAGE CLASS

## AIM:

Write a C program to calculate the Product of given natural numbers using Recursion

## ALGORITHM:

1.	Define a recursive function Product that takes an integer parameter n.
2.	Return n multiplied by the result of the calculateProduct function called with n - 1.
3.	Declare an integer variable n and an unsigned long long variable product.
4.	Initialize n with the value n (for the first n natural numbers).
5.	Call the calculateProduct function with n and store the result in the product variable.
6.	Print the result, indicating it is the product of the first n natural numbers.

## PROGRAM:
```
#include <stdio.h>
int product(int num)
{
    if (num==0)
    {
        return 1;
    }
    else
    return num*product(num-1);
}
int main()
{
    int num;
    scanf("%d",&num);
    int res=product(num);
    printf("Product is = %d",res);
}
```

## OUTPUT:

<img width="861" height="352" alt="Screenshot 2025-10-22 074228" src="https://github.com/user-attachments/assets/c350d2fe-147d-478a-a5ef-141a32fcf826" />


## RESULT:

Thus the program has been executed successfully.
 
 


# EX-23-ARRAYS AND ITS OPERATIONS

## AIM:

Write a C Program to find Sum of Diagonal Elements of a Matrix[3x3]

## ALGORITHM:

1.	Declare and initialize the matrix with the desired values.
2.	Create a loop to iterate through each row of the matrix.
3.	Inside the loop, calculate the sum of the elements in the diagonal where row is equal to column.
4.	Print the sum of diagonal.

## PROGRAM:
```
#include <stdio.h>

int main()
{
    int row,col,N,M,sum=0;
    scanf("%d %d",&N,&M);
    int arr[N][M];
    for(row=0;row<N;row++)
    {
        for(col=0;col<M;col++)
        {
            scanf("%d",&arr[row][col]);
        }
    }
    for (row=0;row<N;printf("\n"),row++)
    {
        for(col=0;col<M;col++)
        {
            if(row==col)
            {
                printf("%d",arr[row][col]);
                sum=sum+arr[row][col];
            }
        }
    }
    printf("The Sum of Diagonal Elements of a Matrix =  %d",sum);
    return 0;
}

```


## OUTPUT

<img width="1159" height="448" alt="Screenshot 2025-10-22 074648" src="https://github.com/user-attachments/assets/ec695475-0145-44a5-83b1-7733fe167daf" />

 
 

 ## RESULT
 
The program to find the sum of diagonal elements has been executed successfully.

# EX-24-STRINGS

## AIM:

Write a program in C to find the largest and smallest word in a string.

## ALGORITHM:

1.	Intialize a string.
2.	use scanf to get the input from the user.
3. Find the length of the words in the string.
4. print the word with largest and smallest length.
5. End the program.

## PROGRAM:
```
#include <stdio.h>
#include <string.h>
#include <ctype.h>
int main()
{
    char str[1000];
    char word[100],smallest[100],largest[100];
    int i=0,j=0,minlen=1000,maxlen=0;
    scanf("%[^\n]s",str);
    while (str[i]!='\0')
    {
        if (!isspace(str[i])&&str[i]!='\n')
        {
            word[j++]=str[i];
        }
        else
        {
            if(j>0)
            {
                word[j]='\0';
                if(j<minlen)
                {
                    minlen=j;
                    strcpy(smallest,word);
                }
                if (j>maxlen)
                {
                    maxlen=j;
                    strcpy(largest,word);
                }
                j=0;
            }
        }
        i++;
    }
    if(j>0)
    {
        word[j]='\0';
        if(j<minlen)
        {
            strcpy(smallest,word);
        }
        if(j>maxlen)
        {
            strcpy(largest,word);
        }
    }
        printf("The largest word is '%s'\n",largest);
        printf("and the smallest word is '%s'\n",smallest);
        printf("in the string : 'this is a string with largest and smallest word.'.");
    }

```

 ## OUTPUT
<img width="1162" height="327" alt="Screenshot 2025-10-22 075407" src="https://github.com/user-attachments/assets/03af1a3a-5c28-4f30-aa1c-17c81754270c" />

 

## RESULT

Thus the C program to String process executed successfully



# EX -25 –POINTERS
## AIM

write a c program to find factorial of the given number using pointer:

## ALGORITHM
Step 1: Start the program.
Step 2: Declare a integer, use scanf to get the input from the user.
Step 3: Use integer pointer to point the address of the integer.
Step 4: use for loop to find the factorial.
Step 5: End the program.

## PROGRAM
```
#include <stdio.h>
int main()
{
    int num,ind,res=1;
    int *ptr=&num;
    scanf("%d",ptr);
    for (ind=1;ind<=*ptr;ind++)
    {
        res=res*ind;
    }
    printf("Factorial of entered number is : %d",res);
}
```

## OUTPUT
<img width="991" height="292" alt="Screenshot 2025-10-22 083426" src="https://github.com/user-attachments/assets/0f29846c-fb55-4012-adf2-7d87bdf9b70c" />

 

## RESULT

Thus the C program to find the factorial of the given number using pointer has been executed successfully.


