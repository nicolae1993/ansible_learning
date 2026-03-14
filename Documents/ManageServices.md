```bash
ansible-playbook --ask-become-pass site_services.yml

TASK [start httpd (Centos)] *************************************************************************************************************************

skipping: [172.31.44.126]

skipping: [172.31.44.135]

changed: [172.31.42.76]
``` 


site_services.yml

```yaml
   - name: start httpd (Centos)
      tags: apache,redhat,httpd
      service:
          name: httpd
          state: started
      when: ansible_distribution == "RedHat"

    - name: copy default html file for site
      tags: apache,apache2,httpd
      copy:
       src: default_site.html
       dest: /var/www/html/index.html
       owner: root
       group: root
       mode: 06
```
