---
layout: post
title: Devoxx PL 18 - State or events?
---

## State or events? Which shall I keep? - Jakub Pilimon

* This talk was mostly based on the blog entry [Event Storming and Spring with a Splash of DDD (https://spring.io/blog/2018/04/11/event-storming-and-spring-with-a-splash-of-ddd)
 
### Talk overview
* Event Storming
* Event Architecture
* Lightweight implementation

### Event Storming
* All we need is unlimited space on a wide wall, sticky notes and both business and technical people gathered in one room
* Can derive your public API / micro-services / modules

Why Events? 
* Loose coupling
* ORM’s can introduce accidental complexity into our applications. E.g. loading a list of child objects when we only need to check number of objects (we are just calling .size() on the list)
* OOP is a bad name – Message Oriented Programming better name
 
### Demo
Used spock & TDD

```java
Def
Given
When (and)
Then
```

The old way
this.limit = ?
At this point there are no orange notes in the code
Create an event object
ID (ccuuid)
Timestamp
“amount”
Contract is still the same
Use map for db
API.match
Save == easy
Load == tricky
 
Considerations
Backwards Compatibility
Learning curve
Different perspectives
 
Event Architecture
Channels
RabbitMQ
EJP
 
