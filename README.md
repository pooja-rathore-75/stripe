# README

This README would normally document whatever steps are necessary to get the
application up and running.

Things you need to cover:

* Ruby Version: `3.0.0`

* Rails Version: `6.0.6.1`

* Run Bundle
  `bundle install`

* Need to configure your STRIPE_PUBLISHABLE_KEY and STRIPE_SECRET_KEY in `.evn` file.

* Configure the postgres username and password in `database.yml` and `docker-compose.yml` file.

* Run the below command to set the configuration of docker:
  `docker-compose build`
  `docker-compose up`

* If server is not running, then need to run the following command:

  `docker-compose up -d`

  Note: docker-compose up -d command starts the Docker containers defined in the docker-compose.yml file in detached mode. This means the containers will run in the background and won't display their logs in the terminal.

  `docker-compose run web bash`

  Note: docker-compose run web bash command runs the web service defined in the docker-compose.yml file, and starts a Bash shell in it. This allows you to access the command line interface of the running Docker container, which can be useful for various purposes like running database migrations, installing packages, debugging, etc.

  Then, we need to run in terminal - 
  `rails db:create` and `rails db:migrate`

  After this need to exit from the terminal run: `exit`

  Note: Overall, these commands are commonly used in a Dockerized Rails application to start the containers and access the shell of the running web service.

  And in last need to run the server:
    `docker-compose build`
    `docker-compose up`

* If you are facing `/app/public/packs/manifest.json.` related issue, Need to run assets precompile.
    `rails assets:precompile`
