# Forget HTTP

This GitHub organization focuses on designing abstract HTTP helpers or coding reference implementations, as described in IETF/W3C/etc specifications.

**This is one of the least opinionated collection of repositories that you will find on HTTP.**

## More bla

* http://www.youtube.com/watch?v=9Qnx1h5cQxo
* http://hyperrest.github.io/2013-06-10-http-hell-no/
* http://hyperrest.github.io/2013-10-14-man-overboard/
* http://www.youtube.com/watch?v=UqTlToUYK1E
* https://vimeo.com/20784244
* http://seancribbs.com/tech/2012/01/16/webmachine-vs-grape/


## HTTP flow overview

\* HTTP/2.0 encapsulation is omitted

1. receive request
    1. parse messaging - [p1-messaging](http://tools.ietf.org/html/draft-ietf-httpbis-p1-messaging)
    2. parse semantics - [p2-semantics](http://tools.ietf.org/html/draft-ietf-httpbis-p2-semantics) (and extensions)
2. prepare response
    1. decide
3. send response
    1. generate semantics
    2. generate messaging


## Effort overview (roadmap)

Dependencies and their reference implementations:

* 1. and 3. need a server
    * [HTTPDD Server](https://github.com/for-GET/server)
* 2. needs an FSM
    * [HTTPDD (HTTP decision diagram)](https://github.com/for-GET/http-decision-diagram)
    * [HTTPDD Machine](https://github.com/for-GET/machine)
* 1.i. and 1.ii. need parsers
    * [Core PEGjs](https://github.com/for-GET/core-pegjs)
* 2.i., 3.i. and 3.ii. need helpers/generators
    * [API PEGjs](https://github.com/for-GET/api-pegjs)
* 1., 2. and 3. need language agnostic tests
    * [parse->AST->stringify (API PEGjs)](https://github.com/for-GET/api-pegjs-test)
    * Decision
        * [Content Negotiation](https://github.com/for-GET/conneg-test)
        * Caching
        * Conditional
        * ...
