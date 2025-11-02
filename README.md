#include <stdio.h>

int main() {
    int size, i, largest;
    int arr[100];
    char text[100];
    int vowelCount = 0;

    
    printf("Finding the Largest Element in an Array\n");
    printf("Enter the number of elements: ");
    scanf("%d", &size);

    printf("Enter %d elements:\n", size);
    for (i = 0; i < size; i++) {
        scanf("%d", &arr[i]);
    }

    largest = arr[0]; 
    for (i = 1; i < size; i++) {
        if (arr[i] > largest) {
            largest = arr[i];
        }
    }

    printf("The largest number is: %d\n\n", largest);

    printf("Counting Vowels in a String\n");
    printf("Enter a word or sentence: ");
    getchar(); 
    fgets(text, sizeof(text), stdin);

    for (i = 0; text[i] != '\0'; i++) {
        switch (text[i]) {
            case 'a': case 'e': case 'i': case 'o': case 'u':
            case 'A': case 'E': case 'I': case 'O': case 'U':
                vowelCount++;
                break;
        }
    }

    printf("The number of vowels is: %d\n", vowelCount);

    return 0;
}
