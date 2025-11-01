#include <stdio.h>
#include <string.h>

int main() {
    int n, i;
    int numbers[100];
    int largest;

    printf("Find the Largest Element in an Array\n");
    printf("Enter how many elements: ");
    scanf("%d", &n);

    printf("Enter %d numbers:\n", n);
    for (i = 0; i < n; i++) {
        scanf("%d", &numbers[i]);
    }

    largest = numbers[0];
    for (i = 1; i < n; i++) {
        if (numbers[i] > largest) {
            largest = numbers[i];
        }
    }

    printf("The largest element is: %d\n\n", largest);

    char str[200];
    int count = 0;

    printf("Count the Number of Vowels in a String\n");
    printf("Enter a word or sentence: "); 
    getchar();
    fgets(str, sizeof(str), stdin);

    for (i = 0; i < strlen(str); i++) {
        char ch = str[i];
        if (ch == 'a' || ch == 'e' || ch == 'i' || ch == 'o' || ch == 'u' ||
            ch == 'A' || ch == 'E' || ch == 'I' || ch == 'O' || ch == 'U') {
            count++;
        }
    }

    printf("The number of vowels in the string is: %d\n", count);

    return 0;
}
