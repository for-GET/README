# Forget HTTP

This GitHub organization focuses on designing abstract HTTP helpers or coding reference implementations, as described in IETF/W3C/etc specifications.

**This is one of the least opinionated collection of repositories that you will find on HTTP.**

TODO explanations/references


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
* 1.1. and 1.2. need parsers
    * [Core PEGjs](https://github.com/for-GET/core-pegjs)
* 2.1., 3.1. and 3.2. need helpers/generators
    * [API PEGjs](https://github.com/for-GET/api-pegjs)
