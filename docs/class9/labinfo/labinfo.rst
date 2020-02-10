Lab Environment & Topology 
~~~~~~~~~~~~~~~~~~~~~~~~~~~

..  |lab-diag| image:: /_static/class9/waf111_lab_diagram.png

.. WARNING:: All work is done from the Ubuntu Jump Server which can be access via SSH. No installation or interaction with your local system is required.

All pre-built environments implement the Lab Topology shown below.  Please
review the topology first, then find the section matching the lab environment
you are using for connection instructions.

Environment
-----------

External Jump Server:

* Web Attack Tools: 

 * `nikto <https://github.com/sullo/nikto>`_ - Nikto web server scanner
 * `nmap/nping <https://nmap.org/>`_ - Network mapper

Internal LAMP Server:

* Docker Containers

 * Juice Shop - Extremely Vulnerable Web Application

Lab Topology
------------

The network topology implemented for this lab is very simple. The following
components have been included in your lab environment:

-  1 x Ubuntu Linux 18.04 External Jump Server
-  1 x F5 BIG-IP VE (v15.1) licenced with Best Bundle and Advanced WAF upgrade
-  1 x Ubuntu Linux 18.04 Internal LAMP Server

A graphical representation of the lab:

	|lab-diag|
