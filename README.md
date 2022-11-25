# Evolutionary Algorithm Web Interface

This is a web interface for floatingbits' [evolutionary algorithm library](https://github.com/floatingbits/evolutionary-algorithm),
a library implementing an evolutionary algorithm in php, which is designed to be highly entensible and flexible. 

## Demo
Visit a running demo [here](http://ea.floatingbitsmedia.de/).

## Intention
On the one hand, keeping track of all the generations of specimens and their development throughout the evolution can be a 
tedious task. You need a place to get an overview over your configurations and previous attempts to optimize your algorithms.

On the other hand, I just wanted to show the world my algorithm in action ;)

## Installation
If you want to make your own installation, it should't be too difficult. A web server running php8.1 and a mysql server should be enough. 
Clone this repo, run 
1. `composer install`,
2. `npm install` and `npm run dev` (or `npm run build` for production), 
3. setup a database 
4. and a .env file,
5. and create your database scheme using `bin/console doctrine:schema:create` and you should be good. 

The .env file should look something like this:
``` 
APP_DEBUG: 1 
APP_ENV: "dev" 
DATABASE_URL: "mysql://DB_USER:DB_PASSWORD@DB_HOST:DB_PORT/DB_NAME"
MESSENGER_TRANSPORT_DSN: "doctrine://default?auto_setup=0"
```
(modify to your needs and environment)

## Developing and solving your own EA problems
This repository is just a simple web app that uses bundles and libraries to make the magic work.
If you want to start your own development, have a look at the following libraries:

1. [floatingbits/evolutionary-algorithm](https://github.com/floatingbits/evolutionary-algorithm)
is the library that makes the actual work. Look at that repository's README file to get to know how to solve your own problems ;)
2. [floatingbits/evolutionary-algorithm-bundle](https://github.com/floatingbits/evolutionary-algorithm-bundle)
is a Symfony bundle that makes the functionality of this interface re-usable. Learn from that repository's README file
how to get your algorithms into this web interface.






