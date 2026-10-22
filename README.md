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
Developed By Siddharth CM(212225040413)
#include <stdio.h>

int main() {
    char text[100], ET[100], DT[100];
    int key, i;

    printf("plaintext: ");
    fgets(text, sizeof(text), stdin);

    printf("key: ");
    scanf("%d", &key);

    key = ((key % 26) + 26) % 26;

    for (i = 0; text[i] != '\0'; i++) {
        if (text[i] >= 'A' && text[i] <= 'Z')
            ET[i] = (text[i] - 'A' + key) % 26 + 'A';
        else if (text[i] >= 'a' && text[i] <= 'z')
            ET[i] = (text[i] - 'a' + key) % 26 + 'a';
        else
            ET[i] = text[i];
    }
    ET[i] = '\0';

    for (i = 0; ET[i] != '\0'; i++) {
        if (ET[i] >= 'A' && ET[i] <= 'Z')
            DT[i] = (ET[i] - 'A' - key + 26) % 26 + 'A';
        else if (ET[i] >= 'a' && ET[i] <= 'z')
            DT[i] = (ET[i] - 'a' - key + 26) % 26 + 'a';
        else
            DT[i] = ET[i];
    }
    DT[i] = '\0';

    printf("Encrypted text: %s", ET);
    printf("Decrypted text: %s", DT);

    return 0;
}
```
## OUTPUT:

<img width="1535" height="704" alt="image" src="https://github.com/user-attachments/assets/d0d12d33-b6a0-422c-8d52-54606b277f2e" />

## RESULT :
 Thus the implementation of ceasar cipher had been executed successfully.
