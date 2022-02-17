# SSH Tutorial

* Generate new SSH
```
    ssh-keygen -t rsa -b 4096 -C "your_email@youremail.com"
```
* In order to push into repository with specific RSA_KEY
```bash
    GIT_SSH_COMMAND='ssh -i ~/.ssh/<RSA-PRIVATE-KEY> -o IdentitiesOnly=yes' git push origin master
```
* Another way, type into current git repository
```bash
    git config core.sshCommand 'ssh -i ~/.ssh/<RSA-PRIVATE-KEY>'
```
* Check keys
```bash
    ssh-add -l
```
* Delete all cached before
```bash
    ssh-add -D
```
* In order to clone different repos, create file `config` in ~/.ssh folder
```bash
    touch config
```
```
    # COMPANY NAME 1
    Host company1
            HostName github.com
            User git
            IdentityFile ~/.ssh/id_rsa
            IdentitiesOnly yes
    
    # COMPANY NAME 2
    Host company2
            HostName github.com
            User git
            IdentityFile ~/.ssh/id_gmail_rsa
            IdentitiesOnly yes
```
* Check access
```bash
    ssh -T git@company1
    ssh -T git@company2
```