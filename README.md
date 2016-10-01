#Home gun API
Coding an API (training project) serving `home-gun` Android app.

## Technologies
* Programming language: ruby 2.3.0
* Database: postgres with
* Framework for HTTP requests: Sinatra

## Installation

#### Lauching containers
In separate terminal:
```
docker-machine create -d virtualbox default
eval $(docker-machine env default)
docker-compose up
```

#### Killing containers
```
docker ps -q | xargs docker kill
docker ps -q | xargs docker rm
```

#### Database operations
Running migration schema:
```
PGPASSWORD=pass bundle exec sequel -m database/migrations/ postgres://homegun@`docker-machine ip`:5431/homegun -t
```

Running trough the database:
```
docker exec -it `docker ps -q` bash
psql -Upostgres
\l
\c homegun;
\d
drop table users;
```

## Run

#### Locally
WIP

#### Distant access
WIP

#### Tests suite
WIP

## Troubleshooting
WIP

