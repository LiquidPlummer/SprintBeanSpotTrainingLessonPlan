# Bean Lifecycle
- Instantiation
  - Beans are first instantiated.
  - Their properties are set.
- Awareness 
  - Any associated interfaces or objects are made aware of their existence.
  - The bean is made aware of any associated interfaces as well.
  - [BeanNameAware.setBeanName()](https://docs.spring.io/spring-framework/docs/current/javadoc-api/org/springframework/beans/factory/BeanNameAware.html)
  - [BeanFactoryAware.setBeanFactory()](https://docs.spring.io/spring-framework/docs/current/javadoc-api/org/springframework/beans/factory/BeanFactoryAware.html)
- Initialization
  - Any other methods, particularly custom created methods, are invoked.
    - [InitializingBean.afterPropertiesSet()](https://docs.spring.io/spring-framework/docs/current/javadoc-api/org/springframework/beans/factory/InitializingBean.html#afterPropertiesSet--)
- Service
  - Then the bean is ready for use.
- Destruction
  - Once the bean is no longer used, it is marked for removal and a destroy method is invoked for the bean
  - Custom destroy methods are invoked, if any.
    - [DisposableBean.destroy()](https://docs.spring.io/spring-framework/docs/current/javadoc-api/org/springframework/beans/factory/DisposableBean.html#destroy--)
  - Bean is the destroyed.



<br><br>
See also: 
- [Awareness](https://www.baeldung.com/spring-bean-name-factory-aware)  
- [Bean Lifecycle](https://gitlab.com/revature_training/spring-team/-/blob/master/modules/framework/bean-lifecycle.md)
