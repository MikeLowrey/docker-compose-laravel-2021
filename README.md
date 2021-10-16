## Install Laravel ##
`git clone ... `
`docker-compose build`
`docker-compose up -d`
`docker exec -it laravel-api-app`

`mkdir application`
`cd application`
`composer create-project laravel/laravel .`
`vim .env`
- add the Database Credentials: 
  DATABASE=laravel
  USER=root
  PW=password
check if works with `php artisan route_list` 
