# Installation

# On Mac

## Install
As long as you have Docker in your Mac you can run simple `CURL` command to start creating project. `web-app` is an example of your project URL you can customise:
```
curl -s https://laravel.build/web-app | bash
```

## Sail up!
Go to the directory `cd web-app` after the installation done and we can start running the Laravel Sail that providfe a simple CLI for interacting with Laravel's default Docker configuration:

```terminal
docker-compose up -d
#or
./vendor/bin/sail up - d
```


Ensure that the port you are using, by default it's :80, is not in use by other Docker containers. If it's already used and the following error came up, you can change the port number or kill other containers first:

### Check who uses port (number)
Run this to check who's using the port number you wish to list:

```
sudo lsof -i -P -n | grep <port number> 
```

### Change port
```terminal
ERROR: for mailhog  Cannot start service mailhog: driver failed programming external connectivity on endpoint web-app_mailhog_1 (ae8085daf269cf4a0f7eae07927d10a0975d5ae3a082659314663956afce36c1): Error starting userland proxy: listen tcp4 0.0.0.0:8025: bind: address already in use

ERROR: for laravel.test  Cannot start service laravel.test: Ports are not available: listen tcp 0.0.0.0:80: bind: address already in use
```
You can change the port number
Change to other ports by editing the `docker-compose.yml` file:
```yml
    ports:
      - "8084:80"
```
And try to use port 8084 instaed `http://localhost:8084`

### Stop and remove containers

```
docker-compose down  # Stop container on current dir if there is a docker-compose.yml
```

And then run the up the sail again: `./vendor/bin/sail up`
