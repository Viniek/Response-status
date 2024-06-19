# HTTP response status codes
-HTTP response status codes indicate whether a specific HTTP request has been successfully completed.

Classes of Responses  
## 1XX Informational responses 
***1.100 Continue***  
-Indicates that the client should continue the request or ignore the response if the request is already finished.  
**2.101 Switching Protocols***-  
-Indicates the protocol the server is switching to. 
-Sent in response to an Upgrade request header from the client.    
***3.102 Processing (WebDAV)***  
-Indicates that the server has received and is processing the request, but no response is available yet.   
***4.103 Early Hints***  
-lets the user agent start preloading resources while the server prepares a response or preconnect to an origin from which the page will need resources.
-This status code is primarily intended to be used with the Link header.

## 2XX Successful responses

***200 OK***-The request succeeded. 

***1.GET***-The resource has been fetched and transmitted in the message body.  
***2.HEAD***-The representation headers are included in the response without any message body.  
***3.PUT or POST***-The resource describing the result of the action is transmitted in the message body.  
***4.TRACE***-The message body contains the request message as received by the server.  

***201 Created***  
- The request succeeded, and a new resource was created as a result.   
- Sent after POST requests, or some PUT requests.

***202 Accepted***  
- The request has been received but not yet acted upon.  
- It is intended for cases where another process or server handles the request, or for batch processing.

***203 Non-Authoritative Information***
- Means the returned metadata is not exactly the same as is available from the origin server, but is collected from a local or a third-party copy. 
- This is mostly used for mirrors or backups of another resource. 


***204 No Content***
- There is no content to send for this request, but the headers may be useful.

***205 Reset Content***
- Tells the user agent to reset the document which sent this request.  

***206 Partial Content***
- Used when the Range header is sent from the client to request only part of a resource.

***207 Multi-Status (WebDAV)***
- Conveys information about multiple resources, for situations where multiple status codes might be appropriate.

***208 Already Reported (WebDAV)***
- Used to avoid repeatedly enumerating the internal members of multiple bindings to the same collection.
- Used inside a <dav:propstat> response element

***226 IM Used (HTTP Delta encoding)***
- It is a representation of the result of one or more instance-manipulations applied to the current instance.

## 3XX Redirection messages
***1.300 Multiple Choices***
- The request has more than one possible response and the user user should choose one of them. 

***2.301 Moved Permanently***
- The URL of the requested resource has been changed permanently. The new URL is given in the response.

***3.302 Found***
- The URI of requested resource has been changed temporarily. Further changes in the URI might be made in the future.

***4.303 See Other***  
- To direct the client to get the requested resource at another URI with a GET request.

 ***5.304 Not Modified***
 -  Tells the client that the response has not been modified, so the client can continue to use the same cached version of the response.

 ***6.305 Use Proxy Deprecated***
 -  indicate that a requested response must be accessed by a proxy. 

 ***7.306 unused***
 - This response code is no longer used; it is just reserved.  


  **8.307 Temporary Redirect**: The server sends this response to direct the client to get the requested resource at another URI with the same method that was used in the prior request.  
**9.308 Permanent Redirect**: The server sends this response to direct the client to get the requested resource at another URI with the same method that was used in the prior request.


## 4xx Client Errors
- **400 Bad Request**: The server could not understand the request due to invalid syntax.
- **401 Unauthorized**: The client must authenticate itself to get the requested response.
- **402 Payment Required**: This response code is reserved for future use.
- **403 Forbidden**: The client does not have access rights to the content.
- **404 Not Found**: The server can not find the requested resource.
- **405 Method Not Allowed**: The request method is known by the server but is not supported by the target resource.
- **406 Not Acceptable**: The server can not produce a response matching the list of acceptable values defined in the request's proactive content negotiation headers.
- **407 Proxy Authentication Required**: The client must first authenticate itself with the proxy.
- **408 Request Timeout**: The server would like to shut down this unused connection.
- **409 Conflict**: This response is sent when a request conflicts with the current state of the server.
- **410 Gone**: The content has been permanently deleted from the server, with no forwarding address.
- **411 Length Required**: The server refuses to accept the request without a defined Content-Length header.
- **412 Precondition Failed**: The client has indicated preconditions in its headers which the server does not meet.
- **413 Payload Too Large**: Request entity is larger than limits defined by server.
- **414 URI Too Long**: The URI requested by the client is longer than the server is willing to interpret.
- **415 Unsupported Media Type**: The media format of the requested data is not supported by the server.
- **416 Range Not Satisfiable**: The range specified by the Range header field in the request can't be fulfilled.
- **417 Expectation Failed**: This response code means the expectation indicated by the Expect request header field can't be met by the server.
- **418 I'm a teapot**: This code was defined in 1998 as one of the traditional IETF April Fools' jokes.

## 5xx Server Errors
- **500 Internal Server Error**: The server has encountered a situation it does not know how to handle.
- **501 Not Implemented**: The request method is not supported by the server and cannot be handled.
- **502 Bad Gateway**: The server, while working as a gateway to get a response needed to handle the request, got an invalid response.
- **503 Service Unavailable**: The server is not ready to handle the request.
- **504 Gateway Timeout**: The server is acting as a gateway and cannot get a response in time.
- **505 HTTP Version Not Supported**: The HTTP version used in the request is not supported by the server.
- **506 Variant Also Negotiates**: The server has an internal configuration error: the chosen variant resource is configured to engage in transparent content negotiation itself, and is therefore not a proper end point in the negotiation process.
- **507 Insufficient Storage**: The method could not be performed on the resource because the server is unable to store the representation needed to successfully complete the request.
- **508 Loop Detected**: The server detected an infinite loop while processing a request.
- **510 Not Extended**: Further extensions to the request are required for the server to fulfill it.
- **511 Network Authentication Required**: The client needs to authenticate to gain network access.

For detailed information on each status code, refer to the [MDN Web Docs on HTTP Status](https://github.com/viniek)