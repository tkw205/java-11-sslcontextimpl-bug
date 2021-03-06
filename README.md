# Java 11 SSLContextImpl [![Build Status](https://travis-ci.org/ogolberg/java-11-sslcontextimpl-bug.svg?branch=master)](https://travis-ci.org/ogolberg/java-11-sslcontextimpl-bug)

This project demonstrates a change in SSLContextImpl's behavior introduced in Java 11. 

On Java 10-, SSLContextImpl rethrows a SocketException.

On Java 11, SSLContextImpl wraps a SocketException in an SSLException, typically an SSLProtocolException.

See http://mail.openjdk.java.net/pipermail/jdk-dev/2018-November/002237.html

This project's SSLContextImplIntegrationTest passes on Java 10- and fails on Java 11 (see [linked Travis build](https://travis-ci.org/ogolberg/java-11-sslcontextimpl-bug)).
