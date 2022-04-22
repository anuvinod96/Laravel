The following steps are used to  run my  code

Server - XAMPP
IDE    - VS Code
API test - Postman

We have 3 api

1.http://localhost/foldername/api/register

   input parameters are
   - name
   - email
   - password
   - password_confirmation
   
   The register route returns a token (because it automatically logs you) but we will regenerate it with the login route to check that works well.

2.http://localhost/foldername/api/login

We log in with the account we just created:

  input parameters are
   - email
   - password
  
 We copy the token returned to us (this token proves that we are connected)

Next Step , we will call user api, In this api you have to set two header followning

        ‘headers’ => [
        ‘Accept’ => ‘application/json’,
        ‘Authorization’ => ‘Bearer ‘.$accessToken,

        ]


3.http://localhost/foldername/api/user
 
 output -
This time, informations about your account are returned.
