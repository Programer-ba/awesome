<div class="github-widget" data-repo="vert-x3/vertx-awesome"></div>
## Awesome Vert.x [![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/sindresorhus/awesome)

[<img src="https://raw.githubusercontent.com/vert-x3/vertx-awesome/master/logo-sm.png" align="right" width="250">](http://vertx.io)

*Awesome Vert.x* is a list of awesome frameworks, libraries or other components for use with or that use
[Vert.x](https://github.com/eclipse/vert.x) version 3.

If you want your component to appear here send a pull request to this repository to add it.

Please note that we can't vouch for the stability or production-worthiness of everything on this list unless it has
the icon <img src="https://rawgit.com/vert-x3/vertx-awesome/d93d327/vertx-favicon.svg" alt="(stack)" title="Vert.x Stack" height="16px">
next to it. This icon means the component is part of the official
[Vert.x stack](https://vertx.io/docs/).

For Vert.x version 2 check [this page](https://github.com/vert-x3/vertx-awesome/blob/master/./vert-x2.md).



## Books

* [A gentle guide to asynchronous programming with Eclipse Vert.x for Java developers](http://vertx.io/docs/guide-for-java-devs/) by Julien Ponge, Thomas Segismont and Julien Viet
* [Building Reactive Microservices in Java](https://developers.redhat.com/promotions/building-reactive-microservices-in-java/) by Clément Escoffier
* [Vert.x in Action](https://www.manning.com/books/vertx-in-action) by Julien Ponge

## Build tools

* [Vert.x Maven plugin](https://github.com/fabric8io/vertx-maven-plugin)
* [Vert.x Gradle plugin](https://plugins.gradle.org/plugin/io.vertx.vertx-plugin)

## Web Frameworks

* [Vert.x Jersey](https://github.com/englishtown/vertx-jersey) - Create JAX-RS [Jersey](https://jersey.java.net/) resources in Vert.x.
* [Kovert](https://github.com/kohesive/kovert) - Invisible REST framework for Kotlin + Vert.x Web.
* [Handlers](https://github.com/spriet2000/vertx-handlers-http) - Open web framework for Vert.x.
* [QBit](https://github.com/advantageous/qbit) - REST and WebSocket method call marshaling and reactive library.
* [vertx-rest-storage](https://github.com/swisspush/vertx-rest-storage) - Persistence for REST resources in the filesystem or a redis database.
* [Jubilee](https://github.com/isaiah/jubilee) - A rack compatible Ruby HTTP server built on Vert.x 3.
* [Knot.x](https://github.com/Cognifide/knotx) - Efficient & high-performance integration platform for modern websites built on Vert.x 3.
* [Vert.x Jspare](https://github.com/jspare-projects/vertx-jspare) - Improving your Vert.x 3 experience with Jspare Framework.
* [Irked](https://github.com/GreenfieldTech/irked) - Annotations-based configuration for Vert.x 3 Web and controller framework.
* [REST.VertX](https://github.com/zandero/rest.vertx) - Lightweight JAX-RS (RestEasy) like annotation processor for Vert.x verticals.
* [Atmosphere Vert.x](https://github.com/Atmosphere/atmosphere-vertx) - Realtime Client Server Framework for the JVM, supporting WebSockets and Server Sent Events with Cross-Browser Fallbacks.
* [Vert.x Vaadin](https://github.com/mcollovati/vertx-vaadin) - Run Vaadin applications on Vert.x.

## Authentication Authorisation


* [Vert.x-Pac4j](https://github.com/pac4j/vertx-pac4j) - Vert.x authentication/authorisation implemented using [pac4j](http://www.pac4j.org/).

## Database Clients

*Clients for connecting to databases*

* Relational Databases
  * [JDBC](https://raw.githubusercontent.com/vert-x3/vertx-jdbc-client) <img src="https://rawgit.com/vert-x3/vertx-awesome/d93d327/vertx-favicon.svg" alt="(stack)" title="Vert.x Stack" height="16px"> - Asynchronous interface around a JDBC datasource.
  * [MySQL / PostgreSQL](https://raw.githubusercontent.com/vert-x3/vertx-mysql-postgresql-client) <img src="https://rawgit.com/vert-x3/vertx-awesome/d93d327/vertx-favicon.svg" alt="(stack)" title="Vert.x Stack" height="16px"> - Asynchronous Client for MySQL/PostgreSQL.
  * [PostgreSQL](https://github.com/vietj/reactive-pg-client) - Reactive PostgreSQL Client.
  * [database](https://github.com/susom/database) - Client for Oracle, PostgreSQL, SQL Server, HyperSQL, etc. designed for security, correctness, and ease of use.
  * [jOOQ](https://github.com/jklingsporn/vertx-jooq) - Doing typesafe, asynchronous SQL and generate code using jOOQ.

* NoSQL Databases
  * [MongoDB](https://raw.githubusercontent.com/vert-x3/vertx-mongo-client) <img src="https://rawgit.com/vert-x3/vertx-awesome/d93d327/vertx-favicon.svg" alt="(stack)" title="Vert.x Stack" height="16px"> - An asynchronous client for interacting with a MongoDB database.
  * [Redis](https://raw.githubusercontent.com/vert-x3/vertx-redis-client) <img src="https://rawgit.com/vert-x3/vertx-awesome/d93d327/vertx-favicon.svg" alt="(stack)" title="Vert.x Stack" height="16px"> - Asynchronous API to interact with Redis.
  * [Cassandra](https://raw.githubusercontent.com/vert-x3/vertx-cassandra-client) <img src="https://rawgit.com/vert-x3/vertx-awesome/d93d327/vertx-favicon.svg" alt="(stack)" title="Vert.x Stack" height="16px"> - A Vert.x client allowing applications to interact with a Cassandra service.
  * [Cassandra](https://github.com/englishtown/vertx-cassandra) - Asynchronous API to interact with Cassandra and Cassandra Mapping.
  * [OrientDB](https://github.com/cstamas/vertx-orientdb) - Non-blocking OrientDB server integration.
  * [Bitsy](https://github.com/cstamas/vertx-bitsy) - Non-blocking Bitsy Graph server integration.
  * [MarkLogic](https://github.com/etourdot/vertx-marklogic) - Asynchronous client for Marklogic Database Server.
  * [SirixDB](https://github.com/sirixdb/sirix/tree/master/bundles/sirix-rest-api) - Non-blocking SirixDB HTTP-server.

* [vertx-pojo-mapper](https://github.com/BraintagsGmbH/vertx-pojo-mapper) - Non-blocking POJO mapping for MySQL and MongoDB.
* [vertx-mysql-binlog-client](https://github.com/guoyu511/vertx-mysql-binlog-client) - A Vert.x client for tapping into MySQL replication stream.
* [vertx-mongo-streams](https://github.com/st-h/vertx-mongo-streams) - Helpers to pump Vert.x streams to/from MongoDB GridFS using the MongoDB async driver.

## Integration

* Server-Sent Events
  * [jEaSSE](https://github.com/mariomac/jeasse) - Java Easy SSE. A simple, lightweight implementation of SSE.
  * [vertx-sse](https://github.com/aesteve/vertx-sse) - Vert.x SSE implementation + event-bus SSE bridge.

* Mail
  * [SMTP](https://raw.githubusercontent.com/vert-x3/vertx-mail-client) <img src="https://rawgit.com/vert-x3/vertx-awesome/d93d327/vertx-favicon.svg" alt="(stack)" title="Vert.x Stack" height="16px"> - Async SMTP client.
  * [vertx-smtp-server](https://github.com/cinterloper/vertx-smtp-server) - SMTP server bridging to EventBus.

* REST
  * [Vert.x REST Client](https://github.com/hubrick/vertx-rest-client) - A REST client for Vert.x with support for RxJava and request caching.
  * [Retrofit adapter for Vert.x](https://github.com/vietj/retrofit-vertx) - A highly scalable adapter for Retrofit with Vert.x.

* Messaging
  * [AMQP 1.0](https://raw.githubusercontent.com/vert-x3/vertx-amqp-bridge) <img src="https://rawgit.com/vert-x3/vertx-awesome/d93d327/vertx-favicon.svg" alt="(stack)" title="Vert.x Stack" height="16px"> - Interact with AMQP 1.0 servers using the Vert.x Producer and Consumer APIs.
  * [MQTT](https://raw.githubusercontent.com/vert-x3/vertx-mqtt) <img src="https://rawgit.com/vert-x3/vertx-awesome/d93d327/vertx-favicon.svg" alt="(stack)" title="Vert.x Stack" height="16px"> - Provides two different components : an MQTT server for handling all the MQTT communication and messages exchanges with clients and an MQTT client for sending and receiving messages against an MQTT broker.
  * [RabbitMQ](https://raw.githubusercontent.com/vert-x3/vertx-rabbitmq-client) <img src="https://rawgit.com/vert-x3/vertx-awesome/d93d327/vertx-favicon.svg" alt="(stack)" title="Vert.x Stack" height="16px"> - A RabbitMQ client (AMQP 0.9.1).
  * [Kafka Client](https://raw.githubusercontent.com/vert-x3/vertx-kafka-client) <img src="https://rawgit.com/vert-x3/vertx-awesome/d93d327/vertx-favicon.svg" alt="(stack)" title="Vert.x Stack" height="16px"> - A Kafka client.
  * [kafka](https://github.com/cyngn/vertx-kafka) - Kafka client for consuming and producing messages.
  * [Kafka Service](https://github.com/hubrick/vertx-kafka-service) - Kafka producer and consumer with retry logic.
  * [SaltStack](https://github.com/cinterloper/vertx-salt) - A bi-directional bridge between the SaltStack event system and the Vert.x event bus.
  * [STOMP](https://raw.githubusercontent.com/vert-x3/vertx-stomp) <img src="https://rawgit.com/vert-x3/vertx-awesome/d93d327/vertx-favicon.svg" alt="(stack)" title="Vert.x Stack" height="16px"> - A Kafka client and server.
  * [ZeroMQ](https://github.com/dano/vertx-zeromq) - ZeroMQ Event Bus bridge.
  * [MQTT Broker](https://github.com/GruppoFilippetti/vertx-mqtt-broker) - MQTT Broker (MQTT ver. 3.1.1 and 3.1 compliant).
  * [Azure ServiceBus](https://github.com/TextBack/vertx-azure-servicebus) - Azure [ServiceBus](https://azure.microsoft.com/en-us/services/service-bus/) producer and consumer (fully async, doesn't use Microsoft Azure SDK).
  * [AMQP 1.0 - Kafka bridge](https://github.com/rhiot/amqp-kafka-bridge) - Bridge for sending/receiving messages to/from Apache Kafka using the AMQP 1.0 protocol.
  * [Vert.x Kafka Client](https://raw.githubusercontent.com/vert-x3/vertx-kafka-client) <img src="https://rawgit.com/vert-x3/vertx-awesome/d93d327/vertx-favicon.svg" alt="(stack)" title="Vert.x Stack" height="16px"> - Apache Kafka client for reading and sending messages from/to an Apache Kafka cluster.

* JavaEE
  * [JCA adaptor](https://raw.githubusercontent.com/vert-x3/vertx-jca) <img src="https://rawgit.com/vert-x3/vertx-awesome/d93d327/vertx-favicon.svg" alt="(stack)" title="Vert.x Stack" height="16px"> - Java Connector Architecture Adaptor for the Vert.x event bus.
  * [Weld](https://github.com/weld/weld-vertx) - Brings the CDI programming model into the Vert.x ecosystem (register CDI observer methods as Vert.x message consumers, CDI-powered Verticles, define routes in a declarative way, etc.).

* Meteor
  * [Meteor](https://github.com/jmusacchio/vertxbus/) - Meteor integration support through Vert.x event bus.

* Metrics
  * [Hawkular metrics](https://github.com/tsegismont/vertx-monitor) - [Hawkular](http://www.hawkular.org/) implementation of the Vert.x Metrics SPI.
  * [DropWizard metrics](https://raw.githubusercontent.com/vert-x3/vertx-dropwizard-metrics) <img src="https://rawgit.com/vert-x3/vertx-awesome/d93d327/vertx-favicon.svg" alt="(stack)" title="Vert.x Stack" height="16px"> - Metrics implementation using DropWizard metrics.
  * [Micrometer metrics](https://raw.githubusercontent.com/vert-x3/vertx-micrometer-metrics) <img src="https://rawgit.com/vert-x3/vertx-awesome/d93d327/vertx-favicon.svg" alt="(stack)" title="Vert.x Stack" height="16px"> - Metrics implementation using Micrometer metrics.
  * [OpenTsDb Metrics](https://github.com/cyngn/vertx-opentsdb) - [OpenTsDb](http://opentsdb.net/) metrics client for Vert.x.
  * [Bosun Monitoring](https://github.com/cyngn/vertx-bosun) - [Bosun](https://bosun.org/) client library for Vert.x.

* Netflix - Hystrix
  * [Hystrix Metrics Stream](https://github.com/kennedyoliveira/hystrix-vertx-metrics-stream.git) - Emits metrics for Hystrix Dashboard from a Vert.x application with [Hystrix](https://github.com/Netflix/Hystrix).

* Dart
  * [Vert.x Dart SockJS](https://github.com/wem/vertx-dart-sockjs) - [Dart](https://www.dartlang.org/) integration for [Vert.x SockJS bridge](http://vertx.io/docs/vertx-web/java/#_sockjs_event_bus_bridge) and plain SockJS with use of dart:js.

* Push Notifications
  * [Onesignal](https://github.com/jklingsporn/vertx-push-onesignal) - Send push notifications to (mobile/web) apps from your Vert.x application with [OneSignal](https://onesignal.com/).

* CNCF CloudEvents
  * [CloudEvents.io Java SDK](https://github.com/cloudevents/sdk-java) - Send and receive [CloudEvents](https://cloudevents.io/) using the [Vert.x HTTP Transport](https://github.com/cloudevents/sdk-java/blob/master/http/vertx/README.md) for CloudEvents.

## Middleware

* [Apache Camel](https://github.com/apache/camel/blob/master/components/camel-vertx/src/main/docs/vertx-component.adoc) - [Apache Camel](http://camel.apache.org/) component for bridging Camel with the Vert.x event bus.
* [Gateleen](https://github.com/swisspush/gateleen) - Middleware library based on Vert.x to build advanced JSON/REST communication servers.
* [Gravitee.io](https://gravitee.io) - An OSS API Platform including an API Gateway and an OAuth2 / OIDC authorization server based on Vert.x Core / Vert.x Web and other modules.

## Language Support

*Programming language support for Vert.x*

* [Python](https://github.com/vert-x3/vertx-lang-python) - Python support.
* [TypeScript](https://github.com/michel-kraemer/vertx-lang-typescript) - TypeScript support.
* [EcmaScript](https://github.com/reactiverse/es4x) - EcmaScript >=6 (JavaScript) support.

*Language extensions*

* [Grooveex](https://github.com/aesteve/grooveex) - Syntactic sugar + utilities (DSL builders, etc.) on top of [vertx-lang-groovy](https://github.com/vert-x3/vertx-lang-groovy).

## Reactive

* [vertx-util](https://github.com/cyngn/vertx-util) - Light weight promises & latches for Vert.x.
* [QBit](https://github.com/advantageous/qbit) - Async typed actor-like lib that runs easily in Vert.x Async Callbacks. Callback management.
* [VxRifa](https://nsforth.github.io/vxrifa) - Utility library for Vert.X that allows using strong-typed interfaces in communication through EventBus.

## Sync Thread Non Block

* [Sync](https://github.com/vert-x3/vertx-sync) - Synchronous but non-OS-thread-blocking verticles.

## Vert.x Event Bus Clients

*Clients to connect applications to the Vert.x event bus*

* [JavaScript](https://www.npmjs.com/package/vertx3-eventbus-client) <img src="https://rawgit.com/vert-x3/vertx-awesome/d93d327/vertx-favicon.svg" alt="(stack)" title="Vert.x Stack" height="16px"> - JavaScript event bus client.
* [C++11](https://github.com/julien3/vertxbuspp) - C++11 event bus client.
* [Java](https://github.com/saffron-technology/vertx-eventbusbridge) - Java implementation of vertxbus.js.
* [Java](https://github.com/abdlquadri/vertx-eventbus-java) - Java and Android Event Bus Client.
* [Java](https://github.com/danielstieger/javaxbus) - Simple Java Event Bus Client using plain TCP socket I/O.
* [CLI](https://github.com/cinterloper/vxc) - Command-line binary client for Vert.x event bus - pipe in JSON, emit JSON.
* [Swift](https://github.com/tobias/vertx-swift-eventbus) - Event bus client for [Apple's Swift](https://swift.org) using the [TCP-based protocol](https://github.com/vert-x3/vertx-tcp-eventbus-bridge).
* [Python](https://github.com/jaymine/TCP-eventbus-client-Python) - Event bus client for Python using the [TCP-based protocol](https://github.com/vert-x3/vertx-tcp-eventbus-bridge).
* [C#](https://github.com/jaymine/TCP-eventbus-client-C-Sharp) - Event bus client for C# using the [TCP-based protocol](https://github.com/vert-x3/vertx-tcp-eventbus-bridge).
* [C](https://github.com/jaymine/TCP-eventbus-client-C) - Event bus client for C99 using the [TCP-based protocol](https://github.com/vert-x3/vertx-tcp-eventbus-bridge).
* [Go](https://github.com/jponge/vertx-go-tcp-eventbus-bridge)- Event bus client for Go-lang using the [TCP-based protocol](https://github.com/vert-x3/vertx-tcp-eventbus-bridge).
* [Smalltalk](https://github.com/mumez/VerStix)- Event bus client for [Pharo Smalltalk](http://pharo.org/) using the [TCP-based protocol](https://github.com/vert-x3/vertx-tcp-eventbus-bridge).
* [Java](https://github.com/nielsbaloe/vertxui/tree/master/vertxui-core/src/main/java/live/connector/vertxui/client/transport) - Event bus support in JavaScript through Java code.

## Cluster Managers

*Implementations of the Vert.x cluster manager SPI*

* [JGroups Cluster Manager](https://github.com/vert-x3/vertx-jgroups) - JGroups cluster manager.
* [Atomix Cluster Manager](https://github.com/atomix/atomix-vertx) - An [Atomix](http://atomix.io) based cluster manager implementation for Vert.x 3.
* [Consul Cluster Manager](https://github.com/romalev/vertx-consul-cluster-manager) - Consul cluster manager.

## Cloud Support

* [S3](https://github.com/hubrick/vertx-s3-client) - A fully functional Vert.x client for S3.

## Docker


## Microservices

* [Vert.x GraphQL Service Discovery](https://github.com/engagingspaces/vertx-graphql-service-discovery) - [GraphQL](http://graphql.org/) service discovery and querying for your Vert.x microservices.
* [HTTP Request Multiplexer - Kalfor](https://github.com/derveloper/kalfor) - Combine multiple HTTP GET requests into a single POST. A dead simple alternative to Facebook's [GraphQL](http://graphql.org/) and Netflix's [Falcor](http://netflix.github.io/falcor/).
* [Resilience4j](https://github.com/resilience4j/resilience4j) - Resilience4j is a fault tolerance library designed for Java8 and functional programming. Resilience4j provides modules for Circuit Breaking, Rate Limiting, Bulkheading, Automatic retrying, Response caching and Metric measuring.

## Search Engines

* [Vert.x Elasticsearch Service](https://github.com/englishtown/vertx-elasticsearch-service) - Vert.x 3 [Elasticsearch](https://www.elastic.co/) service with event bus proxying.
* [Vert.x Elasticsearch Service (redesign)](https://github.com/hubrick/vertx-elasticsearch-service) - Vert.x 3 [Elasticsearch](https://www.elastic.co/) service with event bus proxying. Redesign of the [Vert.x Elasticsearch Service](https://github.com/englishtown/vertx-elasticsearch-service). Heavy usage of DTOs over eventbus and no more JsonObjects. Added support for ES plugins.
* [Vert.x Solr Service](https://github.com/englishtown/vertx-solr-service) - Vert.x 3 Solr service with event bus proxying.

## Service Factory

* [Node.js Service Factory](https://github.com/mellster2012/vertx-nodejs-service-factory) - Vert.x Node.js Service Factory.
* [Eclipse SISU Service Factories](https://github.com/cstamas/vertx-sisu) - Vert.x integration with [Eclipse SISU](https://www.eclipse.org/sisu/) DI container offering alternatives for `vertx-service-factory` and `vertx-maven-service-factory`.

## Config

* [Vert.x Config AWS SSM Store](https://github.com/Finovertech/vertx-config-aws-ssm) - A [config store](http://vertx.io/docs/vertx-config/java/) implementation for retrieving configuration values from the [AWS EC2 SSM Parameter Store](https://aws.amazon.com/ec2/systems-manager/parameter-store/).
* [Vert.x Boot](https://github.com/jponge/vertx-boot) - Deploying verticles from a HOCON configuration.

## Dependency Injection

* [Vert.x Guice](https://github.com/englishtown/vertx-guice) - Vert.x verticle factory for Guice dependency injection.
* [Vert.x HK2](https://github.com/englishtown/vertx-hk2) - Vert.x verticle factory for HK2 dependency injection.
* [Spring Vert.x Extension](https://github.com/amoAHCP/spring-vertx-ext) - Vert.x verticle factory for Spring DI injection.
* [Vert.x Beans](https://github.com/rworsnop/vertx-beans) - Inject Vert.x objects as beans into your Spring application.
* [QBit](https://github.com/advantageous/qbit) - QBit works with Spring DI and Spring Boot (and of course Vert.x). Allows you to use QBit, Vert.x, Spring DI and Spring Boot in the same application.
* [Vert.x Eclipse SISU](https://github.com/cstamas/vertx-sisu) - Vert.x integration with [Eclipse SISU](https://www.eclipse.org/sisu/) DI container.
* [Vert.x Spring Verticle Factory](https://github.com/juanavelez/vertx-spring-verticle-factory) - A Vert.x Verticle Factory that makes use of Spring to obtain and configure Verticles.

## Testing


## Development Tools

* [Vert.x health check](https://github.com/vert-x3/vertx-health-check) - Allows for remote health checking in Vert.x projects.
* [Vert.x Hot](https://github.com/dazraf/vertx-hot) - A Maven plugin for the hot-deploy of Maven Vert.x projects.
* [slush-vertx](https://www.npmjs.com/package/slush-vertx) - A template driven Vert.x project generator for different languages and build tools.
* [Vert.x for Visual Studio Code](https://github.com/pmlopes/VertxSnippet) - A Visual Studio Code (polyglot) plugin for Vert.x. Also available from the [Marketplace](https://marketplace.visualstudio.com/items?itemName=pmlopes.vertxsnippet).
* [Vert.x Starter](http://www.jetdrone.xyz/vertx-starter/) - A browser-based project starter and project templates for Vert.x applications.
* [Vert.x LiveReload](https://github.com/ybonnel/vertx-livereload) - A simple livereload server for Vert.x applications.

## Miscellaneous

* [Vert.x Child Process](https://github.com/vietj/vertx-childprocess) - Spawn child process from Vert.x.
* [vertx-redisques](https://github.com/swisspush/vertx-redisques) - A highly scalable redis-persistent queuing system for Vert.x.
* [Simple File Server](https://github.com/pitchpoint-solutions/sfs) - An OpenStack Swift compatible distributed object storage server that can serve and securely store billions of large and small files using minimal resources implemented using Vert.x.
* [Vert.x Boot](https://github.com/jponge/vertx-boot) - Deploying verticles from a HOCON configuration.
* [GDH](https://github.com/maxamel/GDH) - Generalized Diffie-Hellman key exchange Java library built on top of Vert.x.

## Distribution


## Examples

* [Vert.x feeds](https://github.com/aesteve/vertx-feeds) - Example of an RSS aggregator built using Vert.x, Gradle, MongoDB, Redis, Handlebars templates, AngularJS, the event bus and SockJS.
* [Vert.x Markdown service](https://github.com/aesteve/vertx-markdown-service) - Example on how to use [service-proxy](https://github.com/vert-x3/vertx-service-proxy) with Gradle.
* [Example using event bus and service proxies to connect vertx and node](https://github.com/advantageous/vertx-node-ec2-eventbus-example) - Step by step example with wiki description showing how to connect Vert.x and Node using event bus and service proxies.
* [Vert.x Todo-Backend implementation](https://github.com/aesteve/todo-backend-vertx) - Pure Java 8 implementation of the Todo MVC backend. Uses a Vert.x LocalMap for storage.
* [Kotlin Todo-Backend implementation](https://github.com/aesteve/vertx-kotlin-todomvc) - Kotlin implementation of the Todo MVC backend.
* [Scala Todo-Backend implementation](https://github.com/aesteve/vertx-scala-todomvc) - Scala implementation of the Todo MVC backend.
* [Grooveex Todo-Backend implementation](https://github.com/aesteve/todo-backend-grooveex) - Todo MVC backend implementation with Vert.x + Groovy + some syntactic sugar + DSL routing facilities.
* [Vert.x Gradle Starter](https://github.com/yyunikov/vertx-gradle-starter) - Java 8 starter application with example of using Vert.x with Gradle build system, profiles configuration and SLF4J.
* [Vert.x Gentics Mesh Example](https://github.com/gentics/mesh-vertx-example) - Example on how to build a template-based web server with Gentics Mesh and handlebars.
* [HTTP/2 showcase](https://github.com/aesteve/http2-showcase) - A simple demo, showing how HTTP/2 can drastically improve user experience when a huge latency is involved.
* [Vert.x Music Store](https://github.com/tsegismont/vertx-musicstore) - An example application on how to build Vert.x applications with RxJava.
* [Crabzilla](https://github.com/crabzilla/crabzilla) - Yet another Event Sourcing experiment. A project exploring Vert.x to develop Event Sourcing / CQRS applications.
* [Vert.x PostgreSQL Starter](https://github.com/BillyYccc/vertx-postgresql-starter) - A starter to build a monolithic CRUD RESTful Web Service with Vert.x stack and PostgreSQL.
* [Cloud Foundry](https://github.com/amdelamar/vertx-cloudfoundry) - An example Vert.x for deploying to a [Cloud Foundry](https://www.cloudfoundry.org/) service provider.
* [Knative](https://github.com/knative/docs/tree/master/serving/samples/helloworld-vertx) - An example application on how to use [Reactive Extensions Vert.x](https://github.com/vert-x3/vertx-rx) with [Knative](https://github.com/knative).
## Deployment

* [Vert.x Deploy Application](https://github.com/msoute/vertx-deploy-tools) - (Seamless) deploy to AWS based Vert.x application clusters.

## Utilities

* [Chime](https://github.com/LisiLisenok/Chime) - Time scheduler working on Vert.x event bus allowing for scheduling with _cron-style_ and _interval_ timers.
* [Vert.x Cron](https://github.com/diabolicallabs/vertx-cron) - Schedule events with cron specifications. Has event bus and Observable versions.
* [Vert.x POJO config](https://github.com/aesteve/vertx-pojo-config) - Allows for mapping between standard JSON configuration and a (type-safe) configuration Java bean. Also allows the configuration bean to be validated through JSR 303.
* [Vert.x Async](https://github.com/gchauvet/vertx-async) - Portage of caolan/async nodejs module to Vert.x framework that provides helpers methods for common async patterns.
* [Vert.x JOLT](https://github.com/lusoalex/vertx-jolt) - JSON to JSON transformation tool based on the original bazaarvoice JOLT project. Helpful to transform different json structure into an expected json format.
* [Vert.x Dependent Verticle Deployer](https://github.com/juanavelez/vertx-dependent-verticle-deployer) - A Vert.x Verticle intended to deploy verticles and their dependent verticles.
* [Vert.x Dataloader](https://github.com/engagingspaces/vertx-dataloader) - Java port of Facebook Dataloader for Vert.x. Efficient batching and caching for your data layer.
* [Vert.x Util](https://github.com/juanavelez/vertx-util) - A collection of Vert.x utility methods.
* [Vert.x Web Accesslog](https://github.com/romanpierson/vertx-web-accesslog) - Just a simple handler to be used in Vert.x Web to generate access logs.
* [Vert.x GraphQL Utils](http://github.com/tibor-kocsis/vertx-graphql-utils) - A route handler and Vert.x compatible interfaces to handle GraphQL queries in Vert.x and Vert.x Web.
* [Nannoq-Tools](https://noriginmedia.github.io/nannoq-tools/) - Nannoq-Tools is a toolkit for constructing robust, scalable and distributed applications leveraging Vert.x including modules for authentication, cluster management, Firebase Cloud Messaging, DynamoDB, fully generic queries, REST, and more.

## Community

- [User Group](https://groups.google.com/forum/?fromgroups#!forum/vertx) - Discuss all user issues related to *using* Vert.x.
- [Developer Group](https://groups.google.com/forum/?fromgroups#!forum/vertx-dev) - A group for Vert.x core *developers* and *contributors*.
- [Gitter chat](https://gitter.im/eclipse-vertx/vertx-users) general chat for Vert.x releated chat.
- [Issues](https://github.com/vert-x3/issues/issues) - Vert.x core issue tracker.
- [Wiki](https://github.com/vert-x3/wiki/wiki) - Contains useful information about Vert.x.
- [Learning Materials](http://vertx.io/materials/) - A list of articles and presentations on Vert.x.
- [Blog](http://vertx.io/blog/) - The official Vert.x blog containing many tutorials and other information.
- [2017 Events](https://github.com/vert-x3/wiki/wiki/Vert.x-2017-Events) - A list of 2017 Vert.x talks and presentations.

## Social events / Meetups

- [Amsterdam/The Netherlands](https://www.meetup.com/Vert-x-NL)
- [Paris](https://www.meetup.com/Paris-vert-x-Meetup/)

## Front-End

* [VertxUI](https://github.com/nielsbaloe/vertxui) - A pure Java front-end toolkit with descriptive fluent views-on-models, POJO traffic, JUnit testing on the virtual DOM or mixed-language on a real DOM, and more.

## Contribute

Contributions welcome! Read the [contribution guidelines](https://github.com/vert-x3/vertx-awesome/blob/master/CONTRIBUTING.md) first.