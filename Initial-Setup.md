Welcome to runaterra's initial setup page. 

This page is divided in three sections:

 - [Development environment setup](#development-environment-setup)
 - [QA environment setup](#QA-environment-setup)
 - [Production environment setup](#production-environment-setup)

### Development environment setup

> It is recommended to use [Vagrant](https://www.vagrantup.com/) in order to avoid possible errors at the moment of setting up your environment.

Because of Runaterra's [architecture](Architecture) each service lives in its own repository and all development related to that specific service should be done on it. This makes the process of setting a development environment a tedious task. Luckily, git counts with [submodules](https://git-scm.com/book/en/v2/Git-Tools-Submodules) to help us in this kind of situations.

In order to setup an specific service follow the instructions listed in its repository's **README** or **Wiki page**. Instead, if you wish to setup all services at once you have the following options:

 - Use Vagrant ([Download](https://www.vagrantup.com/downloads.html))
    1. Execute this in your command line `git clone --recursive https://github.com/intellisys/intranet`
    2. Execute `vagrant up`
    3. Execute `vagrant ssh`
    4. Inside of the vagrant's virtual machine execute go into `/vagrant/` and execute `. run-all-services.sh`
    5. All set! Now you can access runaterra's web dashboard on `http://192.168.100.1`

 - Manual setup
    1. Execute this in your command line `git clone --recursive https://github.com/intellisys/intranet`
    2. Go into every service subdirectory and run its `SERVICENAME-dev-bootstrap.sh' file.
    3. Go into the project's root folder and run the file `run-all-services.sh`
    5. All set! Now you can access runaterra's web dashboard on `http://localhost:8000`


### QA environment setup
 1. Execute this in your command line `git clone --recursive https://github.com/intellisys/intranet`
 2. Go into every service subdirectory and run its `SERVICENAME-QA-bootstrap.sh' file.
 3. Go into the project's root folder and run the file `run-all-services.sh`

### Production environment setup

Some considerations must be taken when setting a production environment:

 - Not all services run on the same host
