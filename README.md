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

'Config' file in SSH
```
#Account EloiStree
Host github.com-eloistree
 HostName github.com
 IdentityFile ~/.ssh/eloistree_id_rsa

#Account OMI
Host github.com-omi
 HostName github.com
 IdentityFile ~/.ssh/omi_id_rsa

#Account EloiStree3D
Host github.com-eloistree3D
 HostName github.com
 IdentityFile ~/.ssh/eloistree3d_id_rsa

#Account Drone XR
Host github.com-dronexr
 HostName github.com
 IdentityFile ~/.ssh/dronexr_id_rsa

```

Install git on your computer and launch Git BASH
```
cd .ssh
ssh-keygen -t ed25519 -f acountname_id_rsa -C "accountname@gmail.com"
cat gitaccount_id_rsa.pub
```
Then add the text to the Github Account and use 
Exemple : `git@github.com-omi:OpenMacroInput/2022_07_21_INamedBoolean.git`

![image](https://user-images.githubusercontent.com/20149493/219948869-2a80d12d-9fbf-44c6-b021-213c920e9089.png)




