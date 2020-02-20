Exercise 1.1: Use the Guided Configuration to Build a WAF Policy
------------------------------------------------------------------------
Objective
~~~~~~~~~~~~~~~~

- Create a transparent policy using the guided configuration utiliy

- Apply the security policy to an existing virtual server

- Do an intial review of the OWASP dashboard, and apply some simple signature based protection via the dahboard

- Estimated time for completion: **15** **minutes**.

Please ensure this virtual server is configured before you begin:

- ``Juice_Shop_VS``

Create security policy using the Guided Configuration
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

#. On the Main tab, click **Security > Guided Configuration**. This opens the Guided Configuration screen

#. Click on the **Polices List**

    .. image:: /_static/class9/webappbutton.png

#. Click on the **Web Application Protection** template button.

    .. image:: /_static/class9/webapptemplate.png

#. The guided configuration now gives you a configuration example of the tempalte style you are looking to deploy and a list of the objects it will guide you throuhgh the creation of.  Click the  **Next** button.

#. Give your configuration the name ``juice_shop_waf`` this will also name your security policy.

#. Under **Select Enforcement Mode** select **Blocking**

    .. Note:: Typically you would deploy a new policy in a transparent mode so you can observe the logs before blocking to help avoid false positives.  But come on....this is a lab.  We are going to block stuff!  

#. Click on **Show Advanced Settings** button in the upper right hand corner of your page.

    .. image:: /_static/class9/advanced2.png

#. Under **Server Technologies** add the following to the selected window.  Adding these technologies will assist in building a more precise policy.

    - Express.js
    - JavaScript
    - JQuery
    - Node.js

    .. image:: /_static/class9/servertechnologies.png

    .. Note:: We are adding these technologies since we know what the application is using.  There is also a feature that can be turned on that can allow the policy to learn these technologies.

#. On the next place a check next to **Assign Policy to Virtual Server**, under **Virtual Server** choose **Use Existing**, and move the Juice_Shop_VS to the selected window.  Press **Save & Next**

    .. image:: /_static/class9/addvs.png


#. The next page will summarize the objects and policy configuration.  Review, and take notice that you can also go back and edit.  When done click **Deploy** at the bottom of the screen.  It will take a few moments to complete the policy build.