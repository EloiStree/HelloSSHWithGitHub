# HelloSSHWithGitHub
I am tired of forgeting how to setup SSH for GitHub. Let's note the steps.


------------------


# HelloSSHWithGitHub
I am tired of forgeting how to setup SSH for GitHub. Let's note the steps.


## Solo Account 

https://youtu.be/vExsOTgIOGw

```
ssh-keygen -t ed25519 -C "mail@gmail.com"
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_ed25519
clip <~/.ssh/id_ed25519.pub
```

## Multi Account

https://youtu.be/N2hMGEeYR7c

```
// Example for a first account
cd .ssh
ssh-keygen
cat id_rsa.pub
// Copy the key to github
// Create config file in ssh
notepad config
--- In file 
#Account Eloi
Host github.com
 HostName github.com
 IdentityFile ~/.ssh/id_rsa
--- In File
mv config.txt config


// Example for a multi account
ssh-keygen -f aliasName_id_rsa
```

