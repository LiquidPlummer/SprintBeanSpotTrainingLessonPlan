# Bean Lifecycle
1. Beans are first instantiated.
1. Their properties are set.
1. Any associated interfaces or objects are made aware of their existence.
1. The bean is made aware of any associated interfaces as well.
1. Any other methods, particularly custom created methods, are invoked.
1. Then the bean is ready for use.
1. Once the bean is no longer used, it is marked for removal and a destroy method is invoked for the bean
1. Custom destroy methods are invoked, if any.
1. Bean is the destroyed.

<br><br>
See also: 
- [Awareness](https://www.baeldung.com/spring-bean-name-factory-aware)  
- [Bean Lifecycle](https://gitlab.com/revature_training/spring-team/-/blob/master/modules/framework/bean-lifecycle.md)
