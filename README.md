## Ansible part
```
cd ansible/
vagrant up
```
`Vagrantfile` describes the box and the provisioning part of it.
Inside of `mariadb` folder is a simple play, that will use `ansible-vault` to get credentials for MariaDB. 

One thing you'd need is to create a password-file at `ansible/ansible-vault-password.yml` and put the Vault password into it (I will provide the password thru email).

Not ideal, but secure and nothing is stored in plain text.


## Jenkinsfile
There is one prerequisite - Jenkins has to be setup with Docker-in-Docker. Makes it easier to build Python (or other) projects, that need tons of dependencies and all. Keeps it clean.

To run this, just load the code from Jenkinsfile into Pipeline job. Or add this repo as `scm` source and point to `jenkins/Jenkinsfine`.

Resulting in:
```
Hello, world!
Your IP address is: 80.56.18.65
You succesfully ran this script!
```