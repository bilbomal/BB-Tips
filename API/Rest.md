
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
* ### Test arbitrary HTTP methods
  * The HTTP specification lists a few supported methods that web servers should handle. But since an HTTP request is just text, it's it's possible to send an arbitrary method in the request that's not in the specification, like ```FOO```. Make requests to your API using a random method and ensure you get a proper response back from the API. If a ```200 OK``` response is returned from any of these requests, further investigation is warranted.


# Playing with parameters
* ### IDOR Tips
  * ```/api/users/user@email.com``` -> ```/api/users/..%2Fuser@email.com```
  * ```/api/account/123/``` -> ```/api/account/..%2F..%2F123```
  * ```/api/account/123``` - > ```/api/account/123/../123```
