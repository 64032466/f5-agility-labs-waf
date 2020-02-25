Lab 4 – Advanced configuration protections using the OWASP Dashboard
---------------------------------------------------------------------
Objective
~~~~~~~~~~~

- Apply some final configurations to protect against the OWASP Top 10

- Do a final review of the OWASP Compliance Dashboard

Build additional configuration protections against the OWASP Top 10
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

#. On the OWASP Dashboard, path **Security -> Overview -> OWASP Compliance**. Click on the expand arrow next to **A2 Broken Authentication**. We still have no Login Enforcement resources.  What we want to applty ere is known resources in the application that can only be reached by a user who has already gone through a successful login process.  

    - Under A2 click the link named **Not Fulfilled** next to Login Enforcement.  

        .. image:: /_static/class9/loginenforcementtab.png

    - In the Authenticated URLs field enter ``/#/privacy-security/`` and press ther add button and ``/#/wallet`` and press the add button.  
    - Press the **Save** button below.  Then press the **Apply Policy** Button in the top right corner. 
    - Now press the link in the note message below titled **Learning and Blocking Settings Screen**

        .. image:: /_static/class9/enforcementURLs.png

    - On this screen check off the **Alarm** and **Block**
    - Press **Save** below and **Apply Policy** in the top right.
    - These protections are now applied to A2, and also to A5.


#. Back on the OWASP Dashboard, path **Security -> Overview -> OWASP Compliance**. Click on the expand arrow next to **A4  XML External Entities**.  Previous signature protections already are helping to mitigate these XML exploits.  Here are the steps to apply the DTDs 

    - Navigate to **Security -> Application Security -> Content Profiles -> XML Profiles**.
    - Click the name of the default XML profile. (Typically we create a new profile, and we do not modify a default profile, but for simplicity and since we only have one application we will do so here)
    - Under Profile Properties, click the XML Firewall Configuration tab.
    - On the Defense Configuration list, click Advanced.
    - Clear the Allow DTDs check box.
    - Click the **Update** button.
    - Go to **Security -> Application Security -> Policy Building -> Learning and Blocking Settings Settings**.
    - Expamnd the **Content Profiles** section.  Place a check in the  **Alarm** and the **Block** settings next to **XML data does not comply with format settings**.  
    - Press **Save** at the bottom of the screen and **Apply Policy** in the top right corner.  

#. On the OWASP Dashboard, path **Security -> Overview -> OWASP Compliance**. Click on the expand arrow next to **A7 Cross-Site Scripting (XSS)**.  If you remember, A1 Injection included the protections against a lot of signatures and one of those catagories was XSS.  We are not using any HttpOnly cookies in this app so the last requirement to earn us 100% needed is