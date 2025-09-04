## EX. NO: 1 : IMPLEMENTATION OF CAESAR CIPHER
 

## AIM:

To implement the simple substitution technique named Caesar cipher using C language.

## DESCRIPTION:

To encrypt a message with a Caesar cipher, each letter in the message is changed using a simple rule: shift by three. Each letter is replaced by the letter three letters ahead in the alphabet. A becomes D, B becomes E, and so on. For the last letters, we can think of the
alphabet as a circle and "wrap around". W becomes Z, X becomes A, Y bec mes B, and Z
becomes C. To change a message back, each letter is replaced by the one three before it.

## EXAMPLE:



![image](https://github.com/Hemamanigandan/CNS/assets/149653568/eb9c6c43-8c80-4cdd-b9d4-91705a311c79)

## ALGORITHM:

### STEP-1: Read the plain text from the user.
### STEP-2: Read the key value from the user.
### STEP-3: If the key is positive then encrypt the text by adding the key with each character in the plain text.
### STEP-4: Else subtract the key from the plain text.
### STEP-5: Display the cipher text obtained above.

## PROGRAM:
```
def caesar_encrypt(text, key):
    result = ""
    for c in text:
        if c.isupper():
            result += chr(((ord(c) - ord('A') + key) % 26) + ord('A'))
        elif c.islower():
            result += chr(((ord(c) - ord('a') + key) % 26) + ord('a'))
        else:
            result += c  # keep non-alphabet characters unchanged
    return result

def caesar_decrypt(text, key):
    return caesar_encrypt(text, -key)

# Main program
message = input("Enter the message to encrypt: ")
key = int(input("Enter the Caesar Cipher key (an integer): "))

encrypted = caesar_encrypt(message, key)
print("Encrypted Message:", encrypted)

decrypted = caesar_decrypt(encrypted, key)
print("Decrypted Message:", decrypted)

```
## OUTPUT :
<img width="646" height="226" alt="image" src="https://github.com/user-attachments/assets/2d14fe7f-dfdb-4c14-bcd9-774149eac9ef" />

RESULT:
The program is executed successfully
