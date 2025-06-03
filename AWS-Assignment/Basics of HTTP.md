

### What is HTTP?
The Hypertext Transfer Protocol (HTTP) is designed to enable communications between clients and servers.
HTTP works as a request-response protocol between a client and server.

HTTP Methods:
---
GET
POST
PUT
HEAD
DELETE
PATCH
OPTIONS
CONNECT
TRACE

The two most common HTTP methods are: GET and POST.

### GET is used to request data from a specified resource
POST is used to send data to a server to create/update a resource




### The PUT Method: 
PUT is used to send data to a server to create/update a resource.

### The HEAD Method:
HEAD is almost identical to GET, but without the response body.

In other words, if GET /users returns a list of users, then HEAD /users will make the same request but will not return the list of users.

A HEAD request is useful for checking what a GET request will return before actually making a GET request - a HEAD request can read the Content-Length header to check the size of the file, without actually downloading the file.

### The DELETE Method :

The DELETE method deletes the specified resource.

### The PATCH Method
The PATCH method is used to apply partial modifications to a resource.

### The OPTIONS Method
The OPTIONS method describes the communication options for the target resource.

### The CONNECT Method
The CONNECT method is used to start a two-way communications (a tunnel) with the requested resource.

### The TRACE Method
The TRACE method is used to perform a message loop-back test that tests the path for the target resource (useful for debugging purposes).


**CODE Status**
-------
100 | Continue
101 | Switching Protocols
200 | OK
201 | Created
202 | Accepted
203 |Non-Authoritative Information (since HTTP
204 | no content
205 |Reset Content
206 | Partial Content
304 | not modified
400 | Bad request
401 |Unauthorized
402 | payment required
403 |Forbidden
404 | Not Found : The requested resource was not found on the server.
500 | Internal Server Error : The server encountered an error while processing the request.
301 | Moved Permanently: The requested resource has been permanently moved to a new URL.


