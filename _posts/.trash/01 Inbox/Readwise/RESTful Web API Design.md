---
title: RESTful Web API Design
author: martinekuan
cover: https://learn.microsoft.com/en-us/media/logos/logo-ms-social.png
dateRead: 
status: 
tag: 
type:articles
---
![rw-book-cover](https://learn.microsoft.com/en-us/media/logos/logo-ms-social.png)

## Metadata
- Author: [[martinekuan]]
- Full Title: RESTful Web API Design
- Category: #articles
- URL: https://learn.microsoft.com/en-us/azure/architecture/best-practices/api-design

## Highlights
- REST is independent of any underlying protocol and is not necessarily tied to HTTP. However, most common REST API implementations use HTTP as the application protocol, and this guide focuses on designing REST APIs for HTTP. ([View Highlight](https://read.readwise.io/read/01gp3dcpz1st2sbpyqvejaat5f))
- A primary advantage of REST over HTTP is that it uses open standards, and does not bind the implementation of the API or the client applications to any specific implementation. ([View Highlight](https://read.readwise.io/read/01gp3dd8e5ttvwcmtybnf2st9j))
- Here are some of the main design principles of RESTful APIs using HTTP:
  • REST APIs are designed around *resources*, which are any kind of object, data, or service that can be accessed by the client.
  • A resource has an *identifier*, which is a URI that uniquely identifies that resource. For example, the URI for a particular customer order might be:
  • Clients interact with a service by exchanging *representations* of resources. Many web APIs use JSON as the exchange format. For example, a GET request to the URI listed above might return this response body:
  • REST APIs use a uniform interface, which helps to decouple the client and service implementations. For REST APIs built on HTTP, the uniform interface includes using standard HTTP verbs to perform operations on resources. The most common operations are GET, POST, PUT, PATCH, and DELETE.
  • REST APIs use a stateless request model. HTTP requests should be independent and may occur in any order, so keeping transient state information between requests is not feasible. The only place where information is stored is in the resources themselves, and each request should be an atomic operation. This constraint enables web services to be highly scalable, because there is no need to retain any affinity between clients and specific servers. Any server can handle any request from any client. That said, other factors can limit scalability. For example, many web services write to a backend data store, which may be hard to scale out. For more information about strategies to scale out a data store, see [Horizontal, vertical, and functional data partitioning](https://learn.microsoft.com/en-us/azure/architecture/best-practices/data-partitioning).
  • REST APIs are driven by hypermedia links that are contained in the representation. For example, the following shows a JSON representation of an order. It contains links to get or update the customer associated with the order.
  {
  "orderID":3,
  "productID":2,
  "quantity":4,
  "orderValue":16.60,
  "links": [
  {"rel":"product","href":"https://adventure-works.com/customers/3", "action":"GET" },
  {"rel":"product","href":"https://adventure-works.com/customers/3", "action":"PUT" }
  ]
  } ([View Highlight](https://read.readwise.io/read/01gp3ddzv14m6r48ky87sytndq))
    - Note: RESTful APIs using HTTP are designed with a few main principles. Resources are objects, data, or services that can be accessed by a client. Each resource has a special name called an identifier that helps it be found. Clients communicate with services by exchanging information about the resources. RESTful APIs use a special type of interface that helps the client and service work together. This interface includes using standard HTTP verbs to do things with the resources. REST APIs also use something called a stateless request model which means that each request is an atomic operation and the only place information is stored is in the resources themselves. Furthermore, REST APIs use hypermedia links which are like special roads that help people get to the resources.
- In 2008, Leonard Richardson proposed the following [maturity model](https://martinfowler.com/articles/richardsonMaturityModel.html) for web APIs:
  • Level 0: Define one URI, and all operations are POST requests to this URI.
  • Level 1: Create separate URIs for individual resources.
  • Level 2: Use HTTP methods to define operations on resources.
  • Level 3: Use hypermedia (HATEOAS, described below). ([View Highlight](https://read.readwise.io/read/01gp3dq3e1nan3zangv2fvbr8y))
- Focus on the business entities that the web API exposes. For example, in an e-commerce system, the primary entities might be customers and orders ([View Highlight](https://read.readwise.io/read/01gp3dqnpsyhv9kczxgfjgpj4h))
