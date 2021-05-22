# Sprintcube Lamp Project

**Written in 2021-05-2**

* [What is it?](#What-is-it)
* [Analysis](#Analysis)
* [How everything works](#How-everything-works)
* [Highlights](#Highlights)
* [General thoughts](#General-thoughts)

Check the address: `https://github.com/sprintcube/docker-compose-lamp`.

## Whats is it?

Docker receipt providing a webserver, mysql database, redis and a server just to have a phpMyAdmin to manage the database.

The project is ready to consume a local `.env` to make it highly customizable. You can set solely on the .env file the project's name base that will be used by all services, ports for services, mysql database credentials and some paths.

## Analysisz

Following the project tree.

```
.
├── bin
│   ├── mariadb
│   │   └── Dockerfile
│   ├── mysql
│   │   └── Dockerfile
│   ├── mysql8
│   │   └── Dockerfile
│   ├── php54
│   │   └── Dockerfile
│   ├── php56
│   │   └── Dockerfile
│   ├── php71
│   │   └── Dockerfile
│   ├── php72
│   │   └── Dockerfile
│   ├── php73
│   │   └── Dockerfile
│   ├── php74
│   │   └── Dockerfile
│   └── php8
│       └── Dockerfile
├── config
│   ├── php
│   │   └── php.ini
│   └── vhosts
│       └── default.conf
├── data
│   └── mysql
│       ├── auto.cnf
│       ├── binlog.000001
│       ├── binlog.000002
│       ├── binlog.index
│       ├── ca-key.pem
│       ├── ca.pem
│       ├── client-cert.pem
│       ├── client-key.pem
│       ├── docker [error opening dir]
│       ├── #ib_16384_0.dblwr
│       ├── #ib_16384_1.dblwr
│       ├── ib_buffer_pool
│       ├── ibdata1
│       ├── ib_logfile0
│       ├── ib_logfile1
│       ├── ibtmp1
│       ├── #innodb_temp [error opening dir]
│       ├── mysql [error opening dir]
│       ├── mysql.ibd
│       ├── performance_schema [error opening dir]
│       ├── private_key.pem
│       ├── public_key.pem
│       ├── server-cert.pem
│       ├── server-key.pem
│       ├── sys [error opening dir]
│       ├── undo_001
│       └── undo_002
├── docker-compose.yml
├── LICENSE
├── logs
│   ├── apache2
│   │   ├── error.log
│   │   └── other_vhosts_access.log
│   └── mysql
├── README-ja.md
├── README.md
├── sample.env
├── todo.md
└── www
    ├── assets
    │   └── css
    │       ├── bulma.css.map
    │       └── bulma.min.css
    ├── index.php
    ├── phpinfo.php
    ├── test_db_pdo.php
    └── test_db.php
```

The project is *almost* ready to work out of the box. You just needs to copy the `sampe.env` to .env and the sample already have the default variables to work.

Notice the contents in the `bin` folder. There's a folder that carries a `Dockerfile` each. By the environment files, you can choose from wich folder do you want to fetch the docker service setup.

You customizes also the placement for apache log, mounted locally and by default is setted to `logs` folder.

The `data` folder os designed to be mounted locally and holds real data for mysql filesystem.

The `config` folder holds..., configurations! For php and webserver. Some configurations files are locally mounted and poured in the Docker image, so you can make configurations locally and pass to the images configurations.

## Highlights

`Apache` and `Mysql` are the stack available for webserver and database, respectively. Though, you can choose Mysql version through configuration file.

## General toughts

This package was very good for self talght. But as you get this package, you MUST NOT use it without modifications. A careless devops or developer may use this package with minimum modifications, just tweaking out some variables (or even making no changes). But once you parameterize the environment, there's no other reason left to keep everything parameterized. The non used Dockerfile folder for database and php in other versions turns useless (so, dirty code in the project). May you think that you keep things in this mode because if you needs a new environment, just tweaks some variables and execute `docker-compose up -d --build`, that another brand new docker environment will pop up with new vars. This is true, but in this way in throw away one of the biggest advantages of Docker, that keep the project as an environment receipt. If you needs to review an old setup, then you have no way to go back in the old setup (and does not EVEN think to include `.env` in version control, ok?).

Summing up: DO NOT BE LAZY (AN A RECKLESS PREFESSIONAL). Once you choose your environment setup, wipe out everything that is not used on your environment. Even better, do not depends upon `.env` variables. Replaces every variable usage with static parameter.

