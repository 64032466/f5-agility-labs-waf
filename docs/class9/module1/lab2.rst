Lab 2 – Discover the OWASP Dashboard
--------------------------------------------------------
Objective
~~~~~~~~~~~~~~~~

- Open up and view the OWASP Compliance Dashboard

- Apply some basic attack signatures using the Dashboard

- Disable the staging of the security policy

Discover and learn to operate the Dashboard
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

#. On the Main tab, click **Security -> Overview -> OWASP Compliance**. This opens the OWASP Dashboard.  Highlight your new policy ``juice_shop_waf``.  You will see that your score is 0/10 for securing against the OWASP top 10.  Though you will see partial % scores for some.

#. Click on the expand arrow next to A1 Injection.  This will display the attack signature types and required protections you need to secure yourself against this risk.

    .. image:: /_static/class9/a1initialreview.png

#. On that same screen in the OWASP Dashboard, hover your pointer over **SQL-Injection** and select the **checkmark**.  Also hover over **Server Side Code Injection** and select the **checkmark**.  These checkmarks apply the protections to the policy.  Notice your potential A1 Injection protection % increased.

    .. Note::  In the dashboard, if you see the checkmark available, it will enforce will enforce

    .. image:: /_static/class9/a1addsignatures.png

#. Press the blue **Review & Update** button below.  On the pop up window press the blue **Save & Apply Policy** button.  

    .. Note:: While all attack signatures in this policy are in staging, we just used the OWASP dashboard to bypass the staging for those 2 catagories.  This would be a typical approach to secure an application immediatly against a certain catagory of injection signatures.  These signatures are now blocked, while staging (learning and alarming) the rest of the signatures.  

#. Now for the sake of running a learning lab in a reasonable amount of time.  We will turn off signature staging.  This will replicate a user waiting out the default 7 days of staging your attack signatures.


    - Go to **Security -> Application Security -> Security Policies** And select your policy by name
    - Under the Enforcement Readiness Period change that to zero and press **Save**
    - Go to **Security -> Application Security -> Policy Building -> Learning and Blocking Settings**
    - Expand **Attack Signatures**
    - Uncheck the box next to **Enable Signature Staging**
    - Press **Save** at the bottom of that screen
    - Press **Apply Policy** button at the top right corner of your screen

    .. image:: /_static/class9/disablestaging.png

#. Go back to your OWASP Dashboard **Security -> Overview -> OWASP Compliance**.  Select your policy ``juice_shop_waf``..  You can now see a lot more OWASP protections now.

    .. image:: /_static/class9/dbwithblocking.png

    .. Note:: When we disabled the staging, we represented a user waiting out the enforcement readiness period.  We basically just time traveled to the future!!  https://youtu.be/8qrriKcwvlY

#. Congratulations!  Your business now has a protected app, and you have visibility into how well you are protected against the OWASP Top 10.  In the following labs we will work to get you even nore risk protection.  