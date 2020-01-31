#include <stdio.h>
 
#define MAXROW      10
#define MAXCOL      10
 
int main()
{
    int matrix[MAXROW][MAXCOL];
    int i,j,r,c;
     
    printf("Enter number of Rows :");
    scanf("%d",&r);
    printf("Enter number of Cols :");
    scanf("%d",&c);
 
    printf("\nEnter matrix elements :\n");
    for(i=0;i< r;i++)
    {
        for(j=0;j< c;j++)
        {
            printf("Enter element [%d,%d] : ",i+1,j+1);
            scanf("%d",&matrix[i][j]);
        }
    }
 
    /*check condition to print diagonals, matrix must be square matrix*/
    if(r==c)
    {
            /*print diagonals*/
            for(i=0;i< c;i++)
            {
                for(j=0;j< r;j++)
                {
 
                    if(i==j)
                        printf("%d\t",matrix[j][i]);    /*print elements*/
                    else
                        printf("\t");   /*print space*/
                }
                printf("\n");   /*after each row print new line*/      
            }
    }
    else
    {
        printf("\nMatrix is not a Square Matrix.");
    }
    return 0;   
}
output:
Enter number of Rows :2                                                                                                 
Enter number of Cols :2                                                                                                 
                                                                                                                        
Enter matrix elements :                                                                                                 
Enter element [1,1] : 6                                                                                                 
Enter element [1,2] : 4                                                                                                 
Enter element [2,1] : 2                                                                                                 
Enter element [2,2] : 9                                                                                                 
6                                                                                                                       
        9                                                                                                               
            
