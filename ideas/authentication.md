Status: done

implement an cookie storage on the login service after authenticate the users. 
Generate a token which includes logged user detals and make it secure.

Protect all the service and endpoints with an @authenticate
if service is running locally allow all the conection and don validate the cookie nither the token.
if service is running on other type of service, validate the token and return data only if user is available.

