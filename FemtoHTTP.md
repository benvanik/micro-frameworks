# FemtoHTTP #

FemtoHTTP is a lightweight subsystem for handling HTTP network traffic that compiles as a framework for OS X and a static library for the iPhone/iPod Touch. It doesn't support much now, but is designed to work better than the sack of suck that is CFNetwork.

Status: **in progress**
  * Source: [FemtoHTTP/](http://code.google.com/p/micro-frameworks/source/browse/#svn/FemtoHTTP/trunk/FemtoHTTP)
  * Documentation: TODO
  * Binaries: TODO

## Features ##
  * Fully compatible with the iPhone SDK
  * Pure Objective C
  * No external dependencies
  * Trivial to consume
  * Full HTTP/1.1 support (keep-alive, chunked encoding, etc)
  * Connection pooling
  * Cookies
  * HTTP compression (gzip/deflate)

## Limitations ##
The goal of the framework is to remain small, easy to use, and general, and as such it does not contain a lot of fluff features. Below are some of the things that I left out, but may add in the future.
  * No HTTPS - could add SSL as an optional dependency
  * No HTTP authentication - don't care

## TODO ##
  * Feature list, in decreasing order of importance:
    1. 'Keep-Alive: timeout=N, max=M' support
    1. Partial content (Content-Range/Range/206)
    1. Automatic redirect following
    1. Proxy authentication
    1. Pipelining mode (batch requests/responses)
  * Unit tests (also test for memory leaks)
    * Different servers
    * Pooling
    * String encodings
    * IPv6
    * Proxies/authenticated proxies
    * POST/HEAD
    * Cookies
    * Socket stuff
    * Redirects
    * Compression
  * Better memory behavior (less autorelease so less pool clutter)