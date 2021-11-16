# What you get #
nginx, node (npm), php8, mysql, mailhog

 
## Install Laravel ##
`git clone https://github.com/MikeLowrey/docker-compose-laravel-2021.git .`

`docker-compose build`

`docker-compose up -d`

If you don't have `composer` and/or `node` installed on your local machine, you can enter the container and install Laravel inside the container. The same applies to later processes when you need node.  You step inside a container with this command:

`docker exec -it laravel-2021-app bash`

`mkdir application`

`cd application`

`composer create-project laravel/laravel .`

`vim .env`

- add the Database Credentials: 

  DATABASE=laravel
  
  USER=laravel
  
  PW=password

`composer install`

`npm install`

`npm run dev`
  
Check if works with: `php artisan route_list` 

visit your browser and check if localhost:8000 avaible

### MailHog ###
Edit you .env file to this:
```
MAIL_MAILER=smtp
MAIL_HOST=localhost
MAIL_PORT=1025
MAIL_USERNAME=null
MAIL_PASSWORD=null
MAIL_ENCRYPTION=null
MAIL_FROM_ADDRESS=hello@world.com
MAIL_FROM_NAME="${APP_NAME}"
```
To check your mails, use your browser. Enter localhost:8025 there.

### How do I change the nginx port from 8000 to any other port?
You can change the nginx port in the docker-compose.yml file. Currently 8000:80 . For example: 9000:80. 

```
nginx
  ...
  ports:
    - 9000:80
  ...
```
