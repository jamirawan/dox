# Installation

# On Mac

## Install

### Install With `curl`
As long as you have Docker in your Mac you can run simple `CURL` command to start creating project. `web-app` is an example of your project URL you can customise:
```terminal
curl -s https://laravel.build/web-app | bash
```
### Install with Composer

```terminal
composer create-project laravel/laravel 
# or with Laravel Installer web-app
composer global require laravel/installer
laravel new web-app
# then go to the web-ap folder
cd web-app
php artisan serve
```

## Sail up!
Go to the directory `cd web-app` after the installation done and we can start running the Laravel Sail that providfe a simple CLI for interacting with Laravel's default Docker configuration:

```terminal
docker-compose up -d
#or
./vendor/bin/sail up - d
```

With alias setup: `sail up -d` (refer to 'Sail' section for alias setup)


Ensure that the port you are using, by default it's :80, is not in use by other Docker containers. If it's already used and the following error came up, you can change the port number or kill other containers first:

### Check who uses port (number)
Run this to check who's using the port number you wish to list:

```terminal
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

```terminal
docker-compose down  # Stop container on current dir if there is a docker-compose.yml
```

And then run the up the sail again: `./vendor/bin/sail up` or `sail up -d` if you have your alias setup. 

This may take a few minutes but you'll see this line where you can check your web app:
```terminal
laravel.test_1  | Starting Laravel development server: http://0.0.0.0:80
```

So your project web local web app is: `http://0.0.0.0:80` or just `localhost`
