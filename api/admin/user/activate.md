## [api](../..)/[admin](..)/user/activate

Associates a user with an organization and, optionally, a set of locations.


#### Required inputs

* user id
* organization id
* set of location ids (optional)

The exact format of the request depends on the integration. In some cases, the required inputs may be obtained indirectly through a separate mapping. 

Accepted request formats
* Nexudus `Activate coworker contract` webhook, see [Nexudus](nexudus)


#### HTTP status codes

Either of the following status code will be returned in the response, together with a body in JSON format.

* 200  
  includes details on the activated/created user
  
* 400  
  includes details on the problem with the client request
  
* 500  
  may include details on the server problem in the API


#### Notes

If the identified user does not yet have an account within iotspot, an account will be created.

If a matching user account exists but is associated with a non-demo account that differs from the identified organization, an error will be returned.
