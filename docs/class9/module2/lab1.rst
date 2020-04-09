Lab 1 – Attempt to Hack the Juice Shop
--------------------------------------

Objective
~~~~~~~~~

- Restart the Juice Shop application.
- Attempt the server side XSS hack.
- Attempt the SQL injection hack.

Task - Restart the Juice Shop Application
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The Juice Shop application must be restarted to reset the database. Log onto the Internal LAMP Server by navigating to the Systems column, clicking on the Access dropdown and then clicking on **WEB SHELL**

.. image:: /_static/class9/web_shell_internal_lamp.png

At the shell prompt, type the following commands to restart the Juice Shop application. The first command will list the running docker containers. Note the STATUS. The second command restarts the docker container and the third command will list the running container where you should see the STATUS listed as Up for a few seconds which confirms the application was restarted.

.. code-block:: none

    docker ps
    docker restart `docker ps -lq`
    docker ps

The letters after ``docker ps`` are lowercase L (el) Q (queue) and the character on either end is a backtick.

.. image:: /_static/class9/docker_ps_restart.png

Go back to the Module 1 / Lab 3 page and run through the hacks. They should fail. Click `here <../module0/lab3.html>`_ to jump to that page.