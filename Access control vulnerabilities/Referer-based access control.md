# Referer-based access control 

## Lab Overview
This lab demonstrates an access control vulnerability where the application relies on the HTTP Referer header to determine whether a user is authorized to perform administrative actions. Instead of enforcing authorization based on the authenticated user's permissions on the server, the application trusts client-controlled request headers, which can be easily modified by an attacker.

The objective of the lab is to login as the normal user wiener and exploit the flawed access control mechanism to gain administrative privileges. By intercepting and modifying requests with Burp Suite, it is possible to manipulate the Referer header and bypass the application's authorization checks, ultimately promoting the wiener account to an administrator.

First we need to access the web application
<img width="1920" height="928" alt="image" src="https://github.com/user-attachments/assets/3809ae2e-abfb-4f19-a7f7-c3dbb32fb348" />

## Intercepting the Request

![Burp Request](images/request.png)
