
# Methology
* ### Test authorized endpoints without authorization
  * If your API has an endpoint, say ```/users```, that requires an authenticated request, set up checks that do not use authentication and ensure the service responds with the proper message and status code.
* ### Test with incorrect authentication
 * Try and access authorized endpoints with incorrect tokens or credentials.
* ### Test user privileges
* ### Test unhandled HTTP methods

# Different HTTP Methods
* ### Using ```HEAD``` to bypass authentication
  * Find pages or endpoints in your web service that require authentication or authorization, and make a request using ```HEAD``` instead of ```GET```. If the service is secure, you should get a ```405 Method Not Allowed``` or ```501 Method Unimplemented``` response. If you get a ```200 OK``` response, you've disovered a vulnerability.
