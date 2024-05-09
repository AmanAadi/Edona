# Edona - Encryptor Decryptor
EDONA is a password encryptor and decryptor tool written in Python3.
- It uses a secret key to encrypt and decrypt passwords.
- You have to remember the secret key that you use to encrypt the password.
- Secret key help to decrypt the encrypted password.
- You don't need to copy the encrypted or decrypted password manually as It gets copied automatically.


### Video Demo: 
[![Edona Demo video](https://img.youtube.com/vi/f5o5bD9033M/0.jpg)](https://www.youtube.com/watch?v=f5o5bD9033M)


### Idea of this project:
When we save a password directly in a file on our computer. It is a security threat to us because, what if our computer gets hacked and the data is stolen? Then the attacker can use our password to perform malicious actions.

But when you encrypt the password and then save it in a file. Then there will be no security issue because, the password can only be decrypted using the secret PIN that you have set for that password.


## Requirements:
* Python3
* Install all required modules:
```pip install -r requirements.txt```


## How to use:
1. Input a pin (It should only contain numbers).
2. Input a password or any data.
3. Click on 'encrypt' to encrypt the password using the pin.
4. Click on 'decrypt' to decrypt the password using the pin.
* Note: It automatically copy the encrepted or decrypted password. so you don't need to copy manually. 


## Encoding process:
* Take input string from user.
* Take a secret pin from the user.
* Encode the input string to base64.
* Split the base64 encoded string in the length number of pin. ex: if user input 32 then its length is 2 therefore base64 string or password is split into two parts.
* Replace the character with its pin digit from letters. ex: as 3 is first character of 32, therefore each character of the first part of base64 string or passsword is exceed by that value. ('a' becomes 'd').


## Decoding process:
* Take encrypted string or password from user.
* Take a secret pin from the user that user use to encrypt the password previously.
* Split the encrypted password in the length number of secret pin.
* Restore the character throuch pin value. ex: as 3 is first character of 32, therefore each character of the first part of base64 string or passsword is back to the value. ('d' becomes 'a').

