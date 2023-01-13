<a href="/JS/AJAX/XMLHttp.md">&lt; Previous</a>
&nbsp;&nbsp;&nbsp;
<a href="/JS/AJAX/Request.md">Next &gt;</a>
<hr>
<h1>1XX</h1>
The <b>1XX (Informational)</b> class of status code indicates an interim response for communicating connection status or request progress prior to completing the requested action and sending a final response. 1xx responses are terminated by the first empty line after the status-line (the empty line signaling the end of the header section). Since HTTP/1.0 did not define any 1XX status codes, a server MUST NOT send a 1xx response to an HTTP/1.0 client.
<br><br>
A client MUST be able to parse one or more 1XX responses received prior to a final response, even if the client does not expect one. A user agent MAY ignore unexpected 1XX responses.
<br><br>
A proxy MUST forward 1xx responses unless the proxy itself requested the generation of the 1XX response. For example, if a proxy adds an "Expect: 100-continue" field when it forwards a request, then it need not forward the corresponding 100 (Continue) response(s).
<h2>100</h2>
The <b>100 (Continue)</b> status code indicates that the initial part of a request has been received and has not yet been rejected by the server. The server intends to send a final response after the request has been fully received and acted upon.
<br><br>
When the request contains an Expect header field that includes a 100-continue expectation, the 100 response indicates that the server wishes to receive the request payload body. The client ought to continue sending the request and discard the 100 response.
<br><br>
If the request did not contain an Expect header field containing the 100-continue expectation, the client can simply discard this interim response.
<h2>101</h2>
The <b>101 (Switching Protocols)</b> status code indicates that the server understands and is willing to comply with the client's request, via the Upgrade header field, for a change in the application protocol being used on this connection. The server MUST generate an Upgrade header field in the response that indicates which protocol(s) will be switched to immediately after the empty line that terminates the 101 response.
<br><br>
It is assumed that the server will only agree to switch protocols when it is advantageous to do so. For example, switching to a newer version of HTTP might be advantageous over older versions, and switching to a real-time, synchronous protocol might be advantageous when delivering resources that use such features.
<h1>2XX</h1>
The 2XX (Successful) class of status code indicates that the client's request was successfully received, understood, and accepted.
<h2>200</h1>
The <b>200 (OK)</b> status code indicates that the request has succeeded. The payload sent in a 200 response depends on the request method. For the methods defined by this specification, the intended meaning of the payload can be summarized as:
<ul>
<li><b>GET</b> - A representation of the target resource.</li>
<li><b>HEAD</b> - Ahe same representation as GET, but without the representation data.</li>
<li><b>POST</b> - A representation of the status of, or results obtained from, the action.</li>
<li><b>PUT, DELETE</b> - A representation of the status of the action.</li>
<li><b>OPTIONS</b> - A representation of the communications options.</li>
<li><b>TRACE</b> - A representation of the request message as received by the end server.</li>
</ul>
Aside from responses to CONNECT, a 200 response always has a payload, though an origin server MAY generate a payload body of zero length. If no payload is desired, an origin server ought to send 204 (No Content) instead. For CONNECT, no payload is allowed because the successful result is a tunnel, which begins immediately after the 200 response header section.
<br><br>
A 200 response is cacheable by default; i.e., unless otherwise indicated by the method definition or explicit cache controls.
<h2>201</h2>
The <b>201 (Created)</b> status code indicates that the request has been fulfilled and has resulted in one or more new resources being created. The primary resource created by the request is identified by either a Location header field in the response or, if no Location field is received, by the effective request URI.
<br><br>
The 201 response payload typically describes and links to the resource(s) created.
<h2>202</h2>
The <b>202 (Accepted)</b> status code indicates that the request has been accepted for processing, but the processing has not been completed. The request might or might not eventually be acted upon, as it might be disallowed when processing actually takes place. There is no facility in HTTP for re-sending a status code from an asynchronous operation.
<br><br>
The 202 response is intentionally noncommittal. Its purpose is to allow a server to accept a request for some other process (perhaps a batch-oriented process that is only run once per day) without requiring that the user agent's connection to the server persist until the process is completed. The representation sent with this response ought to describe the request's current status and point to (or embed) a status monitor that can provide the user with an estimate of when the request will be fulfilled.
<h2>203</h2>
The <b>203 (Non-Authoritative Information)</b> status code indicates that the request was successful but the enclosed payload has been modified from that of the origin server's 200 (OK) response by a transforming proxy. This status code allows the proxy to notify recipients when a transformation has been applied, since that knowledge might impact later decisions regarding the content. For example, future cache validation requests for the content might only be applicable along the same request path (through the same proxies).
<br><br>
The 203 response is similar to the Warning code of 214 Transformation Applied, which has the advantage of being applicable to responses with any status code.
<br><br>
A 203 response is cacheable by default; i.e., unless otherwise indicated by the method definition or explicit cache controls.
<h2>204</h2>
The <b>204 (No Content)</b> status code indicates that the server has successfully fulfilled the request and that there is no additional content to send in the response payload body. Metadata in the response header fields refer to the target resource and its selected representation after the requested action was applied.
<br><br>
For example, if a 204 status code is received in response to a PUT request and the response contains an ETag header field, then the PUT was successful and the ETag field-value contains the entity-tag for the new representation of that target resource.
<br><br>
The 204 response allows a server to indicate that the action has been successfully applied to the target resource, while implying that the user agent does not need to traverse away from its current "document view" (if any). The server assumes that the user agent will provide some indication of the success to its user, in accord with its own interface, and apply any new or updated metadata in the response to its active representation.
<br><br>
For example, a 204 status code is commonly used with document editing interfaces corresponding to a "save" action, such that the document being saved remains available to the user for editing. It is also frequently used with interfaces that expect automated data transfers to be prevalent, such as within distributed version control systems.
<br><br>
A 204 response is terminated by the first empty line after the header fields because it cannot contain a message body.
<br><br>
A 204 response is cacheable by default; i.e., unless otherwise indicated by the method definition or explicit cache controls.
<h2>205</h2>
The <b>205 (Reset Content)</b> status code indicates that the server has fulfilled the request and desires that the user agent reset the "document view", which caused the request to be sent, to its original state as received from the origin server.
<br><br>
This response is intended to support a common data entry use case where the user receives content that supports data entry (a form, notepad, canvas, etc.), enters or manipulates data in that space, causes the entered data to be submitted in a request, and then the data entry mechanism is reset for the next entry so that the user can easily initiate another input action.
<br><br>
Since the 205 status code implies that no additional content will be provided, a server MUST NOT generate a payload in a 205 response. In other words, a server MUST do one of the following for a 205 response: a) indicate a zero-length body for the response by including a Content-Length header field with a value of 0; b) indicate a zero-length payload for the response by including a Transfer-Encoding header field with a value of chunked and a message body consisting of a single chunk of zero-length; or, c) close the connection immediately after sending the blank line terminating the header section.
<h1>3XX</h1>
The 3xx (Redirection) class of status code indicates that further action needs to be taken by the user agent in order to fulfill the request. If a Location header field is provided, the user agent MAY automatically redirect its request to the URI referenced by the Location field value, even if the specific status code is not understood. Automatic redirection needs to done with care for methods not known to be safe, since the user might not wish to redirect an unsafe request.
<br><br>
There are several types of redirects:
<ul>
  <li>Redirects that indicate the resource might be available at a different URI, as provided by the Location field, as in the status codes 301 (Moved Permanently), 302 (Found), and 307 (Temporary Redirect).</li>
  <li>Redirection that offers a choice of matching resources, each capable of representing the original request target, as in the 300 (Multiple Choices) status code.</li>
  <li>Redirection to a different resource, identified by the Location field, that can represent an indirect response to the request, as in the 303 (See Other) status code.</li>
  <li>Redirection to a previously cached result, as in the 304 (Not Modified) status code.</li>
