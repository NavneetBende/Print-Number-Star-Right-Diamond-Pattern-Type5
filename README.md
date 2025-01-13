PRINTING PATTERN:
2

3*3

4*4*4

4*4*4

3*3

2

PREREQUISITE:
Basic knowledge of C language and use of loops.

ALGORITHM:
Take the number of rows as input from the user and store it in any variable.(‘r‘ in this case).
Run a loop ‘r’ number of times to iterate through each of the rows. From i=0 to i<r. The loop should be structured as for( i=1 ; i<=r : i++).
Use an if condition to to print the top half of the pyramid. if (i<=r/2) run a loop from j=0 to j<=i. The loop should be structured as for(j=1; j<=i ; j++)
Run an if statement if(j!=1). If true the print star and count else only print count.
Then in the outer if statement increment count. Then print a newline
Inside this loop print count.
Outside this loop increment count and print a newline
Else decrement count and run a loop from j=0 to j<r-i. The loop should be structured as for(j=0; j<\r-i ; j++). inside the loop run an if statement if(j!=0) then print star and count else just print count.
After the loop print a newline.
CODE IN C:
#include<stdio.h>
int main()
{
int i,j,r,count;                                       //declaring integer variables i,j for loops , r for number of rows
printf("Enter the number of rows/columns :\n");        //asking user for the number of rows;
scanf("%d",&r);                                        //taking number of rows and saving in variable r
count=2;                                               //intialising count =2
for(i=1;i<=r;i++)                                      //loop for number of rows
  {
    if(i<=r/2)
      {
        for(j=1;j<=i;j++)                              //loop to print digit in every column of a row
          {
            if(j!=1)
              {
                printf("*%d",count);                    //printing digit
              }
            else
              {
                printf("%d",count);                     //printing digit
              }
          }         
        count++;                                       //incrementing count
        printf("\n");                                  //printing newline

      }
    else
      {
        count--;

        for(j=0;j<r-i+1;j++)
          {
            if(j!=0)
              {
                 printf("*%d",count);
              }
            else
              {
                 printf("%d",count);
              }
          }

         printf("\n");
       }
  }
}
TAKING INPUT:DISPLAYING OUTPUT:
 

