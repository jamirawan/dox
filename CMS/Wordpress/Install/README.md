---
layout: default
title: Install Wordpress
parent: Wordpress
grand_parent: CMS
nav_order: 1
has_children: false
has_toc: true

---
# Install locally with DDEV

For this, you will only need
* Git
* Docker
* Terminal or some sort
* Code editor

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

#Configure database credentials: DB_NAME; DB_USER; DB_PASSWORD;
ddev mysql 

#Launch the site
ddev start

# Or you can create bedrock
ddev composer create roots/bedrock
```
*You can access the MySQL phpMyAdmin via port 8037:*

https://wp.ddev.site:8037/db_structure.php?server=1&db=db

```bash
Starting wp... 
v1.16.6: Pulling from drud/ddev-webserver
aa935f1478c2: Pull complete 
Digest: sha256:427431af678eb6aa6d144da28b190e065a9b8b467fa7d5814a4300c46421ad15
Status: Downloaded newer image for drud/ddev-webserver:v1.16.6
docker.io/drud/ddev-webserver:v1.16.6
v1.16.2: Pulling from drud/ddev-router
852e50cd189d: Already exists 
a9d81f536096: Pull complete 
f0ed0b709232: Pull complete 
5b8f22c6d2f4: Pull complete 
32bfd22d29be: Pull complete 
0d0b503f4f5d: Pull complete 
e079beac713f: Pull complete 
ecf9babaabbd: Pull complete 
e31872daac11: Pull complete 
1cc8d85bdd61: Pull complete 
9cacd080ec99: Pull complete 
ae5915eed897: Pull complete 
3a6288e65659: Pull complete 
0d00339a5544: Pull complete 
f327efbdb21c: Pull complete 
2efc7a66c1e3: Pull complete 
Digest: sha256:c743ef28342cd109d1611a25b31eb1c3306914fdbefcd1c4db84fda4ac8a6ce4
Status: Downloaded newer image for drud/ddev-router:v1.16.2
docker.io/drud/ddev-router:v1.16.2
v1.16.0: Pulling from drud/ddev-dbserver-mariadb-10.2
171857c49d0f: Pull complete 
419640447d26: Pull complete 
61e52f862619: Pull complete 
928020f0412e: Pull complete 
f9b22d867bcc: Pull complete 
1b5f9e2cc9e3: Pull complete 
c978fcde1334: Pull complete 
fd4d9e93f2fb: Pull complete 
92d8ee36e7ef: Pull complete 
5bb4a3b88960: Pull complete 
a8c8203bfbec: Pull complete 
aa577d2ceeeb: Pull complete 
d82880dc0eb7: Pull complete 
db9aecaf009d: Pull complete 
f03de15eaca5: Pull complete 
9fb8be7ac41b: Pull complete 
efa19fd83e0e: Pull complete 
c2be885f155a: Pull complete 
8f0a7d77fd38: Pull complete 
da0d36f85d5d: Pull complete 
28307cb0745f: Pull complete 
a0c38ab11057: Pull complete 
4bdae4666bab: Pull complete 
8f46afc5f64b: Pull complete 
Digest: sha256:1f9108ee69733e4874798dab844dd8c68d2b497e6dac49002b1de5e07aa4b743
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