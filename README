INTRODUCTION
------------

ZMDev is the content management system for the Zeitgeist Developers.

ZMDev is developed on top of the [Ruby on Rails](http://rubyonrails.org/) framework, and uses [RefineryCMS](http://refinerycms.com/) for content management.

DEVELOPMENT
-----------

Setting up a development environment is pretty straightforward. You will need to have Ruby installed, and it is recommended that you use RVM to manage your rubies and gems.

If your using a linux distribution DO NOT use the ruby that comes with ubuntu. If you have a ruby installed it is ok, when using RVM it will override whatever ruby you have installed on your system.

1) Installing RVM

RVM has a simple installer that downloads and sets up your your RVM environment.

After you run the first command to download and install RVM, make sure you read the documentation that outputs as it has information on setting up your shell, and packages to install to allow seamless building of rubies.

2) Installing Ruby

Before installing your first Ruby, if your using a multi-core CPU, you will want to tell the build system to use all of your CPU cores so that the Ruby build goes faster.

    echo "rvm_make_flags="-j 4" >> ~/.rvmrc

This assumes you have 4 cores, adjust to however many cores your system has.

Once you have RVM installed you'll want to build your first ruby. You'll want Ruby 1.9.2.

    rvm install 1.9.2
    rvm use 1.9.2

This may take awhile depending on how fast your machine is.

3) Create a Gemset

Gemsets allow you to install gems into separate containers. This is a feature of RVM that allows you to have multiple Ruby projects on the go without worrying about gem version conflicts.

    rvm gemset create zmdev
    rvm gemset use zmdev

Note that when you change the directory of your shell to the project path for the first time that RVM will ask you if you want to allow the .rvmrc file that is located in the project root. This file contains a command that will set your Ruby and gemset so you can be sure that you are always using the correct gemset.

4) Bundle the project gems

Now you will need to install all of the project dependencies. This is automatically handled with a system called Bundler. So first you will need to install Bundler, then you can bundle the gems for the project.

    gem install bundler
    bundle install

The first command should go rather quickly, the second will take some time as needs to download and install all of the required dependencies.

5) Setup the database

For development you will probably want to stick with a sqlite database. This way you don't have to mess around with any database servers. To do this you'll want to copy the example config, then we'll run the migrations to instantiate the database schema.

    cp config/database.yml.sqlite3 config/database.yml
    rake db:migrate

6) Run the server

Now that everything is setup, you should be able to run the server and browse the site.

    rails s

TESTING
-------

TODO

