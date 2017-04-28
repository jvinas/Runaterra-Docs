Welcome to runaterra’s initial setup page.

This page is divided in three sections:

-  `Development environment setup`_
-  `QA environment setup`_
-  `Production environment setup`_

Development environment setup
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

    It is recommended to use `Vagrant`_ in order to avoid possible
    errors at the moment of setting up your environment.

Because of Runaterra’s `architecture`_ each service lives in its own
repository and all development related to that specific service should
be done on it. This makes the process of setting a development
environment a tedious task. Luckily, git counts with `submodules`_ to
help us in this kind of situations.

In order to setup an specific service follow the instructions listed in
its repository’s **README** or **Wiki page**. Instead, if you wish to
setup all services at once you have the following options:

-  Use Vagrant (`Download`_)

   #. Execute this in your command line
      ``git clone --recursive https://github.com/intellisys/intranet``
   #. Execute ``vagrant up``
   #. Execute ``vagrant ssh``
   #. Inside of the vagrant’s virtual machine execute go into
      ``/vagrant/`` and execute ``. run-all-services.sh``
   #. All set! Now you can access runaterra’s web dashboard on
      ``http://192.168.100.1``

-  Manual setup

   #. Execute this in your command line
      ``git clone --recursive https://github.com/intellisys/intranet``
   #. Go into every service subdirectory and run its
      \`SERVICENAME-dev-bootstrap.sh’ file.
   #. Go into the project’s root folder and run the file
      ``run-all-services.sh``
   #. All set! Now you can access runaterra’s web dashboard on
      ``http://localhost:8000``

QA environment setup
~~~~~~~~~~~~~~~~~~~~

#. Execute this in your command line
   ``git clone --recursive https://github.com/intellisys/intranet``
#. Go into every service subdirectory and run its
   \`SERVICENAME-QA-bootstrap.sh’ file.
#. Go into the project’s root folder and run the file
   ``run-all-services.sh``

Production environment setup
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Some considerations must be taken when setting a production environment:

-  Not all services run on the same host

.. _Development environment setup: #development-environment-setup
.. _QA environment setup: #QA-environment-setup
.. _Production environment setup: #production-environment-setup
.. _Vagrant: https://www.vagrantup.com/
.. _architecture: Architecture
.. _submodules: https://git-scm.com/book/en/v2/Git-Tools-Submodules
.. _Download: https://www.vagrantup.com/downloads.html
