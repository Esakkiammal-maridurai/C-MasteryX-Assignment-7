1. Swap Two Numbers Using Pointers

#include <stdio.h>

void swap(int *a, int *b) {
    int temp;
    temp = *a;
    *a = *b;
    *b = temp;
}

int main() {
    int x, y;

    printf("Enter two numbers: ");
    scanf("%d %d", &x, &y);

    printf("Before swapping: x = %d, y = %d\n", x, y);

    swap(&x, &y);

    printf("After swapping: x = %d, y = %d\n", x, y);

    return 0;
}


Output:

Enter two numbers: 10 20
Before swapping: x = 10, y = 20
After swapping: x = 20, y = 10

2. Reverse an Array Using Pointers
#include <stdio.h>
int main() {
    int a[100], n, i, temp;
    int *start, *end;

    printf("Enter array size: ");
    scanf("%d", &n);

    printf("Enter array elements: ");
    for (i = 0; i < n; i++) {
        scanf("%d", &a[i]);
    }

    start = a;
    end = a + n - 1;

    while (start < end) {
        temp = *start;
        *start = *end;
        *end = temp;

        start++;
        end--;
    }

    printf("Reversed array: ");
    for (i = 0; i < n; i++) {
        printf("%d ", a[i]);
    }

    return 0;
}


Output:

Enter array size: 5
Enter array elements: 1 2 3 4 5
Reversed array: 5 4 3 2 1

3. Find Maximum and Minimum Using Pointers
#include <stdio.h>

int main() {
    int a[100], n, i;
    int max, min;
    int *p;

    printf("Enter array size: ");
    scanf("%d", &n);

    printf("Enter array elements: ");
    for (i = 0; i < n; i++) {
        scanf("%d", &a[i]);
    }

    p = a;
    max = *p;
    min = *p;

    for (i = 1; i < n; i++) {
        p = a + i;

        if (*p > max) {
            max = *p;
        }

        if (*p < min) {
            min = *p;
        }
    }

    printf("Maximum element: %d\n", max);
    printf("Minimum element: %d\n", min);

    return 0;
}


Output:

Enter array size: 5
Enter array elements: 12 5 30 8 2
Maximum element: 30
Minimum element: 2
