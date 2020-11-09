# Web APIs

## Broadcast Channel API

The Broadcast Channel API allows communication between browsing contexts (windows, tabs, iframes) and workers on the same origin. Think of a use-case like, once you logout from an app running in a browser tab, you want to broadcast it to the app instances opened in other tabs of the same browser.

- [https://html.spec.whatwg.org/multipage/web-messaging.html#broadcasting-to-other-browsing-contexts](https://html.spec.whatwg.org/multipage/web-messaging.html#broadcasting-to-other-browsing-contexts)


## Domains

### Testing
There are official domains you’re supposed to use for documentation, testing, etc. They are specifically reserved by IANA for these purposes. Originally it was just example.com, but they now have a list of all them: [https://www.iana.org/domains/reserved](https://www.iana.org/domains/reserved)


## Requests
### Request limits
Can HTTP POST be limitless?
```
The HTTP protocol does not specify a limit.
The POST method allows sending far more data than the GET method, which is limited by the URL length - about 2KB.
The maximum POST request body size is configured on the HTTP server and typically ranges from
1MB to 2GB
The HTTP client (browser or other user agent) can have its own limitations. Therefore, the maximum POST body request size is min(serverMaximumSize, clientMaximumSize).
```
taken from this [StackOverflow answer](https://stackoverflow.com/a/55998160/818739)