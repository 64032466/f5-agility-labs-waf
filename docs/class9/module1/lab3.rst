Lab 3 – Continue to add protections using the OWASP Dashboard
---------------------------------------------------------------


Task – Use the Dashboard and other methods to continue to protect against the OWASP Top 10
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

#. On the Main tab, click **Security > Overview > OWASP Complaince**. Click on the expand arrow next to A1 Injection.  You can see the missing piece is for 100% Injwection protection is applying **Evasion Techniques**.  


#. At this point clicking on the checkmark and applying would move these into a blocking mode.  You are welcome to do this, but let's see how this dashboard interects with your policy.  Perform the following steps to apply in the policy.

    - Go to **Security -> Application Security -> Policy Building -> Learning and Blcoking Settings**
    - Click and expand the section titled **Evasion Technique detected** 
    - Click the checkbox for **Enable** all
    - Press **Save** at the bottom of that screen
    - Press **Apply Policy** button at the top right corner of your screen

    .. image:: /_static/class9/evasiontechniques.png

#. Go back to the Dashboard.  Click **Security > Overview > OWASP Complaince**.  You now see you are 100% protected against A1 Injection.  Now expand **A2 Broken Authentication**.  You can see with some of the default protections, and the previous attack signatures we applied are providing some protections.  

    .. Note:: Unfortunatly protecting against all of the OWASP top 10 is not as easy as applying signatures.  Sometimes you need to apply more app specific protections.  Especially if you have a login page.  If your application does not have a login, this would be a good example of when to select the no symbol (I call it the ghostbuster symbol) button, which will ignore the requirement since it does not apply here.

#. The following steps will decalre our login page for the Juice Shop app, then we will apply more A2 Broken Authenticaton protections against it.

    - Under A2 click the link named **Not Fulfilled** next to Login Enforcement

        .. image:: /_static/class9/loginenforcement.png

    - This brings you to the part of the policy where you declare the info for your login page.  Press **Create** on the top right corner of the page.  
    - In the login URL field enter ``/#/login``
    - In **Authentication Type** select **HTML Form**
    - Type ``email`` in the **Username Parameter Name**
    - Type ``password`` in the **Password Parameter Name**
    - Type ``Invalid`` in the **A string that should NOT appear in the response** field
    - Click Save and Apply the policy.  

#. Now we will apply brute force protection to the login page we created

    - Go to **Security -> Application Security -> Brute Force Attack Prevention**
    - Click **Create** in the top right corner
    - On **Login Page** select the login page we just created
