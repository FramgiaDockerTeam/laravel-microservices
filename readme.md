# Laravel Microservices

Running Laravel with Microservices Architecture using Docker Containers.

Inspired by [Laradock](https://github.com/LaraDock/laradock)

The following containers will be run by default:
- nginx
- application (for storing project source code)
- php-fpm
- workspace (for working around with the all project)
- mysql
- mysql_test (for running integration test)
- mongodb
- redis
- data (for storing `mysql`, `mongo`, `redis` data)
- data_test (for storing `mysql`, `mongo`, `redis` data while running test)
- logs (for storing some system logs)

## Usage
- Copy file `docker-compose.yml` to your Laravel folder.
- You should change the `project` keyword with your real project name in `docker-compose.yml` file.
- Create `.docker` folder, add a `.gitkeep` file into it, then add `.docker` folder to `.gitignore`. The project's persistant data (mysql, redis, mongodb data ...) will be stored inside this folder.
- You can change other database and container names as well.
- Run `docker-compose up` and enjoy.
- If you do not need any services (such as `mongodb` or `redis`), simply remove it from `docker-compose.yml`

## Links
Our `docker-compose.yml` is powered by the following images:
- [Laravel nginx image](https://github.com/FramgiaDockerTeam/laravel-nginx)
- [Laravel php-fpm image](https://github.com/FramgiaDockerTeam/laravel-php-fpm)
- [Laravel project workspace image](https://github.com/FramgiaDockerTeam/laravel-workspace)
