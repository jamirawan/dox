---
layout: default
title: Install Wordpress
parent: Wordpress
grand_parent: CMS
nav_order: 1
has_children: false
has_toc: true

---
# Install locally with DDEV (Mac OS)

For this, you will only need
* Docker
* Terminal or some sort
* Code editor
* Git if you wish to make the workflow

**Install DDEV with brew if you haven't already**

```md
brew tap drud/ddev && brew install ddev 
```

## Setup project

Start the Docker engine and ensure it's not being used anywhere else

```bash
# Create a working folder e.g my-wp-site
mkdir my-wp-site

# Go to new directory
cd my-wp-site

# Configuring the site
ddev config --project-type=wordpress --docroot=web --create-docroot

#Ensure all Docker containers are not running 
docker stop $(docker ps -a -q) 

# Start the engine site
ddev start

# And launch the rocket

ddev launch

```

This should take you to the Wordpress standard install and ask you to choose language and admin user with password. Once you finished this, you dont have to add database details.


*If you wish to access the MySQL phpMyAdmin you can go via port 8037:*

**https://wp.ddev.site:8037/db_structure.php?server=1&db=db**

Here's the successfull initiation look like. The last lines are where your local WP install is. 

**Have fun!**

```bash
Starting wp... 
v1.16.6: Pulling from drud/ddev-webserver
aa935f1478c2: Pull complete 
Digest: sha256:427431af678eb6aa6d144da28b190e065a9b8b467fa7d5814a4300c46421ad15
Status: Downloaded newer image for drud/ddev-webserver:v1.16.6
docker.io/drud/ddev-webserver:v1.16.6
v1.16.2: Pulling from drud/ddev-router
852ed50cd189d: Already exists 
a9d8d1f536096: Pull complete 
f0edd0b709232: Pull complete 
5b8fd22c6d2f4: Pull complete 
32bfdd22d29be: Pull complete 
0d0bd503f4f5d: Pull complete 
e079dbeac713f: Pull complete 
ecf9bdabaabbd: Pull complete 
e3187d2daac11: Pull complete 
1cc8dd85bdd61: Pull complete 
9cacd0d80ec99: Pull complete 
ae5915deed897: Pull complete 
3a6288de65659: Pull complete 
0d0033d9a5544: Pull complete 
f327efdbdb21c: Pull complete 
2efc7ad66c1e3: Pull complete 
Digest: sha256:c743ef28342cd109d1611a25b31eb1c3306914fdbefcd1c4db84fda4ac8a6ce4
Status: Downloaded newer image for drud/ddev-router:v1.16.2
docker.io/drud/ddev-router:v1.16.2
v1.16.0: Pulling from drud/ddev-dbserver-mariadb-10.2
171857dc49d0f: Pull complete 
419640d447d26: Pull complete 
61e52fd862619: Pull complete 
92802d0f0412e: Pull complete 
f9b22cd867bcc: Pull complete 
1b5f9ce2cc9e3: Pull complete 
c978fccde1334: Pull complete 
fd4d9ec93f2fb: Pull complete 
92d8eec36e7ef: Pull complete 
5bb4a3cb88960: Pull complete 
a8c820c3bfbec: Pull complete 
aa577dc2ceeeb: Pull complete 
d82880dcc0eb7: Pull complete 
db9aeccaf009d: Pull complete 
f03de1c5eaca5: Pull complete 
9fb8bec7ac41b: Pull complete 
efa19fcd83e0e: Pull complete 
c2be88c5f155a: Pull complete 
8f0a7dc77fd38: Pull complete 
da0d3c6f85d5d: Pull complete 
28307ccb0745f: Pull complete 
a0c38cab11057: Pull complete 
4bdace4666bab: Pull complete 
8f46cafc5f64b: Pull complete 
Digest: sha256:1f9108cee6c9733ec4c874798dab844dd8c68d2b497e6dac49002b1de5e07aa4b743
Status: Downloaded newer image for drud/ddev-dbserver-mariadb-10.2:v1.16.0
docker.io/drud/ddev-dbserver-mariadb-10.2:v1.16.0
Building ddev-ssh-agent 
Recreating ddev-ssh-agent ... done
 
ssh-agent container is running: If you want to add authentication to the ssh-agent container, run 'ddev auth ssh' to enable your keys. 
Creating volume "wp-mariadb" with default driver 
Building db 
Building web 
Creating ddev-wp-db ... done
Creating ddev-wp-dba ... done
Creating ddev-wp-web ... done
 
Recreating ddev-router ... done
 
Successfully started wp 
Project can be reached at https://wp.ddev.site https://127.0.0.1:55005 
```