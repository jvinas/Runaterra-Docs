Welcome to our hosting and deployment page, here you'll learn most of what you need to understand how and where Runaterra is deployed. Also: 
 - How services are distributed between hosts.
 - How they should behave in relation to external services that are managed by other teams. 
 - How is the project's codebase organized. 

If you have not read about Runaterra's architecture we recommend you to do it [here](Architecture).


## Services groups

Services running in runnaterra can be divided into 3 logical groups:
 - **Application Front-end**
     - [Dashboard](Architecture#dashboard-ekko) (Ekko)
 - **Application Back-end** 
     - [Human Resources](Architecture#human-resources-taric) (Taric)
     - [Accounting](Architecture#accounting-teemo) (Teemo)
     - [Notifications](Architecture#notifications-karma) (Karma)

![Services-groups](https://i.imgsafe.org/e3ae83a0b7.png)

### Services host distribution

![Services-groups](https://i.imgsafe.org/e396d78a54.png)

### Codebase and deployment

Every service is deployed independently of all others and counts with its own repository in which it **must** contain the following files :

 - `README.md`: contains all documentation specific to this service. (This can be replaced with a wiki page if needed)
 - `SERVICENAME-prod-bootstrap.sh`: shell script which sets up all necessary configurations for the production environment.
 - `SERVICENAME-dev-bootstrap.sh`: shell script which sets up all necessary configurations for development.

> This repository only serves as a reference central point for Runaterra's entire codebase.

> Because is recommended for the development environment setup to be done using [Vagrant](https://www.vagrantup.com/) (see, [initial Setup](Initial-Setup)), bootstrap.sh files must take care of the complete installation of the environment.

### Continous integration

To improve the deployment process, continuous integration with [Jenkins](https://jenkins.io/) is setup for each service within a job named `runaterra_SERVICENAME(See Runaterra's [All Links]() Page). 

---
To start setting your environment and get into work visit out [initial Setup](Initial-Setup) page.
