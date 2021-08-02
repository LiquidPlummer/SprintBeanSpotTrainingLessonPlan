# Spring Bean Scope
By default, spring beans are Singleton Scope and are created eagerly. Eager means the beans are instantiated as soon as the container starts up. If you wanted to change these behaviors you would use the @Scope and @Lazy annotations.

### @Scope
Use this annotation when describing a bean to change it's scope to something other than singleton. This annotation takes as a parameter a string of the desired scope. 

### @Lazy
Use this annotation to stop the IoC container from creating singleton beans at startup, and instead only create it when it is requested. This is similar to how Java loads classes. When autowiring it is necessary to also use @Lazy with @Autowired to get lazy behavior. Non-singleton scoped beans behave like a lazy singleton, they are created when requested.

## Scopes

- Singleton Scope (default) - One instance of this bean is created, when the bean is requested a reference to the singleton is returned.
- Prototype Scope - Each time the bean is requested, a new instance is created and referenced.
- Request Scope* - For each HTTP request a new instance of the bean is created and referenced. This bean is associated with the request and is discarded when the request is - completed.
- Session Scope* - For each HTTP session a new instance of the bean is created and referenced. This bean is associated with the session and is discarded when the session is completed.
- Gloabl Session Scope* - A single bean instance is scoped to the lifecycle of a global HTTP session. Generally only valid when used in a portlet context.
- Application Scope* - Scopes a single bean definition to the lifecycle of a ServletContext.

\* Only valid with a web-aware ApplicationContext.
  
<br><br>
See also: [Bean Scopes](https://gitlab.com/revature_training/spring-team/-/blob/master/modules/framework/bean-scopes.md)
