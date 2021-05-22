# Laradock

* [What is it?](#What-is-it)
* [Analysis](#Analysis)
* [How everything works](#How-everything-works)
* [Highlights](#Highlights)
* [General thoughts](#General-thoughts)

## What is it?

Is a Docker receipt that seems to bring in containers all (or almost all) third party applications that is compatible to the Laravel (!!!!!!!)

## Analysis


```
.
├── CODE_OF_CONDUCT.md
├── CONTRIBUTING.md
├── DOCUMENTATION
│   ├── config.toml
│   ├── content
│   │   ├── contributing
│   │   │   └── index.md
│   │   ├── documentation
│   │   │   └── index.md
│   │   ├── getting-started
│   │   │   └── index.md
│   │   ├── help
│   │   │   └── index.md
│   │   ├── introduction
│   │   │   └── index.md
│   │   └── related-projects
│   │       └── index.md
│   ├── static
│   │   ├── CNAME
│   │   ├── ads.txt
│   │   └── custom-style.css
│   └── themes
│       └── hugo-material-docs
│           ├── CHANGELOG.md
│           ├── LICENSE.md
│           ├── README.md
│           ├── archetypes
│           │   └── default.md
│           ├── layouts
│           │   ├── 404.html
│           │   ├── _default
│           │   │   ├── __list.html
│           │   │   └── single.html
│           │   ├── index.html
│           │   ├── partials
│           │   │   ├── drawer.html
│           │   │   ├── footer.html
│           │   │   ├── footer_js.html
│           │   │   ├── head.html
│           │   │   ├── header.html
│           │   │   ├── nav.html
│           │   │   └── nav_link.html
│           │   └── shortcodes
│           │       ├── note.html
│           │       └── warning.html
│           ├── static
│           │   ├── fonts
│           │   │   ├── icon.eot
│           │   │   ├── icon.svg
│           │   │   ├── icon.ttf
│           │   │   └── icon.woff
│           │   ├── images
│           │   │   ├── favicon.ico
│           │   │   ├── favicons
│           │   │   │   ├── android-icon-144x144.png
│           │   │   │   ├── android-icon-192x192.png
│           │   │   │   ├── android-icon-36x36.png
│           │   │   │   ├── android-icon-48x48.png
│           │   │   │   ├── android-icon-72x72.png
│           │   │   │   ├── android-icon-96x96.png
│           │   │   │   ├── apple-icon-114x114.png
│           │   │   │   ├── apple-icon-120x120.png
│           │   │   │   ├── apple-icon-144x144.png
│           │   │   │   ├── apple-icon-152x152.png
│           │   │   │   ├── apple-icon-180x180.png
│           │   │   │   ├── apple-icon-57x57.png
│           │   │   │   ├── apple-icon-60x60.png
│           │   │   │   ├── apple-icon-72x72.png
│           │   │   │   ├── apple-icon-76x76.png
│           │   │   │   ├── apple-icon-precomposed.png
│           │   │   │   ├── apple-icon.png
│           │   │   │   ├── browserconfig.xml
│           │   │   │   ├── favicon-16x16.png
│           │   │   │   ├── favicon-32x32.png
│           │   │   │   ├── favicon-96x96.png
│           │   │   │   ├── favicon.ico
│           │   │   │   ├── manifest.json
│           │   │   │   ├── ms-icon-144x144.png
│           │   │   │   ├── ms-icon-150x150.png
│           │   │   │   ├── ms-icon-310x310.png
│           │   │   │   └── ms-icon-70x70.png
│           │   │   ├── laradock-full-logo.jpg
│           │   │   ├── logo.png
│           │   │   └── photos
│           │   │       ├── KiTTY
│           │   │       │   ├── Connection.png
│           │   │       │   ├── ConnectionData.png
│           │   │       │   ├── ConnectionSSH.png
│           │   │       │   ├── ConnectionSSHAuth.png
│           │   │       │   ├── Session.png
│           │   │       │   ├── Terminal.png
│           │   │       │   ├── TerminalKeyboard.png
│           │   │       │   ├── TerminalShell.png
│           │   │       │   ├── Window.png
│           │   │       │   └── WindowAppearance.png
│           │   │       ├── PHPStorm
│           │   │       │   ├── DebugRemoteOn.png
│           │   │       │   ├── RemoteDebuggingSuccess.png
│           │   │       │   ├── RemoteHost.png
│           │   │       │   ├── RemoteTestDebuggingSuccess.png
│           │   │       │   ├── RemoteWebDebuggingSuccess.png
│           │   │       │   ├── Settings
│           │   │       │   │   ├── BuildDeploymentConnection.png
│           │   │       │   │   ├── BuildDeploymentConnectionMappings.png
│           │   │       │   │   ├── BuildDeploymentDebugger.png
│           │   │       │   │   ├── EditRunConfigurationRemoteExampleTestDebug.png
│           │   │       │   │   ├── EditRunConfigurationRemoteWebDebug.png
│           │   │       │   │   ├── LangsPHPDebug.png
│           │   │       │   │   ├── LangsPHPInterpreters.png
│           │   │       │   │   ├── LangsPHPPHPUnit.png
│           │   │       │   │   ├── LangsPHPServers.png
│           │   │       │   │   ├── WindowsFirewallAllowedApps.png
│           │   │       │   │   ├── WindowsHyperVManager.png
│           │   │       │   │   └── hosts.png
│           │   │       │   └── linux
│           │   │       │       └── configuration
│           │   │       │           ├── debugConfiguration.png
│           │   │       │           └── serverConfiguration.png
│           │   │       └── SimpleHostsEditor
│           │   │           └── AddHost_laravel.png
│           │   ├── javascripts
│           │   │   ├── application.js
│           │   │   └── modernizr.js
│           │   └── stylesheets
│           │       ├── application.css
│           │       ├── highlight
│           │       │   └── highlight.css
│           │       ├── palettes.css
│           │       └── temporary.css
│           └── theme.toml
├── LICENSE
├── README-zh.md
├── README.md
├── adminer
│   └── Dockerfile
├── aerospike
│   └── Dockerfile
├── apache2
│   ├── Dockerfile
│   ├── sites
│   │   ├── default.apache.conf
│   │   ├── default.apache.ssl.example
│   │   └── sample.conf.example
│   ├── ssl
│   ├── startup.sh
│   └── vhost.conf
├── aws-eb-cli
│   └── Dockerfile
├── beanstalkd
│   └── Dockerfile
├── beanstalkd-console
│   └── Dockerfile
├── caddy
│   ├── Dockerfile
│   └── caddy
│       ├── Caddyfile
│       └── authlist.conf
├── cassandra
│   └── Dockerfile
├── certbot
│   ├── Dockerfile
│   ├── letsencrypt
│   └── run-certbot.sh
├── clickhouse
│   ├── Dockerfile
│   ├── config.xml
│   ├── docker-entrypoint-initdb.d
│   │   └── init-db.sh
│   ├── docker_related_config.xml
│   ├── entrypoint.sh
│   └── users.xml
├── couchdb
│   └── Dockerfile
├── dejavu
│   └── Dockerfile
├── docker-compose.neo4j.yml
├── docker-compose.sync.yml
├── docker-compose.yml
├── docker-registry
│   └── Dockerfile
├── docker-sync.yml
├── docker-web-ui
│   └── Dockerfile
├── elasticsearch
│   └── Dockerfile
├── gearman
│   └── Dockerfile
├── gitlab
│   └── Dockerfile
├── grafana
│   └── Dockerfile
├── graylog
│   ├── Dockerfile
│   └── config
│       ├── graylog.conf
│       └── log4j2.xml
├── haproxy
│   └── Dockerfile
├── hhvm
│   ├── Dockerfile
│   └── server.ini
├── ide-codiad
│   ├── Dockerfile
│   └── config.php
├── ide-icecoder
│   └── Dockerfile
├── ide-theia
│   └── Dockerfile
├── ide-webide
│   └── Dockerfile
├── ipython
│   ├── Dockerfile.controller
│   ├── Dockerfile.engine
│   ├── ipcontroller-client.json
│   └── ipcontroller-engine.json
├── jenkins
│   ├── CONTRIBUTING.md
│   ├── Dockerfile
│   ├── Jenkinsfile
│   ├── README.md
│   ├── docker-compose.yml
│   ├── init.groovy
│   ├── install-plugins.sh
│   ├── jenkins-support
│   ├── jenkins.sh
│   ├── jenkins_home
│   ├── plugins.sh
│   ├── publish.sh
│   ├── tests
│   │   ├── functions.bats
│   │   ├── install-plugins
│   │   │   ├── Dockerfile
│   │   │   └── update
│   │   │       └── Dockerfile
│   │   ├── install-plugins.bats
│   │   ├── plugins
│   │   │   ├── Dockerfile
│   │   │   └── plugins.txt
│   │   ├── runtime.bats
│   │   ├── test_helpers.bash
│   │   └── upgrade-plugins
│   │       └── Dockerfile
│   └── update-official-library.sh
├── jupyterhub
│   ├── Dockerfile
│   ├── Dockerfile.user
│   ├── jupyterhub_config.py
│   ├── start-notebook.sh
│   ├── start-singleuser.sh
│   ├── start.sh
│   └── userlist
├── kibana
│   └── Dockerfile
├── laravel-echo-server
│   ├── Dockerfile
│   ├── laravel-echo-server.json
│   └── package.json
├── laravel-horizon
│   ├── Dockerfile
│   ├── supervisord.conf
│   └── supervisord.d
│       └── laravel-horizon.conf.example
├── logs
│   ├── apache2
│   └── nginx
├── logstash
│   ├── Dockerfile
│   ├── config
│   │   └── logstash.yml
│   └── pipeline
├── mailcatcher
│   └── Dockerfile
├── maildev
│   └── Dockerfile
├── mailhog
│   └── Dockerfile
├── manticore
│   ├── Dockerfile
│   └── config
│       └── sphinx.conf
├── mariadb
│   ├── Dockerfile
│   ├── docker-entrypoint-initdb.d
│   │   └── createdb.sql.example
│   └── my.cnf
├── memcached
│   └── Dockerfile
├── mercure
│   └── Dockerfile
├── minio
│   └── Dockerfile
├── mongo
│   └── Dockerfile
├── mongo-webui
│   └── Dockerfile
├── mosquitto
│   ├── Dockerfile
│   └── mosquitto.conf
├── mssql
│   └── Dockerfile
├── mysql
│   ├── Dockerfile
│   ├── docker-entrypoint-initdb.d
│   │   └── createdb.sql.example
│   └── my.cnf
├── neo4j
│   ├── Dockerfile
│   ├── docker-entrypoint.sh
│   └── local-package
│       └── neo4jlabs-plugins.json
├── nginx
│   ├── Dockerfile
│   ├── logrotate
│   │   └── nginx
│   ├── nginx.conf
│   ├── sites
│   │   ├── app.conf.example
│   │   ├── confluence.conf.example
│   │   ├── default.conf
│   │   ├── laravel.conf.example
│   │   ├── laravel_varnish.conf.example
│   │   ├── node.conf.example
│   │   └── symfony.conf.example
│   ├── ssl
│   └── startup.sh
├── percona
│   ├── Dockerfile
│   ├── docker-entrypoint-initdb.d
│   │   └── createdb.sql.example
│   └── my.cnf
├── php-fpm
│   ├── Dockerfile
│   ├── aerospike.ini
│   ├── laravel.ini
│   ├── mysql.ini
│   ├── opcache.ini
│   ├── phalcon.ini
│   ├── php5.6.ini
│   ├── php7.0.ini
│   ├── php7.1.ini
│   ├── php7.2.ini
│   ├── php7.3.ini
│   ├── php7.4.ini
│   ├── php8.0.ini
│   ├── xdebug
│   ├── xdebug.ini
│   ├── xhprof.ini
│   └── xlaravel.pool.conf
├── php-worker
│   ├── Dockerfile
│   ├── supervisord.conf
│   └── supervisord.d
│       ├── laravel-scheduler.conf.example
│       └── laravel-worker.conf.example
├── phpmyadmin
│   └── Dockerfile
├── portainer
│   └── Dockerfile
├── postgres
│   ├── Dockerfile
│   └── docker-entrypoint-initdb.d
│       ├── createdb.sh.example
│       ├── init_confluence_db.sh
│       ├── init_gitlab_db.sh
│       ├── init_jupyterhub_db.sh
│       └── init_sonarqube_db.sh
├── postgres-postgis
│   └── Dockerfile
├── rabbitmq
│   └── Dockerfile
├── react
│   ├── Dockerfile
│   ├── README.md
│   ├── package-lock.json
│   ├── package.json
│   ├── public
│   │   ├── favicon.ico
│   │   ├── index.html
│   │   ├── logo192.png
│   │   ├── logo512.png
│   │   ├── manifest.json
│   │   └── robots.txt
│   └── src
│       ├── Theme.js
│       ├── assets
│       │   ├── Local
│       │   │   ├── ar.js
│       │   │   ├── en.js
│       │   │   └── messages.js
│       │   ├── fonts
│       │   │   └── Roboto
│       │   │       ├── Roboto-Black.ttf
│       │   │       ├── Roboto-BlackItalic.ttf
│       │   │       ├── Roboto-Bold.ttf
│       │   │       ├── Roboto-BoldItalic.ttf
│       │   │       ├── Roboto-Italic.ttf
│       │   │       ├── Roboto-Light.ttf
│       │   │       ├── Roboto-LightItalic.ttf
│       │   │       ├── Roboto-Medium.ttf
│       │   │       ├── Roboto-MediumItalic.ttf
│       │   │       ├── Roboto-Regular.ttf
│       │   │       ├── Roboto-Thin.ttf
│       │   │       └── Roboto-ThinItalic.ttf
│       │   └── images
│       │       └── reactjs.jpg
│       ├── components
│       │   ├── Controls
│       │   │   ├── Button
│       │   │   │   └── Button.js
│       │   │   └── InputField
│       │   │       └── InputField.js
│       │   ├── Loader
│       │   │   ├── Loader.js
│       │   │   └── Loader.scss
│       │   ├── Navbar
│       │   │   └── Navbar.js
│       │   ├── NotFound
│       │   │   └── NotFound.js
│       │   └── Snackbar
│       │       └── Snackbar.js
│       ├── containers
│       │   ├── App.js
│       │   ├── App.scss
│       │   ├── Home
│       │   │   └── Home.js
│       │   └── Login
│       │       └── Login.js
│       ├── index.js
│       ├── network
│       │   ├── apis
│       │   │   └── index.js
│       │   └── interceptors
│       │       └── index.js
│       ├── routes
│       │   ├── History.js
│       │   └── Routes.js
│       ├── scss
│       │   ├── _general.scss
│       │   ├── _rtl.scss
│       │   ├── _variables.scss
│       │   └── base.scss
│       ├── store
│       │   ├── Feature1
│       │   │   ├── FeatureAction.js
│       │   │   ├── FeatureApis.js
│       │   │   ├── FeatureReducer.js
│       │   │   ├── FeatureSagas.js
│       │   │   └── FeatureTypes.js
│       │   ├── Lang
│       │   │   ├── LangAction.js
│       │   │   ├── LangReducer.js
│       │   │   └── LangTypes.js
│       │   ├── Loader
│       │   │   ├── LoaderAction.js
│       │   │   ├── LoaderReducer.js
│       │   │   └── LoaderTypes.js
│       │   ├── Snackbar
│       │   │   ├── SnackbarAction.js
│       │   │   ├── SnackbarReducer.js
│       │   │   └── SnackbarTypes.js
│       │   ├── index.js
│       │   ├── reducers
│       │   │   └── index.js
│       │   └── sagas
│       │       └── index.js
│       └── utils
│           ├── Auth.js
│           ├── Constants.js
│           ├── LazyLoaded.js
│           ├── PrivateRoute.js
│           └── Shared.js
├── redis
│   ├── Dockerfile
│   └── redis.conf
├── redis-cluster
│   └── Dockerfile
├── redis-webui
│   └── Dockerfile
├── rethinkdb
│   └── Dockerfile
├── selenium
│   └── Dockerfile
├── solr
│   └── Dockerfile
├── sonarqube
│   └── Dockerfile
├── sqs
│   └── Dockerfile
├── swagger-editor
│   └── Dockerfile
├── swagger-ui
│   └── Dockerfile
├── sync.sh
├── thumbor
│   └── Dockerfile
├── traefik
│   ├── Dockerfile
│   └── data
├── travis-build.sh
├── varnish
│   ├── Dockerfile
│   ├── default.vcl
│   ├── default_wordpress.vcl
│   └── start.sh
├── weaver
│   └── conf
│       └── sample.env
├── workspace
│   ├── Dockerfile
│   ├── aerospike.ini
│   ├── aliases.sh
│   ├── auth.json
│   ├── composer.json
│   ├── crontab
│   │   └── laradock
│   ├── git-prompt.sh
│   ├── insecure_id_rsa
│   ├── insecure_id_rsa.ppk
│   ├── insecure_id_rsa.pub
│   ├── mc
│   │   └── config.json
│   ├── sources.sh
│   └── xdebug.ini
└── zookeeper
    └── Dockerfile
```

## How everything works

## Highlights

## General thoughts

