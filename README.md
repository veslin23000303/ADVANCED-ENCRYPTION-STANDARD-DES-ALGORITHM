EX-4-ADVANCED-ENCRYPTION-STANDARD-DES-ALGORITHM
## Aim:
To use Advanced Encryption Standard (AES) Algorithm for a practical application like URL Encryption.

## ALGORITHM:
AES is based on a design principle known as a substitution–permutation.
AES does not use a Feistel network like DES, it uses variant of Rijndael.
It has a fixed block size of 128 bits, and a key size of 128, 192, or 256 bits.
AES operates on a 4 × 4 column-major order array of bytes, termed the state
## PROGRAM:
```
NAME:VESLIN ANISH A
REGNO:212223240175
#include <stdio.h>
#include <string.h>


  void xor_encrypt_decrypt(char *input, char *key) {
int input_len = strlen(input);
int key_len = strlen(key);

for (int i = 0; i < input_len; i++) {
    input[i] = input[i] ^ key[i % key_len]; 
}
}

int main() {
char url[] = "https://lms2.cse.saveetha.in";
char key[] = "secretkey"; 

printf("Original URL: %s\n", url);

xor_encrypt_decrypt(url, key);
printf("Encrypted URL: %s\n", url);

xor_encrypt_decrypt(url, key);
printf("Decrypted URL: %s\n", url);

return 0;
}
```
## OUTPUT:
![Screenshot 2024-10-09 161149](https://github.com/user-attachments/assets/e27aee71-fc6e-4b27-ada1-fb05f3ee3941)

## RESULT:
The program for implementing DES encryption and decryption is executed successfully.
