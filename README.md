# EX. NO: 1(A) : IMPLEMENTATION OF CAESAR CIPHER

## AIM:
To implement the simple substitution technique named Caesar cipher using C language.

## ALOGORITHM:

STEP-1: Read the plain text from the user.

STEP-2: Read the key value from the user.

STEP-3: If the key is positive then encrypt the text by adding the key with each character in the plain text.

STEP-4: Else subtract the key from the plain text.

STEP-5: Display the cipher text obtained above.

## PROGRAM:
```
#include <stdio.h>
#include <string.h>
#include <ctype.h>

void caesar_cipher(char* text, int shift) {
    int i;
    char ch;

    for (i = 0; text[i] != '\0'; ++i) {
        ch = text[i];

        // Check if the character is an uppercase letter
        if (isupper(ch)) {
            text[i] = (ch + shift - 'A') % 26 + 'A';
        }
        // Check if the character is a lowercase letter
        else if (islower(ch)) {
            text[i] = (ch + shift - 'a') % 26 + 'a';
        }
    }
}

int main() {
    char text[100];
    int shift;

    printf("Enter a string: ");
    fgets(text, sizeof(text), stdin);

    printf("Enter shift amount: ");
    scanf("%d", &shift);

    // Apply Caesar cipher
    caesar_cipher(text, shift);

    printf("Encrypted text: %s\n", text);

    return 0;
}
```

## OUTPUT:
![image](https://github.com/user-attachments/assets/17b1bc68-77be-4c45-903e-83852b4de593)


## RESULT :
 Thus the implementation of ceasar cipher had been executed successfully.
