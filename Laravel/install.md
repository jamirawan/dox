# Installation

# On Mac

As long as you have Docker in your Mac you can run simple `CURL` command to start creating project. `web-app` is an example of your project URL you can customise:
```Mac-CLI
curl -s https://laravel.build/web-app | bash
```

Go to the directory `cd web-app` after the installation done and we can start running the Laravel Sail that providfe a simple CLI for interacting with Laravel's default Docker configuration:
```Mac-CLI
./vendor/bin/sail up
```