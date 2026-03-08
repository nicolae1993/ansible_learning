ansible all --list-hosts

<img width="880" height="123" alt="image" src="https://github.com/user-attachments/assets/186b4683-2b68-4521-aec8-e4878c8cfa31" />




ansible all -m gather_facts --limit 172.31.44.126
<img width="1202" height="372" alt="image" src="https://github.com/user-attachments/assets/3dfa3e04-e40c-4909-a1f9-39099cfc7a8b" />



ansible all -m apt -a update_cache=true --become --ask-become-pass
<img width="1418" height="130" alt="image" src="https://github.com/user-attachments/assets/6097d240-7529-4750-a071-a9f3309dfd30" />

<img width="1413" height="470" alt="image" src="https://github.com/user-attachments/assets/13e47f3b-94b1-44bf-9b40-d96d81c80b6e" />




