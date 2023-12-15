# corrtan_SpringBootDemo

Quick demo to understand Spring Framework 


- How it works: Core contains - factory of creating beans, manage bean dependencies.
- Main website: https://spring.io/ 
    
- Goals of Spring: lightweight version of Java POJOs - Plain-Old-Java-Objects; dependency injection to promote loose coupling, minimize boilerplate java code

- AOP (aspect oriented programming - logging, security, transactions, etc.)
- Data Access Layer: JDBC helper class (reduce source code > 50%), ORM (object to relational modling, Hibernate/JPA integration), JMS(Java Message Service, sending async msg to message broker), transactions(makes heavy use of AOP)
- Test layer: unit/itegration/mock
- Web Layer: Servlet, WebSocket, Web

- Quickly create a starter Spring Boot project: https://start.spring.io/
- Can be run standalone (includes embedded server i.e. Tomcat):

```bash
java -jar mycoolapp.jar
```

![sb_qa.png](https://github.com/CorrineTan/corrtan_SpringBootDemo/blob/main/sb_qa.png)

- Maven: solve the dependencies issue (Spring, Hibernate, JSON), you dont need to download Jar files and manually put into your project folder. Maven will make these available during compile/run → shopping list, personal shopper.
- spring boot parents for starter - inherit from parent version of spring boot
- spring boot dev tools : added to pom.xml ⇒ auto restart your application when code is updated
- spring boot actuator: expose endpoint to monitor and manager your application. (Free Rest Endpoint!!)

add following to application.properties:

```bash
management.endpoints.web.exposure.include=health,info
management.info.env.enabled=true
```

- Full list of Actuator endpoints: https://docs.spring.io/spring-boot/docs/current/reference/htmlsingle/#actuator.endpoints
Then go to http://localhost:8080/actuator/info and [http://localhost:8080/actuator/](http://localhost:8080/actuator/info)health

![sb_actuator.png](https://github.com/CorrineTan/corrtan_SpringBootDemo/blob/main/sb_actuator.png)

- All spring boot properties (to add to application.properties): https://docs.spring.io/spring-boot/docs/current/reference/html/application-properties.html#appendix.application-properties
