# Floyd-s-Triangle
Floyd's Triangle is a right-angled triangular array of natural numbers. It's created by filling the rows of the triangle with consecutive natural numbers. The first row contains the number 1, the second row contains 2 and 3, the third row contains 4, 5, and 6, and so on.

Here's an example of Floyd's Triangle with 5 rows:

```
1
2 3
4 5 6
7 8 9 10
11 12 13 14 15
```

### C Program to Generate Floyd's Triangle

To generate Floyd's Triangle, we'll use nested loops. The outer loop will handle the rows, and the inner loop will fill in the numbers for each row.

```c
#include <stdio.h>

int main() {
    int n, num = 1;
    printf("Enter the number of rows: ");
    scanf("%d", &n);

    for (int i = 1; i <= n; i++) {
        for (int j = 1; j <= i; j++) {
            printf("%d ", num);
            num++;
        }
        printf("\n");
    }

    return 0;
}
```

### Explanation:

1. **Input Handling:**
   - The user inputs the number of rows `n` for Floyd's Triangle.

2. **Loop for Rows:**
   - The outer loop `for (int i = 1; i <= n; i++)` iterates through each row, starting from 1 up to `n`.

3. **Loop for Numbers:**
   - The inner loop `for (int j = 1; j <= i; j++)` prints the numbers for each row. The number of elements in each row is equal to the row number.

4. **Printing and Incrementing:**
   - Inside the inner loop, the current number `num` is printed, and then `num` is incremented to the next natural number.

5. **Newline for Each Row:**
   - After the inner loop completes for a row, a newline character `\n` is printed to move to the next row.

### Result:

If the user inputs `5`, the program will generate and print the following Floyd's Triangle:

```
1
2 3
4 5 6
7 8 9 10
11 12 13 14 15
```

This program demonstrates the use of nested loops to create a structured triangular pattern with consecutive natural numbers, making it a good exercise for understanding iteration and control flow in C programming.
