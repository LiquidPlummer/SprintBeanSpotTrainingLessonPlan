# Kyle's Spring Bean Spot Training Lesson Plan That's Really Good and That Will Help Everyone Learn to Embrace The Bean

## Overview
Today I'll be talking a bit about Spring Beans, their lifecycle, and a bit about how and why they are used. 

What is a bean? A bean is an object that is instantiated and managed by the Spring IoC container. The purpose of beans is Dependency Injection, to achieve loose coupling.

What is Inversion of Control? This is a programming technique that reverses the idea of control. Instead of your program running the show and making all the desicions about execution, you hand off control to some other entity or entities. In our case we are talking about managing dependencies, we give control to a Spring IoC container to do dependency injection. In this way we achieve loose coupling.

So, what is loose coupling? This is an approach where components depend on eachother to the least extent possible. For us today, that means any dependent objects are instantiated elsewhere and provided to our object via constructors. These objects are our beans, and thay are instantiated by the IoC container. They are provided via dependency injection.

So now, to wrap this all together: Dependency injection of beans to achieve lose coupling in an effort to invert control. Why is all this necessary? To abstract away as much of the implementation details as possible. Spring is a giant framework and there are a lot of things going on, and a lot to learn about. But, without these techniques it would be significantly more difficult, and it would be far more difficult to deal with changes. These techniques are widely used throughout the Spring framework, and allow us to utilize an enormous number of features that can be changed and updated without troubling us. Spring offers modules that handle web service, data persistence, logging, security, basically anything that has wide use in enterprise java applications.

Take web service for example. With just a few set up steps you can get a simple restful API up and running with Spring, by giving control of handling everything to spring. You configure settings like path and port, but you otherwise don't care about implementation. You don't have to instantiate objects and dependencies, spin up a thread pool, listen for incoming connections, establish sockets, and all that. You let Spring do all this for you, you hand control off to spring. The spring hands control back once a request is ready, you handle it, and hand control back to spring. 

- [Bean containers](https://github.com/LiquidPlummer/SprintBeanSpotTrainingLessonPlan/blob/main/overview-containers.md)
  - BeanFactory
    - Applicationcontext
      - specific ApplicationContexts
- [IoC and Dependency Injection](https://github.com/LiquidPlummer/SprintBeanSpotTrainingLessonPlan/blob/main/overview-ioc-injection.md)
- [Scopes](https://github.com/LiquidPlummer/SprintBeanSpotTrainingLessonPlan/blob/main/overview-scopes.md)
  - Singleton*
  - Prototype
  - Request**
  - Session**
  - Global Session**
  - Application**
- [Lifecycle](https://github.com/LiquidPlummer/SprintBeanSpotTrainingLessonPlan/blob/main/overview-bean-lifecycle.md)
- [@Bean Stereotypes](https://github.com/LiquidPlummer/SprintBeanSpotTrainingLessonPlan/blob/main/overview-stereotypes.md)
  - @Component
  - @Repository
  - @Service
  - @Controller
  
  
\* Default scope  
\** Only valid with web-aware ApplicationContext  
 
 
## Links

- Intro to Spring
- [Bean lifecycle](https://gitlab.com/revature_training/spring-team/-/blob/master/modules/framework/bean-lifecycle.md)
- [Scopes of a bean](https://gitlab.com/revature_training/spring-team/-/blob/master/modules/framework/bean-scopes.md)
- [Spring IOC Container & Dependency Injection](https://gitlab.com/revature_training/spring-team/-/blob/master/modules/framework/spring-ioc-container-and-dependency-injection.md)
- [Bean Factory vs Application Context](https://github.com/LiquidPlummer/SprintBeanSpotTrainingLessonPlan/blob/main/BeanFactoryApplicationContext.md)
- Injecting primitives (XML)
- Injecting objects (XML and Java Class)
- XML vs Annotation-based configuration
- Annotations
- [Stereotypes](https://gitlab.com/revature_training/spring-team/-/blob/master/modules/framework/stereotypes.md)
