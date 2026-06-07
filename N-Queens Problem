#include <stdio.h>
#include <stdlib.h>

int x[20], n;

int place(int k, int i)
{
    for (int j = 1; j < k; j++)
    {
        if (x[j] == i || abs(x[j] - i) == abs(j - k))
            return 0;
    }
    return 1;
}


void nQueens(int k)
{
    for (int i = 1; i <= n; i++)
    {
        if (place(k, i))
        {
            x[k] = i;

            if (k == n)
            {
                printf("\nSolution:\n");
                for (int r = 1; r <= n; r++)
                    printf("Queen %d -> Column %d\n", r, x[r]);
            }
            else
            {
                nQueens(k + 1);
            }
        }
    }
}

int main()
{
    printf("Enter number of queens: ");
    scanf("%d", &n);

    nQueens(n);

    return 0;
}
