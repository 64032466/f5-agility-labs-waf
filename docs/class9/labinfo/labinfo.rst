Lab Environment & Topology 
~~~~~~~~~~~~~~~~~~~~~~~~~~~

..  |lab-diag| image:: /_static/class9/waf111_lab_diagram.png

Environment
-----------

External Jump Server:

* Web Attack Tools: 

 * `nikto <https://github.com/sullo/nikto>`_ - Nikto web server scanner
 * `nmap/nping <https://nmap.org/>`_ - Network mapper

Internal LAMP Server:

* Docker Containers

 * Juice Shop - Extremely Vulnerable Web Application

F5 BIG-IP version 15.1

* Licensed Modules

 * Best Bundle (LTM, AFM, APM, ASM)
 * Advanced WAF add-on
 * IP Intelligence

Lab Topology
------------

The network topology implemented for this lab is very simple. The following
components have been included in your lab environment:

-  1 x F5 BIG-IP VE (v15.1) licenced with Best Bundle and Advanced WAF upgrade
-  1 x Ubuntu Linux 18.04 External Jump Server
-  1 x Ubuntu Linux 18.04 Internal LAMP Server

A network diagram of the lab:

	|lab-diag|
