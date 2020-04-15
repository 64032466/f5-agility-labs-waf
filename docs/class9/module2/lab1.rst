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

At the shell prompt, type the following commands to restart the Juice Shop application. The first command will list the running docker containers. Note the STATUS. The second command restarts the Juice Shop docker container (only the first 3 unique charcters of the container ID are required) and the third command will list the running container where you should see the STATUS listed as Up for a few seconds which confirms the application was restarted.

In the web shell run the command ``docker ps``. The output will look like the following:

.. code-block:: none

    CONTAINER ID        IMAGE                   COMMAND                  CREATED             STATUS              PORTS                    NAMES
    9aa79dbe7db6        nginx                   "nginx -g 'daemon of…"   5 days ago          Up 3 hours          0.0.0.0:8888->80/tcp     waf111_lab_guide
    2513932bd0cc        bkimminich/juice-shop   "docker-entrypoint.s…"   2 months ago        Up 3 hours          0.0.0.0:3000->3000/tcp   frosty_hellman
    
    
Run the command ``docker restart 251``, but make sure to type the first 3 characters of your Juice Shop container ID. The output will be the first 3 characters of the container ID:

.. code-block:: none

    251


Run the command ``docker ps`` to ensure the container was restarted. Your web shell should look very similar to the following:

.. image:: /_static/class9/docker_ps_restart.png

Go back to the Module 1 / Lab 3 page and run through the hacks. They should fail. Click `here <../module0/lab3.html>`_ to jump to that page.