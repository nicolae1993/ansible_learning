# ansible_learning

This is my awesome Ansible repository!

Generate public+privare key on the Ansible Server Workstation
Copy the public key /home/user/.ssh/authorized_keys
<img width="385" height="42" alt="image" src="https://github.com/user-attachments/assets/e4235df6-000f-4907-ad16-af73e574a7bd" />



Copy public key in Github Settings -- SSH and GPG keys at SSH keys


Download on the Ansible server the github
git clone https://github.com/nicolae1993/ansible_learning.git

git config --global user.name "nicolae1993"
git config --global user.email "nicolae_stan93@yahoo.com"

cat ~/.gitconfig
[user]
        name = nicolae1993
        email = nicolae_stan93@yahoo.com

git remote set-url origin git@github.com:nicolae1993/ansible_learning.git
git push origin main
