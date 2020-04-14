<p align="center">
<img alt="FastFeet" src="./logo.png" />
</p>

<h1 align="center">FastFeet Application from Rocketseat GoStack</h1>

<blockquote align="center">
:zap: ReactJS application to obtain the GoStack bootcamp certify
</blockquote>

<p align="center">
  <img alt="GitHub language count" src="https://img.shields.io/github/languages/count/LeuAlmeida/fastfeet-web?color=%2304D361">

  <a href="https://leunardo.dev">
    <img alt="Made by Léu Almeida" src="https://img.shields.io/badge/made%20by-Léu%20Almeida-%2304D361">
  </a>
</p>

<p align="center">
<img alt="FastFeet presentation" src="./github/animation.gif" />
</p>

## Introduction

[Fastfeet](https://github.com/LeuAlmeida/fastfeet-web) is a fictitious logistic company and this repository belong to the business logic and is the basis of a general structure and all of this be a part of the [Rocketseat bootcamp](https://github.com/rocketseat) certify.

## :electric_plug: Prerequisites

- [Node.js LTS (>= 12.x)](https://nodejs.org/)
- [Yarn (>= 1.21)](https://yarnpkg.com/) or [NPM (>= 6.9)](https://www.npmjs.com/)
- [Docker CE (>= 19.03.3)](https://docs.docker.com/install/)

# :closed_lock_with_key: API Instructions

First get all the requirements installed on your system.
You will need to run the API using some Docker Images like [PostgreSQL](https://hub.docker.com/_/postgres) and [Redis](https://hub.docker.com/_/redis/).
Certified that do you have wall prerequisites, start the docker images dependencies:

```shell
# Change the <password> below and on .env file to run PostgreSQL
$ sudo docker run --name fastfeet -e POSTGRES_PASSWORD=<password> -p 5432:5432 -d postgres:11

# Execute the Redis docker
$ sudo docker run --name redisfastfeet -p 6379:6379 -d -t redis:alpine
```

### Getting started the API Restful backend

Make a clone from the repo and install the dependencies

```shell

# After clone this repo, enter in the API folder
$ cd api

# Install all dependencies using Yarn
$ yarn
```

Certify yourself that all environments are correct

```shell
# Copy the .env folder
$ cp .env.example .env

# Insert your environments into .env file
$ nano .env

```

Prepare the PostgreSQL database

```shell
# Migrate the database
$ yarn sequelize db:migrate

# Run the seeds
$ yarn sequelize db:seed:all
```

Start the project

```shell
# Run the development server
$ yarn dev

# Case the output appears like this, is all ok
yarn run v1.19.1
$ nodemon src/server.js
[nodemon] 2.0.2
[nodemon] to restart at any time, enter `rs`
[nodemon] watching dir(s): *.*
[nodemon] watching extensions: js,mjs,json
[nodemon] starting `node -r sucrase/register src/server.js`

# The backend will run on port 3333
# https://localhost:3333
```

In a separated terminal, run the queue

```shell
# Run the queue to enable mails and dependencies that uses bee-queue
$ yarn queue

# Case the output appears like this, is all ok
yarn run v1.19.1
$ nodemon src/queue.js
[nodemon] 2.0.2
[nodemon] to restart at any time, enter `rs`
[nodemon] watching dir(s): *.*
[nodemon] watching extensions: js,mjs,json
[nodemon] starting `node -r sucrase/register src/queue.js`
```

# :closed_lock_with_key: Web Application instructions

Make a clone from the repo and install the dependencies. (Certify yourself that the api is running)

```shell
# After clone this repo, enter in the Web folder
$ cd web

# Install all dependencies using Yarn
$ yarn

# Run the project
$ yarn start
```

# :closed_lock_with_key: Mobile App instructions (Has not been tested on iOS)

Make a clone from the repo and install the dependencies

```shell
# After clone this repo, enter in the DevRadar folder
$ cd fastfeet-app

# Install all dependencies using Yarn
$ yarn

# Run the react native metro bundle
$ react-native start

# Run the project
$ react-native run-android
```

## :copyright: License

MIT License.

See [LICENSE](LICENSE) for details.

<hr/>

<h3 align="center">
<a href="http://linkedin.com/in/leonardoalmeida99">Connect me in LinkedIn</a> | <a href="http://behance.net/almeida99">See my Behance</a> | <a href="https://leunardo.dev">Click here to go to my CV</a>
</h3>
