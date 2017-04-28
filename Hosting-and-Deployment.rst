Welcome to our hosting and deployment page, here you’ll learn most of
what you need to understand how and where Runaterra is deployed. Also:

-  How services are distributed between hosts.
-  How they should behave in relation to external services that are
   managed by other teams.
-  How is the project’s codebase organized.

If you have not read about Runaterra’s architecture we recommend you to
do it `here`_.

Services groups
---------------

Services running in runnaterra can be divided into 3 logical groups:

-  **Application Front-end**

   -  `Dashboard`_ (Ekko)

-  **Application Back-end**

   -  `Human Resources`_ (Taric)
   -  `Accounting`_ (Teemo)
   -  `Notifications`_ (Karma)

|Services-groups|

Services host distribution
~~~~~~~~~~~~~~~~~~~~~~~~~~

|Services-groups|

Codebase and deployment
~~~~~~~~~~~~~~~~~~~~~~~

Every service is deployed independently of all others and counts with
its own repository in which it **must** contain the following files :

-  ``README.md``: contains all documentation specific to this service.
   (This can be replaced with a wiki page if needed)
-  ``SERVICENAME-prod-bootstrap.sh``: shell script which sets up all
   necessary configurations for the production environment.
-  ``SERVICENAME-dev-bootstrap.sh``: shell script which sets up all
   necessary configurations for development.

    This repository only serves as a reference central point for
    Runaterra’s entire codebase.

    Because is recommended for the development environment setup to be
    done using `Vagrant`_ (see, `initial Setup`_), bootstrap.sh files
    must take care of the complete installation of the environment.

Continous integration
~~~~~~~~~~~~~~~~~~~~~

To improve the deployment process, continuous integration with
`Jenkins`_ is setup for each service within a job named
\`runaterra\_SERVICENAME(See Runaterra’s `All Links`_ Page).

--------------

To start setting your environment and get into work visit out `initial
Setup`_ page.

.. _here: Architecture
.. _Dashboard: Architecture#dashboard-ekko
.. _Human Resources: Architecture#human-resources-taric
.. _Accounting: Architecture#accounting-teemo
.. _Notifications: Architecture#notifications-karma
.. _Vagrant: https://www.vagrantup.com/
.. _initial Setup: Initial-Setup
.. _Jenkins: https://jenkins.io/
.. _All Links: 

.. |Services-groups| image:: https://i.imgsafe.org/e3ae83a0b7.png
.. |Services-groups| image:: https://i.imgsafe.org/e396d78a54.png
