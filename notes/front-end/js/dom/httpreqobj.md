[UP](../index.md)

# XMLHttpRequest
Use XMLHttpRequest (XHR) objects to interact with servers.  
You can retrieve data from a URL without having to do a full page refresh.  

This enables a Web page to update just part of a page without disrupting what the user is doing.  
XMLHttpRequest is used heavily in Ajax programming

## Not Just XML
Despite its name, XMLHttpRequest can be used to retrieve any type of data, not just XML, and it supports protocols other than HTTP (including file and ftp).  

If your communication needs involve receiving event or message data from the server, consider using server-sent events through the EventSource interface. For full-duplex communication, WebSockets may be a better choice.

## Constructor
The constructor initializes an XMLHttpRequest. It must be called before any other method calls.

	XMLHttpRequest()

## Event Handler
### XMLHttpRequest.onreadystatechange
called whenever the readyState attribute changes

### XMLHttpRequest.readyState
Returns an unsigned short, the state of the request.

## Properties

### Response Related
#### XMLHttpRequest.responseText
Returns a DOMString that contains the response to the request as text, or null if the request was unsuccessful or has not yet been sent

#### XMLHttpRequest.responseType
Is an enumerated value that defines the response type.

#### XMLHttpRequest.responseURL
Returns the serialized URL of the response or the empty string if the URL is null.

#### XMLHttpRequest.responseXML
Returns a Document containing the response to the request, or null if the request was unsuccessful, has not yet been sent, or cannot be parsed as XML or HTML.

### Status Related
#### XMLHttpRequest.status
Returns an unsigned short with the status of the response of the request.

#### XMLHttpRequest.statusText
Returns a DOMString containing the response string returned by the HTTP server. Unlike XMLHTTPRequest.status, this includes the entire text of the response message ("200 OK", for example).


## Methods

### Header Related
#### XMLHttpRequest.setRequestHeader()
Sets the value of an HTTP request header. You must call setRequestHeader()after open(), but before send().

#### XMLHttpRequest.getResponseHeader()
Returns the string containing the text of the specified header, or null if either the response has not yet been received or the header doesn't exist in the response.

#### XMLHttpRequest.getAllResponseHeaders()
Returns all the response headers, separated by CRLF, as a string, or null if no response has been received.


#### XMLHttpRequest.open()
Initializes a request. This method is to be used from JavaScript code; to initialize a request from native code, use openRequest() instead.

#### XMLHttpRequest.send()
Sends the request. If the request is asynchronous (which is the default), this method returns as soon as the request is sent.