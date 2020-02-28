Lab 2 – Use the F5 WAF Tester Tool
----------------------------------

Objective
~~~~~~~~~

- Initialize the F5 WAF Tester Tool
- Use the F5 WAF Tester Tool 

Task - Initialize the F5 WAF Tester Tool
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Initialize the tool

::

   f5-waf-tester --init
   [BIG-IP] Host []: 10.1.1.4
   [BIG-IP] Username []: admin
   [BIG-IP] Password []:
   ASM Policy Name []: ipi_demo
   Virtual Server URL []: http://10.1.10.102
   Blocking Regular Expression Pattern [<br>Your support ID is: (?P<id>\d+)<br>]:
   Number OF Threads [25]:
   [Filters] Test IDs to include (Separated by ',') []:
   [Filters] Test Systems to include (Separated by ',') []:
   [Filters] Test Attack Types to include (Separated by ',') []:
   [Filters] Test IDs to exclude (Separated by ',') []:
   [Filters] Test Systems to exclude (Separated by ',') []:
   [Filters] Test Attack Types to exclude (Separated by ',') []:

Edit the config if required. Much easier than re-running the init if you
made a mistake.

::

   vi ~/.local/lib/python2.7/site-packages/f5_waf_tester/config/config.json

After initialization it looks like this

::

   {
     "asm_policy_name": "ipi_demo",
     "big-ip": {
       "username": "admin",
       "host": "10.1.1.4",
       "password": "admin"
     },
     "blocking_regex": "<br>Your support ID is: (?P<id>\\d+)<br>",
     "threads": 25,
     "filters": {
       "exclude": {
         "attack_type": [],
         "id": [],
         "system": []
       },
       "include": {
         "attack_type": [],
         "id": [],
         "system": []
       }
     },
     "virtual_server_url": "http://10.1.10.102"
   }


Task - Use the F5 WAF Tester Tool
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Run the tool

::

    f5-waf-tester -r f5_waf_tester_report_1.json

Many of the tests failed because the signatures were out of date so
ensure the latest signatures have been installed.
https://support.f5.com/csp/article/K8217

Quickly check how many tests passed and failed

::

    grep true f5_waf_tester_report_1.json | wc -l
    grep false f5_waf_tester_report_1.json | wc -l

View the results of the test

::

    less f5_waf_tester_report_1.json


