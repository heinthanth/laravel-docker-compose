# Laravel Docker

Laravel blog example with `docker-compose`. Laravel blog sample from [Saya Ei Maung](https://github.com/eimg/laravel-book).

## HOW TO

### Application Setup

```shell
$ mkdir db_data
$ cd blog
$ composer install # install composer dependencies
$ cp .env.example .env && vi .env # edit .env according container env
$ npm install # install node dependencies
$ npm run prod # build frontend
$ php artisan key:generate
```

### Container Setup

SSH into container and run migration. **_Don't run if DB persist_**

```shell
$ docker-compose run php sh -c 'cd /var/www/blog && php artisan migrate'

$ docker-compose run php sh -c 'cd /var/www/blog && php artisan db:seed' # add dummy data
```

### DUMMY DATA

"name" => "Bob",
"email" => "bob@gmail.com",

"name" => "Alice",
"email" => "alice@gmail.com",

password = `password`