</ul>
<b>Note:</b> In HTTP/1.0, the status codes 301 (Moved Permanently) and 302 (Found) were defined for the first type of redirect. Early user agents split on whether the method applied to the redirect target would be the same as the original request or would be rewritten as GET. Although HTTP originally defined the former semantics for 301 and 302 (to match its original implementation at CERN), and defined 303 (See Other) to match the latter semantics, prevailing practice gradually converged on the latter semantics for 301 and 302 as well. The first revision of HTTP/1.1 added 307 (Temporary Redirect) to indicate the former semantics without being impacted by divergent practice. Over 10 years later, most user agents still do method rewriting for 301 and 302; therefore, this specification makes that behavior conformant when the original request is POST.
<br><br>
A client SHOULD detect and intervene in cyclical redirections (i.e., "infinite" redirection loops).
<br><br>
<b>Note:</b> An earlier version of this specification recommended a maximum of five redirections. Content developers need to be aware that some clients might implement such a fixed limitation.
<h2>300</h2>
The 300 (Multiple Choices) status code indicates that the target resource has more than one representation, each with its own more specific identifier, and information about the alternatives is being provided so that the user (or user agent) can select a preferred representation by redirecting its request to one or more of those identifiers. In other words, the server desires that the user agent engage in reactive negotiation to select the most appropriate representation(s) for its needs.
<br><br>
If the server has a preferred choice, the server SHOULD generate a Location header field containing a preferred choice's URI reference. The user agent MAY use the Location field value for automatic redirection.
<br><br>
For request methods other than HEAD, the server SHOULD generate a payload in the 300 response containing a list of representation metadata and URI reference(s) from which the user or user agent can choose the one most preferred. The user agent MAY make a selection from that list automatically if it understands the provided media type. A specific format for automatic selection is not defined by this specification because HTTP tries to remain orthogonal to the definition of its payloads. In practice, the representation is provided in some easily parsed format believed to be acceptable to the user agent, as determined by shared design or content negotiation, or in some commonly accepted hypertext format.
<br><br>
A 300 response is cacheable by default; i.e., unless otherwise indicated by the method definition or explicit cache controls.
<br><br>
<b>Note:</b> The original proposal for the 300 status code defined the URI header field as providing a list of alternative representations, such that it would be usable for 200, 300, and 406 responses and be transferred in responses to the HEAD method. However, lack of deployment and disagreement over syntax led to both URI and Alternates (a subsequent proposal) being dropped from this specification. It is possible to communicate the list using a set of Link header fields, each with a relationship of "alternate", though deployment is a chicken-and-egg problem.
<h2>301</h2>
The <b>301 (Moved Permanently)</b> status code indicates that the target resource has been assigned a new permanent URI and any future references to this resource ought to use one of the enclosed URIs. Clients with link-editing capabilities ought to automatically re-link references to the effective request URI to one or more of the new references sent by the server, where possible.
<br><br>
The server SHOULD generate a Location header field in the response containing a preferred URI reference for the new permanent URI. The user agent MAY use the Location field value for automatic redirection. The server's response payload usually contains a short hypertext note with a hyperlink to the new URI(s).
<br><br>
<b>Note:</b> For historical reasons, a user agent MAY change the request method from POST to GET for the subsequent request. If this behavior is undesired, the 307 (Temporary Redirect) status code can be used instead.
<br><br>
A 301 response is cacheable by default; i.e., unless otherwise indicated by the method definition or explicit cache controls.
<h2>302</h2>
The <b>302 (Found)</b> status code indicates that the target resource resides temporarily under a different URI. Since the redirection might be altered on occasion, the client ought to continue to use the effective request URI for future requests.
<br><br>
The server SHOULD generate a Location header field in the response containing a URI reference for the different URI. The user agent MAY use the Location field value for automatic redirection. The server's response payload usually contains a short hypertext note with a hyperlink to the different URI(s).
<br><br>
<b>Note:</b> For historical reasons, a user agent MAY change the request method from POST to GET for the subsequent request. If this behavior is undesired, the 307 (Temporary Redirect) status code can be used instead.
<h2>303</h2>
The <b>303 (See Other)</b> status code indicates that the server is redirecting the user agent to a different resource, as indicated by a URI in the Location header field, which is intended to provide an indirect response to the original request. A user agent can perform a retrieval request targeting that URI (a GET or HEAD request if using HTTP), which might also be redirected, and present the eventual result as an answer to the original request. Note that the new URI in the Location header field is not considered equivalent to the effective request URI.
<br><br>
This status code is applicable to any HTTP method. It is primarily used to allow the output of a POST action to redirect the user agent to a selected resource, since doing so provides the information corresponding to the POST response in a form that can be separately identified, bookmarked, and cached, independent of the original request.
<br><br>
A 303 response to a GET request indicates that the origin server does not have a representation of the target resource that can be transferred by the server over HTTP. However, the Location field value refers to a resource that is descriptive of the target resource, such that making a retrieval request on that other resource might result in a representation that is useful to recipients without implying that it represents the original target resource. Note that answers to the questions of what can be represented, what representations are adequate, and what might be a useful description are outside the scope of HTTP.
<br><br>
Except for responses to a HEAD request, the representation of a 303 response ought to contain a short hypertext note with a hyperlink to the same URI reference provided in the Location header field.
<h2>305</h2>
The <b>305 (Use Proxy)</b> status code was defined in a previous version of this specification and is now deprecated (Appendix B).
<h2>306</h2>
The <b>306 (Not Used)</b> status code was defined in a previous version of this specification, is no longer used, and the code is reserved.
<h2>307</h2>
The <b>307 (Temporary Redirect)</b> status code indicates that the target resource resides temporarily under a different URI and the user agent MUST NOT change the request method if it performs an automatic redirection to that URI. Since the redirection can change over time, the client ought to continue using the original effective request URI for future requests.
<br><br>
The server SHOULD generate a Location header field in the response containing a URI reference for the different URI. The user agent MAY use the Location field value for automatic redirection. The server's response payload usually contains a short hypertext note with a hyperlink to the different URI(s).
<br><br>
<b>Note:</b> This status code is similar to 302 (Found), except that it does not allow changing the request method from POST to GET. This specification defines no equivalent counterpart for 301 (Moved Permanently), (however, defines the status code 308 (Permanent Redirect) for this purpose).
<h1>4XX</h1>
The <b>4XX (Client Error)</b> class of status code indicates that the client seems to have erred. Except when responding to a HEAD request, the server SHOULD send a representation containing an explanation of the error situation, and whether it is a temporary or permanent condition. These status codes are applicable to any request method. User agents SHOULD display any included representation to the user.
<h2>400</h2>
The <b>400 (Bad Request)</b> status code indicates that the server cannot or will not process the request due to something that is perceived to be a client error (e.g., malformed request syntax, invalid request message framing, or deceptive request routing).
<h2>401</h2>
The <b>401 (Unauthorized)</b> status code indicates that the request has not been applied because it lacks valid authentication credentials for the target resource. The server generating a 401 response MUST send a WWW-Authenticate header field containing at least one challenge applicable to the target resource.
<br><br>
If the request included authentication credentials, then the 401 response indicates that authorization has been refused for those credentials. The user agent MAY repeat the request with a new or replaced Authorization header field. If the 401 response contains the same challenge as the prior response, and the user agent has already attempted authentication at least once, then the user agent SHOULD present the enclosed representation to the user, since it usually contains relevant diagnostic information.
<h2>402</h2>
The <b>402 (Payment Required)</b> status code is reserved for future use.
<h2>403</h2>
The <b>403 (Forbidden)</b> status code indicates that the server understood the request but refuses to authorize it. A server that wishes to make public why the request has been forbidden can describe that reason in the response payload (if any).
<br><br>
If authentication credentials were provided in the request, the server considers them insufficient to grant access. The client SHOULD NOT automatically repeat the request with the same credentials. The client MAY repeat the request with new or different credentials. However, a request might be forbidden for reasons unrelated to the credentials.
<br><br>
An origin server that wishes to "hide" the current existence of a forbidden target resource MAY instead respond with a status code of 404 (Not Found).
<h2>404</h2>
The 404 (Not Found) status code indicates that the origin server did not find a current representation for the target resource or is not willing to disclose that one exists. A 404 status code does not indicate whether this lack of representation is temporary or permanent; the 410 (Gone) status code is preferred over 404 if the origin server knows, presumably through some configurable means, that the condition is likely to be permanent.
<br><br>
A 404 response is cacheable by default; i.e., unless otherwise indicated by the method definition or explicit cache controls.
<h2>405</h2>
The <b>405 (Method Not Allowed)</b> status code indicates that the method received in the request-line is known by the origin server but not supported by the target resource. The origin server MUST generate an Allow header field in a 405 response containing a list of the target resource's currently supported methods.
<br><br>
A 405 response is cacheable by default; i.e., unless otherwise indicated by the method definition or explicit cache control.
<h2>406</h2>
The <b>406 (Not Acceptable)</b> status code indicates that the target resource does not have a current representation that would be acceptable to the user agent, according to the proactive negotiation header fields received in the request, and the server is unwilling to supply a default representation.
<br><br>
The server SHOULD generate a payload containing a list of available representation characteristics and corresponding resource identifiers from which the user or user agent can choose the one most appropriate. A user agent MAY automatically select the most appropriate choice from that list. However, this specification does not define any standard for such automatic selection, as described in Status 300.
<h2>407</h2>
The <b>407 (Proxy Authentication Required)</b> status code is similar to 401, but it indicates that the client needs to authenticate itself in order to use a proxy. The proxy MUST send a Proxy-Authenticate header field containing a challenge applicable to that proxy for the target resource. The client MAY repeat the request with a new or replaced Proxy-Authorization header field.
<h2>408</h2>
The <b>408 (Request Timeout)</b> status code indicates that the server did not receive a complete request message within the time that it was prepared to wait. A server SHOULD send the "close" connection option in the response, since 408 implies that the server has decided to close the connection rather than continue waiting. If the client has an outstanding request in transit, the client MAY repeat that request on a new connection.
<h2>409</h2>
The <b>409 (Conflict)</b> status code indicates that the request could not be completed due to a conflict with the current state of the target resource. This code is used in situations where the user might be able to resolve the conflict and resubmit the request. The server SHOULD generate a payload that includes enough information for a user to recognize the source of the conflict.
<br><br>
Conflicts are most likely to occur in response to a PUT request. For example, if versioning were being used and the representation being PUT included changes to a resource that conflict with those made by an earlier (third-party) request, the origin server might use a 409 response to indicate that it can't complete the request. In this case, the response representation would likely contain information useful for merging the differences based on the revision history.
<h2>410</h2>
The <b>410 (Gone)</b> status code indicates that access to the target resource is no longer available at the origin server and that this condition is likely to be permanent. If the origin server does not know, or has no facility to determine, whether or not the condition is permanent, the status code 404 ought to be used instead.
<br><br>
The 410 response is primarily intended to assist the task of web maintenance by notifying the recipient that the resource is intentionally unavailable and that the server owners desire that remote links to that resource be removed. Such an event is common for limited-time, promotional services and for resources belonging to individuals no longer associated with the origin server’s site. It is not necessary to mark all permanently unavailable resources as "gone" or to keep the mark for any length of time — that is left to the discretion of the server owner.
<br><br>
A 410 response is cacheable by default; i.e., unless otherwise indicated by the method definition or explicit cache controls
<h2>411</h2>
The <b>411 (Length Required)</b> status code indicates that the server refuses to accept the request without a defined Content-Length. The client MAY repeat the request if it adds a valid Content-Length header field containing the length of the message body in the request message.
<h2>412</h2>
The <b>412 (Precondition Failed)</b> status code indicates that one or more conditions given in the request header fields evaluated to false when tested on the server. This response code allows the client to place preconditions on the current resource state (its current representations and metadata) and, thus, prevent the request method from being applied if the target resource is in an unexpected state.
<h2>413</h2>
The <b>413 (Payload Too Large)</b> status code indicates that the server is refusing to process a request because the request payload is larger than the server is willing or able to process. The server MAY close the connection to prevent the client from continuing the request.
<br><br>
If the condition is temporary, the server SHOULD generate a Retry-After header field to indicate that it is temporary and after what time the client MAY try again.
<h2>414</h2>
The <b>414 (URI Too Long)</b> status code indicates that the server is refusing to service the request because the request-target is longer than the server is willing to interpret. This rare condition is only likely to occur when a client has improperly converted a POST request to a GET request with long query information, when the client has descended into a "black hole" of redirection (e.g., a redirected URI prefix that points to a suffix of itself) or when the server is under attack by a client attempting to exploit potential security holes.
<br><br>
A 414 response is cacheable by default; i.e., unless otherwise indicated by the method definition or explicit cache controls.
<h2>415</h2>
The <b>415 (Unsupported Media Type)</b> status code indicates that the origin server is refusing to service the request because the payload is in a format not supported by this method on the target resource. The format problem might be due to the request's indicated Content-Type or Content-Encoding, or as a result of inspecting the data directly.
<h2>416</h2>
The <b>416 (Range Not Satisfiable)</b> status code indicates that none of the ranges in the request’s Range header field overlap the current extent of the selected resource or that the set of ranges requested has been rejected due to invalid ranges or an excessive request of small or overlapping ranges.
<br><br>
For byte ranges, failing to overlap the current extent means that the first-byte-pos of all of the byte-range-spec values were greater than the current length of the selected representation. When this status code is generated in response to a byte-range request, the sender SHOULD generate a Content-Range header field specifying the current length of the selected representation.
<br><br>
Example:
<pre>
HTTP/1.1 416 Range Not Satisfiable
Date: Fri, 20 Jan 2012 15:41:54 GMT
Content-Range: bytes */47022
</pre>
Note: Because servers are free to ignore Range, many implementations will simply respond with the entire selected representation in a 200 response. That is partly because most clients are prepared to receive a 200 to complete the task (albeit less efficiently) and partly because clients might not stop making an invalid partial request until they have received a complete representation. Thus, clients cannot depend on receiving a 416 response even when it is most appropriate.
<h2>417</h2>
The <b>417 (Expectation Failed)</b> status code indicates that the expectation given in the request's Expect header field could not be met by at least one of the inbound servers.
<h2>426</h2>
The <b>426 (Upgrade Required)</b> status code indicates that the server refuses to perform the request using the current protocol but might be willing to do so after the client upgrades to a different protocol. The server MUST send an Upgrade header field in a 426 response to indicate the required protocol(s).
<br><br>
Example:
<pre>
HTTP/1.1 426 Upgrade Required
Upgrade: HTTP/3.0
Connection: Upgrade
Content-Length: 53
Content-Type: text/plain<br>
This service requires use of the HTTP/3.0 protocol.
</pre>
<h1>5XX</h2>
The <b>5XX (Server Error)</b> class of status code indicates that the server is aware that it has erred or is incapable of performing the requested method. Except when responding to a HEAD request, the server SHOULD send a representation containing an explanation of the error situation, and whether it is a temporary or permanent condition. A user agent SHOULD display any included representation to the user. These response codes are applicable to any request method.
<h2>500</h2>
The <b>500 (Internal Server Error)</b> status coThe 504 (Gateway Timeout) status code indicates that the server, while acting as a gateway or proxy, did not receive a timely response from an upstream server it needed to access in order to complete the request.de indicates that the server encountered an unexpected condition that prevented it from fulfilling the request.
<h2>501</h2>
The <b>501 (Not Implemented)</b> status code indicates that the server does not support the functionality required to fulfill the request. This is the appropriate response when the server does not recognize the request method and is not capable of supporting it for any resource.
<br><br>
A 501 response is cacheable by default; i.e., unless otherwise indicated by the method definition or explicit cache controls.
<h2>502</h2>
The <b>502 (Bad Gateway)</b> status code indicates that the server, while acting as a gateway or proxy, received an invalid response from an inbound server it accessed while attempting to fulfill the request.
<h2>503</h2>
The <b>503 (Service Unavailable)</b> status code indicates that the server is currently unable to handle the request due to a temporary overload or scheduled maintenance, which will likely be alleviated after some delay. The server MAY send a Retry-After header field to suggest an appropriate amount of time for the client to wait before retrying the request.
<br><br>
<b>Note:</b> The existence of the 503 status code does not imply that a server has to use it when becoming overloaded. Some servers might simply refuse the connection.
<h2>504</h2>
The <b>504 (Gateway Timeout)</b> status code indicates that the server, while acting as a gateway or proxy, did not receive a timely response from an upstream server it needed to access in order to complete the request.
<h2>505</h2>
The <b>505 (HTTP Version Not Supported)</b> status code indicates that the server does not support, or refuses to support, the major version of HTTP that was used in the request message. The server is indicating that it is unable or unwilling to complete the request using the same major version as the client, other than with this error message. The server SHOULD generate a representation for the 505 response that describes why that version is not supported and what other protocols are supported by that server.
