# My Main-App-Hacking-CheckList

## Unauthenticated Testing Phase

1. Domain Selection & Initial Reconnaissance

> Select the target domain (e.g., "example.com")

> Begin all testing without authentication

> Take note of every functionality visible on the page — anything interactive, any forms, buttons, navigation elements, etc. ( i.e login, signup, forgot password, e.t.c )


2. JavaScript File Extraction

> Extract and save all JavaScript files found on the page

> This includes both inline JS ( embedded directly in the HTML ) and external JS files ( linked via "script src=..." )

> Also, do not focus on "example.com" when extracting JS. Go to "example.com/another_endpoint" for more JS files


3. Endpoint Extraction from JavaScript

> Go through each JavaScript file to extract endpoints

> Save all discovered endpoints to endpoints.txt

> Use the "FindSomething" browser extension to assist with this process as well.

> Or you can use https://github.com/4osp3l/0xJS to extract URLs/endpoints in JS files... it's AI-powered and can also scan for security vulnerabilities in JS files.


4. JavaScript File Review for Leaks

> Go through each JS file individually, looking for information leaks or important data

> Look for anything that could help later during testing or potentially lead to a vulnerability when examining the application more deeply


5. Force-Browsing Endpoints ( Unauthenticated Access Testing )

> Take the collected endpoints from endpoints.txt

> Perform force-browsing to see which endpoints are accessible while unauthenticated

> Prioritize and focus on API-looking endpoints as the most interesting targets


6. Start Hacking ( Unauthenticated )

> You should know how to hack or abuse whatever you see while doing unauthenticated testing.


## Authenticated Testing Phase

7. Authenticated Deep Dive

> Log into the application and begin going deep into all areas accessible while authenticated

> Start looking for security vulnerabilities throughout the authenticated portion of the application

8. Context-Based Vulnerability Testing

> Test for specific vulnerabilities based on what is observed in the application

> Don't follow a rigid checklist — let the application's behavior guide the testing approach

Example triggers - 

> If a HTTP GET request contains a ?url= parameter, investigate for SSRF ( Server-Side Request Forgery ) or URL Redirect vulnerabilities

> If user input is reflected on the page, test for XSS

> If there's a file upload feature, test for file upload vulnerabilities

> And so on, depending on what each functionality reveals


9. Start Hacking ( Authenticated )

> > You should know how to hack or abuse whatever you see while doing authenticated testing.


Begin active vulnerability testing and exploitation on the authenticated attack surface
