# Sail

Sail is the `drush` or `wp-cli` equivalent for Laravel which is a light-weight CLI. `sail` is store in `docker-compose.yml` in the project root.

## Install

Install `sail` with Composer:

```terminal
composer require laravel/sail --dev
```

After Sail has been installed, you may run the sail:install Artisan command. This command will publish Sail's docker-compose.yml file to the root of your application:

```terminal
php artisan sail:install
```
By default, to run the sail it's : `.vendor/bin/sail up -d`

## Setup alias

Instead of typing all those path, you should make an alias on the bash profile. Run these command and you don't have to edit the .bash profile:

```terminal
export COMPOSE_FILE=docker-compose.yml
alias sail='bash vendor/bin/sail'
```

## Commands
### Start & stop
Start: 
```terminal
sail up
```

Start with `detached mode`:
```terminal
sail up -d
```

To stop all containers:
```terminal
sail down
```

### Executing

