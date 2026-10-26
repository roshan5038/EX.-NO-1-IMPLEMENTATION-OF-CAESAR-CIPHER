# EX. NO: 1 : IMPLEMENTATION OF CAESAR CIPHER

## AIM:
To implement the simple substitution technique named Caesar cipher using C language.

## ALOGORITHM:

STEP-1: Read the plain text from the user.

STEP-2: Read the key value from the user.

STEP-3: If the key is positive then encrypt the text by adding the key with each character in the plain text.

STEP-4: Else subtract the key from the plain text.

STEP-5: Display the cipher text obtained above.
***Name:Roshan V***

***Reg no:212225240124***

## PROGRAM:
```
#include <stdio.h>
#include <string.h>

int main()
{
    char text[100], encrypt[100], decrypt[100];
    int key, i;

    printf("Enter the plain text: ");
    fgets(text, sizeof(text), stdin);
    text[strcspn(text, "\n")] = '\0';

    printf("Enter the key value: ");
    scanf("%d", &key);

    
    for(i = 0; text[i] != '\0'; i++)
    {
        if(text[i] >= 'a' && text[i] <= 'z')
            encrypt[i] = (text[i] - 'a' + key) % 26 + 'a';
        else if(text[i] >= 'A' && text[i] <= 'Z')
            encrypt[i] = (text[i] - 'A' + key) % 26 + 'A';
        else
            encrypt[i] = text[i];
    }
    encrypt[i] = '\0';

    
    for(i = 0; encrypt[i] != '\0'; i++)
    {
        if(encrypt[i] >= 'a' && encrypt[i] <= 'z')
            decrypt[i] = (encrypt[i] - 'a' - key + 26) % 26 + 'a';
        else if(encrypt[i] >= 'A' && encrypt[i] <= 'Z')
            decrypt[i] = (encrypt[i] - 'A' - key + 26) % 26 + 'A';
        else
            decrypt[i] = encrypt[i];
    }
    decrypt[i] = '\0';

    printf("\nPlain Text     : %s", text);
    printf("\nEncrypted Text : %s", encrypt);
    printf("\nDecrypted Text : %s", decrypt);

    return 0;
}
```
## OUTPUT:
<img width="362" height="342" alt="Screenshot 2026-10-26 102351" src="https://github.com/user-attachments/assets/23d903c3-a9a6-4a86-af25-fef54e9808ee" />

<img width="362" height="342" alt="Screenshot 2026-10-26 102351" src="https://github.com/user-attachments/assets/98641e9c-d303-47b3-a028-2ba3fbae990a" />


## RESULT :
 Thus the implementation of ceasar cipher had been executed successfully.
