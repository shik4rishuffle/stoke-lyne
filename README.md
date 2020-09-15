#   CMS template

Duplicate this repo for a quick and easy Dockerized laravel CMS

### Follow First Steps if this is you are a CMS Template Virgin

##Scripts

**Quick Start**
```
    docker-compose up
```

**First Steps**

When you set up the Docker containers for the first time you will need to do the following steps to ensure that everything is setup correctly

* Run ```docker-compose up mysql```

* Wait for the console to finish and say `[Note] mysqld: ready for connections.` 

* Run: ```docker-compose up php```

* Fix permissions for the `plugins`, `storage`, and `themes` folders/volumes so run the following:
```
docker-compose exec php chown -R www-data /var/www/html
```
* Now run the following to run database migrations (create the table structures etc)
```
docker-compose run artisan october:up
```
* Now you will only need to use the quick start when using your new Dockerized CMS repo!

Now you are an OctoberCMS Chad, go forth and spread your alpha seed.

### useful scripts

Composer, Node and Artisan are all containerized on the network allowing you to easily run commands like so:
```
docker-compose run --rm composer update
```
