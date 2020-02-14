Lab 2 – Discover the OWASP Dashboard
--------------------------------------------------------

Use the Guided Configuration to build a WAF policy.

Task – Open the OWASP Compliance Dashboard
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

#. On the Main tab, click **Security > Overview > OWASP Complaince**. This opens the OWASP Dashboard.  You will see that your score is 0/10 for securing against the OWASP top 10.  Though you will see partial % scores for some.

#. Click on the expand arrow next to A1 Injection.  This will display the attack signature types and required protections you need to secure yourself against this risk.

.. image:: /_static/class9/webappbutton.png
  :width: 600 px

  .. Note:: The guided configuration we used to deploy our policy builds in a staging mode.  So the attack signatures we want are applied to the policy, but will not be set to to blocking for 7 days (default setting)



.. image:: /_static/class9/webappbutton.png
  :width: 600 px

#. Click on the **Web Application Protection** template button.

.. image:: /_static/class9/webapptemplate.png
  :width: 600 px

#. The guided configuration now gives you a configuration example of the tempalte style you are looking to deploy and a list of the objects it will guide you throuhgh the creation of.  Click the  **Next** button.

#. Give your configuration the name ``juice_shop_waf`` this will also name your security policy.

#. Click on **Show Advanced Settings** button in the upper right hand corner of your page.
