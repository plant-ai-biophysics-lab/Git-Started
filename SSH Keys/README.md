# Adding SSH Keys to your Github Account

## SSH Setup (Optional)
```
cd ~/.ssh
ls -al
```
If ssh already exists, `id_rsa` and `id_rsa.pub` will be displayed if not you have to generate your keys.

```
cd ~
mkdir .ssh
cd .ssh
```
Generate ssh keys

```
ssh-keygen -t rsa
```

You'll be prompted to enter a passphrase and then re-enter it. You can leave the passphrase blank for quick access but it is highly recommended to use one. After this you can check your keys using

```
ls -al
```


## Accessing Public Key
```
cd ~/.ssh
cat id_rsa.pub
```
Copy the contents of your public key.

## Adding Key
Click on your account in the upper-right corner. Go to `Account > Setting > SSH and GPG Keys > New SSH Key` <br>

<img src="./.assets/new_SSH_keys.jpg" alt="sample" width="600"/>

Set a title to identify the computer that has the public key, and then paste the contents of 'id rsa.pub' into key. Then, to add the key, enter your github password.

## Checking Github Access
```
cd ~/.ssh
ssh -T git@github.com
```

If everything is set-up correctly you'll be prompted with "Are you sure to continue connecting", type `yes`. After that enter your passphrase, to which a message referring to your github username will popup.

<img src="./.assets/check.jpg" alt="check" width="700"/>
