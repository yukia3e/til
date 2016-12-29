# Generating a new SSH key

1. Open Terminal.

2. Paste the text below, substituting in your email address.  This creates a new ssh key, using the provided email as a label.
```
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
```

3. When you're prompted to "Enter a file in which to save the key," press Enter. This accepts the default file location.

4. At the prompt, type a secure passphrase.

5. Add your SSH key
```
sh-add ~/.ssh/id_rsa
```

6. modify .ssh/config
```
$ vim ~/.ssh/config
Host github.com
    IdentityFile ~/.ssh/github_id_rsa
```
