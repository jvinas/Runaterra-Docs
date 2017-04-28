Welcome to Runaterra’s project architecture page.

In here you’ll find information about Runaterra’s `service oriented
architecture`_.

Overview
--------

Runaterra is divided into the following services:

-  `Dashboard`_ (**Ekko**)
-  `Human Resources`_ (**Taric**)
-  `Accounting`_ (**Teemo**)
-  `Notifications`_ (**Karma**)
-  `User Authentication`_ (**Nami**)

|Architecture-diagram|

Dashboard (**Ekko**)
~~~~~~~~~~~~~~~~~~~~

Provides and unify web-based user interface for all Runaterra’s
services.

Human Resources (**Taric**)
~~~~~~~~~~~~~~~~~~~~~~~~~~~

Provides all functionalities relating to human resources department.

More specifically:

-  Employee’s management (Registration, deletion, etc…).
-  Vacations management.

Accounting (**Teemo**)
~~~~~~~~~~~~~~~~~~~~~~

Provides all functionalities relating to the accounting department.

More specifically:

-  Payroll processing.
-  Accounting files processing (606, TSS, etc…)

Notifications (**Karma**)
~~~~~~~~~~~~~~~~~~~~~~~~~

Provides a single point of integration for email notification scheduling
processes. This is intended to be used by all services who don’t wish to
handle email notifications to be sent within the company by themselves.

More specifically it provides an interface to:

-  Send an email at the moment when the request is made.
-  Schedule an email to be sent in the future.
-  Schedule an email to be send recurrently.

User Authentication (**Nami**)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Provides client services with a single point of integration for managing
user authentication.

--------------

All communication between services its done through `REST`_ APIs using
`JSON`_ formatted requests and responses.

--------------

To learn how and where Runaterra is running services and codebase are
hosted. Visit our `Hosting and Deployment`_ page. For information on how
to set your environment and get to work visit our `Initial setup`_ page.

.. _service oriented architecture: https://en.wikipedia.org/wiki/Service-oriented_architecture
.. _Dashboard: #dashboard-ekko
.. _Human Resources: #human-resources-taric
.. _Accounting: #accounting-teemo
.. _Notifications: #notifications-karma
.. _User Authentication: #user-authentication
.. _REST: http://www.restapitutorial.com/lessons/whatisrest.html
.. _JSON: http://www.json.org/
.. _Hosting and Deployment: hosting-and-deployment
.. _Initial setup: Initial-Setup

.. |Architecture-diagram| image:: https://i.imgsafe.org/e3cb9c883a.png
