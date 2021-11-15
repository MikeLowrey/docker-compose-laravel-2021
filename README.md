# What you get #
nginx, node (npm), php8, mysql, mailhog

 
## Install Laravel ##
`git clone https://github.com/MikeLowrey/docker-compose-laravel-2021.git` .

`docker-compose build`

`docker-compose up -d`

If you dont have composer or node on you local machine installed then go inside inside a container and install laravel. you step inside with this command:

`docker exec -it laravel-2021-app bash`

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

