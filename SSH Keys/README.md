# Adding SSH Keys to your Github Account

## Accessing the Public Key
You have to copy the contents of your public key.
```
cd ~/.ssh
cat id_rsa.pub
```
Copy the contents of your public key.

## Setting up the key in Github Account
Click on to your account at top-right corner `Account > Setting > SSH and GPG Keys > New SSH Key` <br>
Set a title to identify the computer to which the public key belongs to and then paste the contents of `id_rsa.pub` in key. After that enter your github password to add the key.

