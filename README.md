# vetores_euripedes

#intercalação vetores

#include <stdio.h>
#include <stdlib.h>

int main()
{
   int i, A[5] = {1, 2, 3, 4, 5};
   int C[10], B[5] = {6, 7, 8, 9, 10};

   for (i = 0; i < 5; i++)
   {
       C[2 * i] = A[i]; //C[2 * 0] = A [0] == 1
       C[2 * i + 1] = B[i]; //C[2 * 0 + 1] = B [0] = 6
   }
   for (i = 0; i < 10; i++)
   {
       printf("C[%d]: %d\n", i, C[i]);
   }
    return 0;
}
//C[10] = {1, 6, 2, 7, 3, 8, 4, 9, 5, 10}

//cópia de elementos de D menores que 40 para A 
#include <stdio.h>
#include <stdlib.h>

int main()
{
    int D[10] = {22, 16, 42, 51, 19, 36, 60, 17, 70, 28};
    int A[10], j, i;
    j = 0;

    for (i = 0; i < 10; i++)
    {
        if (D[i] < 40)
        {
            A[j] = D[i];
            j++;
        }
    }
     for (i = 0; i < j; i++)
        {
            printf("A[%d]: %d\n", i, A[i]);
        }


    return 0;
}
// A[0] = D [0] == 22 < 40 (ok) ; A[1] = D[1] == 16 < 40 (ok) ; A[2] = D[2] = 42 (não ok) ; A[3] = D[3] = 51 (nao ok) ...
