```
~/projekt [ ansible-playbook -i inv.yaml -l wordpress web.yaml

PLAY [all_hosts] ***************************************************************

TASK [Gathering Facts] *********************************************************
ok: [wordpress]

TASK [install python 2] ********************************************************
changed: [wordpress]

PLAY [wordpress] ***************************************************************

TASK [Gathering Facts] *********************************************************
ok: [wordpress]

TASK [server : Update apt cache] ***********************************************
changed: [wordpress]

TASK [server : Install required software] **************************************
ok: [wordpress] => (item=[u'apache2', u'mysql-server', u'php-mysql', u'php', u'l                                                                                                                               ibapache2-mod-php', u'python-mysqldb'])

TASK [php : Install php extensions] ********************************************
ok: [wordpress] => (item=[u'php-gd', u'php-ssh2'])

TASK [mysql : Create mysql database] *******************************************
ok: [wordpress]

TASK [mysql : Create mysql user] ***********************************************
ok: [wordpress]

TASK [wordpress : Download WordPress] ******************************************
changed: [wordpress]

TASK [wordpress : Extract WordPress] *******************************************
changed: [wordpress]

TASK [wordpress : Update default Apache site] **********************************
changed: [wordpress]

TASK [wordpress : Set the correct permissions on Wordpress directories] ********
changed: [wordpress]

TASK [wordpress : Set the correct permissions for Wordpress files] *************
changed: [wordpress]

TASK [wordpress : Copy wp-config] **********************************************
ok: [wordpress]

RUNNING HANDLER [wordpress : restart apache] ***********************************
changed: [wordpress]

PLAY RECAP *********************************************************************
wordpress                  : ok=15   changed=8    unreachable=0    failed=0    s                                                                                                                               kipped=0    rescued=0    ignored=0
```
