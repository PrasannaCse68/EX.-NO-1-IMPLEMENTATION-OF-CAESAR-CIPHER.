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
```python
def caesar_cipher(text, key):
    key = int(key)
    cipher_text = ""

    for char in text:
        if char.isalpha():
            shift = key % 26
            if char.islower():
                cipher_text += chr((ord(char) - ord('a') + shift) % 26 + ord('a'))
            elif char.isupper():
                cipher_text += chr((ord(char) - ord('A') + shift) % 26 + ord('A'))
        else:
            cipher_text += char

    return cipher_text

plain_text = input("Enter the plain text: ")
key = int(input("Enter the key value: "))
cipher_text = caesar_cipher(plain_text, key)
print("Cipher Text:", cipher_text)

```

## OUTPUT:
![Screenshot 2024-08-19 144308](https://github.com/user-attachments/assets/1ee9d52d-bfa6-42a9-9fd4-00940ae88222)


## RESULT :
 Thus the implementation of ceasar cipher had been executed successfully.
