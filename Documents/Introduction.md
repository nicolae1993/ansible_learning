


Create 3 EC2 instances in AWS. 
workstation Ansible server.
the other three  (srv1 & srv2 & srv3) are for provisioning from workstion.

<img width="1267" height="223" alt="image" src="https://github.com/user-attachments/assets/9ed5e3f2-bd08-4cb2-b6ee-4bcc3d45827b" />



On the Ansible Server Workstation Generate  public+privare key
ssh-keygen -t ed25519

Present here after generation of files /home/ubuntu/.ssh
id_ed25519 and  id_ed25519.pub
<img width="787" height="97" alt="image" src="https://github.com/user-attachments/assets/3e9d8d48-b83e-4973-83a7-b142da1dfa5b" />


Copy the public key into the "Slave Ansible Machines" /home/user/.ssh/authorized_keys 
so we can do ssh without password
<img width="385" height="42" alt="image" src="https://github.com/user-attachments/assets/e4235df6-000f-4907-ad16-af73e574a7bd" />



Copy public key from Ansible Master Server into Github Settings -- SSH and GPG keys at SSH keys
<img width="1444" height="448" alt="image" src="https://github.com/user-attachments/assets/2aab2fcc-23af-437a-9069-a2abfa9dde22" />



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


First command with private IPs from AWS slaves servers
ansible all --key-file ~/.ssh/id_ed25519 -i inventory -m ping

<img width="1342" height="381" alt="image" src="https://github.com/user-attachments/assets/0a01b9b6-150d-451d-aed4-e70975d0e878" />



After declaring this 

<img width="818" height="103" alt="image" src="https://github.com/user-attachments/assets/2aeb3a70-4eaa-4541-9adb-cae9f7802954" />

We can use directly the command 
ansible all -m ping

<img width="792" height="384" alt="image" src="https://github.com/user-attachments/assets/eec7ab3f-d7e6-4112-bc38-d085f2f562f4" />




