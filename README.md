# Genesys-Cloud-Authenticated-messaging-using-Auth0

This guide provides a comprehensive, step-by-step example of integrating Genesys Cloud web messaging with Auth0 to enable authenticated web messaging. The integration involves setting up user authentication via Auth0, exchanging tokens, and enabling a secure Genesys chat widget on your web application.

**Step1:** Login - The user is redirected to the Auth0 login page using the below URL and credentials

https://dev-rtsdfwtg62km32yv.us.auth0.com/authorize?client_id=jsL6NQnBWPAYMTymjAe38x8oRBQj9ijt&redirect_uri=http://localhost:3000/callback&scope=openid profile email phone address&response_type=code&state=369430729d5f8eecc408c11306a930909dfe55c9

**Step 2:** The user is authenticated and redirected to the "redirect_uri" mentioned in the login request along with the code (authCode)

![image](https://github.com/user-attachments/assets/e16c27fa-0957-4e74-88f1-a143ddcc93c6)

**Step 3:** On page load, web page grabs the code(authCode) from the URL and passes it on to the Genesys Auth provider plugin 

![image](https://github.com/user-attachments/assets/a653df09-f77c-4c0d-8513-b1cc0b39316e)

Step 4: Genesys sends an authorization request using its Javascript plugin and exchanges its own JWT. After successful, authentication, the chat widget is displayed

![image](https://github.com/user-attachments/assets/357ae8ca-df84-43b2-824c-e7e3f5f5b86d)

Sample Code - Refer to AuthenticatedWebMessaging.html
