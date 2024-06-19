# HTTP response status codes
-HTTP response status codes indicate whether a specific HTTP request has been successfully completed.

Classes of Responses  
## Informational responses 
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

## Successful responses

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

## Redirection messages
***1.300 Multiple Choices***
- The request has more than one possible response and the user user should choose one of them. 

***2.301 Moved Permanently***
- The URL of the requested resource has been changed permanently. The new URL is given in the response.

***3.302 Found***
- The URI of requested resource has been changed temporarily. Further changes in the URI might be made in the future.

***4.303 See Other***  
- To direct the client to get the requested resource at another URI with a GET request.

 