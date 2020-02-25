Lab 4 – Advanced configuration protections using the OWASP Dashboard
---------------------------------------------------------------------


Task – We will continue applying negative securty protections for the OWASP Top 10
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~



#. Back on the OWASP Dashboard, path **Security -> Overview -> OWASP Complaince**. Click on the expand arrow next to **A4  XML External Entities**.  Previous signature protections already are helping to mitigate these XML exploits.  Here are the steps to apply the DTDs 

    - Navigate to **Security > Application Security > Content Profiles > XML Profiles**.
    - Click the name of the default XML profile. (Typically we create a new profile, and we do not modify a default profile, but for simplicity and since we only have one application we will do so here)
    - Under Profile Properties, click the XML Firewall Configuration tab.
    - On the Defense Configuration list, click Advanced.
    - Clear the Allow DTDs check box.
    - Click Update.
    - Go to **Security -> Application Security -> URLs -> Allowed URLs**
    - Place a check in the 