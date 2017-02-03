# ansible-semaphore

Create a docker container using docker-compose.xml in repository.

1. using terminal , connect to semaphore.
2. Create a playbook directory for "ansible".
3. mysql setup
  - change root privilges - enable remote access
4. In semaphore container
  - test mysql connection. :)  [mysql -h mysql -u root -p]
5. semaphore setup
```
  ~/>  semaphore --setup
 Hello! You will now be guided through a setup to:
   1. Set up configuration for a MySQL/MariaDB database
   2. Set up a path for your playbooks (auto-created)
   3. Run database Migrations
   4. Set up initial seamphore user & password

   > DB Hostname (default 127.0.0.1:3306): mysql:3306
   > DB User (default root):
   > DB Password: MUST_BE_CHANGE_PASSWORD
   > DB Name (default semaphore):
   > Playbook path:  MUST_BE_CHANGE_PLAYBOOK_PATH
   
   Generated configuration:
   {
          "mysql": {
                  "host": "mysql:3306",
                  "user": "root",
                  "pass": "MUST_BE_CHANGE_PASSWORD",
                  "name": "semaphore"
          },
          "port": "",
          "bugsnag_key": "",
          "tmp_path": "/tmp/semaphore",
          "cookie_hash": "x30Ap4e1UuT166oL/XXXXXXXXXXXXXXXX=",
          "cookie_encryption": "pTN+Ycq+XXXXXXXXXXXX+E+DIuZPxxIipk="
   }

 > Is this correct? (yes/no):
``` 
 6. playbook config check.
 7. Run semaphore
  semaphore -config /tmp/semaphore/semaphore_config.json
  
  
  
   
