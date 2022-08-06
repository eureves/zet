# HSTS (HTTP Strict Transport Security)

HSTS is a header of HTTP response, this header triggers special redirect known as "307 Internal redirect" to HTTPS.
When the browser makes first request via HTTPS it saves that information so when you make HTTP request it automaticaly will redirect to HTTPS internaly.
There's also a hardcoded list of preloaded HSTS for Chrome.
This list of websites always will use HTTPS. "https://hstspreload.org".

* Allows browser to allways use HTTPS over HTTP.
* Internal redirect is handled by the browser rather than server.
* Since the HTTP request never leaves the browser it cannot be intercepted.

#security #http 
