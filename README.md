


Create 3 EC2 instances in AWS. 
workstation Ansible server.
the other two (srv1 & srv2) are for provisioning from workstion.

<img width="426" height="141" alt="image" src="https://github.com/user-attachments/assets/b2c909c2-e33a-48cc-9829-71598601f898" />


On the Ansible Server Workstation Generate  public+privare key
ssh-keygen -t ed25519

Present here after generation of files /home/ubuntu/.ssh
id_ed25519 and  id_ed25519.pub
<img width="787" height="97" alt="image" src="https://github.com/user-attachments/assets/3e9d8d48-b83e-4973-83a7-b142da1dfa5b" />


Copy the public key into the "Slave Ansible Machines" /home/user/.ssh/authorized_keys 
so we can do ssh without password
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
