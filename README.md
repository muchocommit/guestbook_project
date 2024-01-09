### Symfony Guestbook project build with https://symfony.com/book ### 

###
Create .env file in root directory. This file will be used for docker-compose build command.
e.g.:
POSTGRES_PASSWORD=app
POSTGRES_DB=app
POSTGRES_USER=app
PHP_PORTS=9001:9000
NGINX_PORTS=8082:80
DIRECTORY=guestbook
###
Create .env.local file in project directory. This file overrides .env file from project directory.
e.g.:
POSTGRES_DB=app
POSTGRES_HOST=database
POSTGRES_PORT=5432
POSTGRES_USER=app
POSTGRES_PASSWORD=app
###
Run `docker-compose build` from root directory. 
Build containers with `docker-compose up -d`
###
Make sure all content from project directory is mounted correctly in the php container:
Run `docker-compose exec php bash` and `ls -la`
Run `composer install` 
###
From php container, build CSS and JS files
`symfony run npm run dev`
Watch for changes
`symfony run -d npm run watch`






