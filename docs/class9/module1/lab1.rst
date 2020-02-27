Lab 1 - Use the Secure Guided Configuration to Build a WAF Policy
------------------------------------------------------------------------
Objective
~~~~~~~~~~~~~~~~

- Create a blocking policy using the guided configuration utiliy

- Apply the security policy to an existing virtual server

- Apply a security logging profile to the virtiual server

Create security policy using the Guided Configuration
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

#. On the Main tab, click **Security > Guided Configuration**. This opens the Guided Configuration screen

#. Click on the **Polices List**

    .. image:: /_static/class9/webappbutton.png

#. Click on the **Web Application Protection** template button.

    .. image:: /_static/class9/webapptemplate.png

#. The guided configuration now gives you a configuration example of the template style you are looking to deploy and a list of the objects it will guide you through the creation of.  Click the  **Next** button.

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

#. Press the **Save & Next** Button below.  

    .. image:: /_static/class9/servertechnologies.png

    .. Note:: We are adding these technologies since we know what the application is using.  There is also a feature that can be turned on that can allow the policy to learn these technologies.

#. On the next place a check next to **Assign Policy to Virtual Server**, under **Virtual Server** choose **Use Existing**, and move the Juice_Shop_VS to the selected window.  Press **Save & Next**

    .. image:: /_static/class9/addvs.png

#. The next page will summarize the objects and policy configuration.  Review, and take notice that you can also go back and edit.  When done click **Deploy** at the bottom of the screen.  It will take a few moments to complete the policy build.

#.  After the policy is created, we will want to go into our virtual server settings for ``Juice_Shop_VS`` to make sure we have a log profile enbaled and selected.

    - Go to **Local Traffic -> Virtual Servers**, and select our Juice Shop virtual server.
    - From the top select the tab **Security** and select the **Policies** dropdown.
    - Under **Log Profile** select **Enabled..** and choose **Log illegal requests**.

    .. image:: /_static/class9/enablelogging.png

    .. Note:: Also take note that that this is where the security poilicy we just created is applied to your virtual server.  You can see under **Application Security Policy** it is now enabled with your new policy.
    
#.  You now have an active application security policy that is learning and staging protections against the Juice_Shop virtual server.  