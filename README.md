# SSH Tutorial

* Generate new SSH
```
    ssh-keygen -t rsa -b 4096 -C "your_email@youremail.com"
```
* In order to push into repository with specific RSA_KEY
```
    GIT_SSH_COMMAND='ssh -i ~/.ssh/<RSA-PRIVATE-KEY> -o IdentitiesOnly=yes' git push origin master
```
* Check keys
```
    ssh-add -l
```
* Delete all cached before
```
    ssh-add -D
```
