# Referer-based access control 

## Lab Overview
This lab demonstrates an access control vulnerability where the application relies on the HTTP Referer header to determine whether a user is authorized to perform administrative actions. Instead of enforcing authorization based on the authenticated user's permissions on the server, the application trusts client-controlled request headers, which can be easily modified by an attacker.

The objective of the lab is to login as the normal user wiener and exploit the flawed access control mechanism to gain administrative privileges. By intercepting and modifying requests with Burp Suite, it is possible to manipulate the Referer header and bypass the application's authorization checks, ultimately promoting the wiener account to an administrator.


First we need to access the web application
<img width="1920" height="928" alt="image" src="https://github.com/user-attachments/assets/3809ae2e-abfb-4f19-a7f7-c3dbb32fb348" />

Then access the admin panel useing the given credintial( administrator:admin)
<img width="1920" height="928" alt="image" src="https://github.com/user-attachments/assets/b5e17398-f4af-43bf-b9ad-d9d5da823bad" />


Now we start burp and intercept the request that upgrades the action of user carlos. then we send the request to burp repeater.
<img width="1920" height="928" alt="image" src="https://github.com/user-attachments/assets/f4e49389-862c-44cd-ad3a-cfae048bf725" />


Now we go back to the lab and logout and login with the normal credintial(wiener:peter) and inspect that page and go to application the Cookies and copy that Cookies.
<img width="1920" height="928" alt="image" src="https://github.com/user-attachments/assets/007d3bfa-8141-4402-b8f7-8fa6929675ab" />


Then go to Burp repeater and replace the Cookie and change the user credintial to wiener.
<img width="960" height="928" alt="image" src="https://github.com/user-attachments/assets/528f848a-ed3b-4577-9e26-6c888f1be03f" />






## Intercepting the Request

![Burp Request](images/request.png)
