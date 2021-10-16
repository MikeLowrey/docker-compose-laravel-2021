## Install Laravel ##
`git clone https://github.com/MikeLowrey/docker-compose-laravel-2021.git`

`docker-compose build`

`docker-compose up -d`

`docker exec -it laravel-2021-app`

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

`npm rund dev`
  
Check if works with: `php artisan route_list` 

visit your browser and check if localhost:8000 avaible
