Usage Guide
===========

*This project it's oriented to all testers wich need an open source web application*.
*Manage all testing data for a Quality Assurance deparment*

Developers
~~~~~~~~~~

Prerequisites
-------------

+ Create virtualenv : ``mkvirtualenv fortunes``
+ Enter your existing virtualenv : ``workon fortunes``
+ Install package : ``python setup.py clean build install test``
+ Regenerate database scripts : ``python www/manage.py makemigrations fortunesadmin``
+ Apply database scripts : ``python www/manage.py migrate``
+ Create new superuser : ``python www/manage.py createsuperuser`` ( *by default is* ``admin`` / ``adminadmin``)

Startup
-------

+ Can start development webserver with : ``python www/manage.py runserver 0.0.0.0:8000``
+ You can handle data from code with : ``python www/manage.py shell``

.. code:: python


    # Introduce some models to start
    from server.models import Server

    s = Server(name="MyTestProject")
    s.save()
    # end
    exit()


ToDo list
~~~~~~~~~

+ **mysql server** trought **docker image** configuration
+ **django** admin database

  + Will need to use bootstraped template ( *https://djangopackages.org/packages/p/django-admin-bootstrapped/* )
  + App : **fortunes-base**
      
      + CRUD for ``Server`` ( *group of connection managers servers* )
  

.. code:: python


    # some python code 