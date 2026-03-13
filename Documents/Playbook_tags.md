~/ansible_learning$ ansible-playbook --list-tags site_v2.yml

playbook: site_v2.yml

  play #1 (all): all    TAGS: []
      TASK TAGS: [always]

  play #2 (web_servers): web_servers    TAGS: []
      TASK TAGS: [apache, httpd, redhat, ubuntu]

  play #3 (db_servers): db_servers      TAGS: []
      TASK TAGS: [db, mariadb, redhat, ubuntu]

  play #4 (file_servers): file_servers  TAGS: []
      TASK TAGS: [samba]
