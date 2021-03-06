<img src="https://raw.github.com/cfregly/fluxcapacitor/master/docs/images/fluxcapacitor-logo.png">

Overview
========
Flux Capacitor is a Java-based distributed application demonstrating the following Netflix Open Source components (in alphabetical order):
* [archaius] (https://github.com/Netflix/archaius) configuration
* [astyanax] (https://github.com/Netflix/astyanax) cassandra client
* [blitz4j] (https://github.com/Netflix/blitz4j) asynchronous logging
* [curator] (https://github.com/Netflix/curator) zookeeper client
* [eureka] (https://github.com/Netflix/eureka) discovery service
* [exhibitor] (https://github.com/Netflix/exhibitor) zookeeper administration
* [governator] (https://github.com/Netflix/governator) guice-based dependency injection extensions
* [hystrix] (https://github.com/Netflix/hystrix) circuit breaker
* [karyon] (https://github.com/Netflix/karyon) common base server
* [ribbon] (https://github.com/Netflix/ribbon) eureka-based REST client
* [servo] (https://github.com/Netflix/servo) metrics

In addition to the Netflix OSS components listed above, Flux Capacitor uses the following Open Source components:
* [graphite] (http://graphite.wikidot.com) metrics
* [guava] (https://code.google.com/p/guava-libraries/)
* [guice] (https://code.google.com/p/google-guice/)
* [jersey] (http://jersey.java.net) REST 
* [jetty] (http://jetty.codehaus.org/jetty) servlet container 
* [jmeter] (http://jmeter.apache.org) jmeter load test
* [netty] (http://netty.io) io server 
* [tomcat] (http://tomcat.apache.org/) servlet container

This project demonstrates many aspects of a complete distributed, scalable application from dynamic configuration to real-time metrics.

This app can be run standalone in a data center, but is optimized for an Amazon Web Services environment.

Architecture Overview
=====================
<img src="https://raw.github.com/cfregly/fluxcapacitor/master/docs/images/fluxcapacitor-netflixoss-overview.jpg">

Real-time Metrics
=================================
Hystrix Dashboard
-----------------
<img src="https://raw.github.com/cfregly/fluxcapacitor/master/docs/images/fluxcapacitor-hystrix-dashboard.jpg">

Historical Metrics
=================================
Graphite Dashboard
------------------
<img src="https://raw.github.com/cfregly/fluxcapacitor/master/docs/images/fluxcapacitor-graphite-dashboard.jpg">

CloudWatch Dashboard
--------------------
<img src="https://raw.github.com/cfregly/fluxcapacitor/master/docs/images/fluxcapacitor-cloudwatch-dashboard.jpg">

Project Overview
================
The following project layout is typical of many distributed applications: 

flux-edge
---------
* Customer-facing REST-based edge service
* Uses Jetty as the servlet container and messaging engine

flux-middletier
---------------
* Internal REST-based middletier service called by the edge service  
* Uses Netty as the messaging engine

flux-core
---------
* Shared classes between edge and middletier

Documentation
==============
Please see [wiki] (https://github.com/cfregly/fluxcapacitor/wiki) for detailed documentation.