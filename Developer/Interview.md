## Interview Questions and Answers
> 开发人员面试题集锦

### Laravel

##### 什么是 HTTP 中间件？
> HTTP 中间件是一种用于过滤 HTTP 请求的技术。Laravel 包含一个中间件，用于检查应用程序用户是否已通过身份验证。


##### ORM 代表什么？
> ORM 代表对象关系映射，把数据库相关字段映射到对应的模型对象里面，相当于有多个一个抽象层。后面直接操作对象


##### 什么是数据迁移为什么迁移很重要？
> 迁移非常重要是因为它允许您通过维护数据库一致性来共享应用程序。
> 如果不进行迁移，则很难共享任何 Laravel 应用程序。
> 它还允许您同步数据库。


##### 如何在 Laravel 模型中自定义表名？
> 自定义表名，您可以重写 protected 变量 $table 的值。

------

### Spring

##### Spring由哪些模块组成?
> 以下是Spring 框架的基本模块：
> 
> Core module
> Bean module
> Context module
> Expression Language module
> JDBC module
> ORM module
> OXM module
> Java Messaging Service(JMS) module
> Transaction module
> Web module
> Web-Servlet module
> Web-Struts module
> Web-Portlet module

##### 什么是Spring IOC 容器？
> Spring IOC 负责创建对象，管理对象（通过依赖注入（DI），装配对象，配置对象，并且管理这些对象的整个生命周期。
> IOC 或 依赖注入把应用的代码量降到最低。它使应用容易测试，单元测试不再需要单例和JNDI查找机制。最小的代价和最小的侵入性使松散耦合得以实现。IOC容器支持加载服务时的饿汉式初始化和懒加载。


##### 什么是Spring的依赖注入？
> 依赖注入，是IOC的一个方面，是个通常的概念，它有多种解释。这概念是说你不用创建对象，而只需要描述它如何被创建。你不在代码里直接组装你的组件和服务，但是要在配置文件里描述哪些组件需要哪些服务，之后一个容器（IOC容器）负责把他们组装起来。

##### 有哪些不同类型的IOC（依赖注入）方式？
> 构造器依赖注入：构造器依赖注入通过容器触发一个类的构造器来实现的，该类有一系列参数，每个参数代表一个对其他类的依赖。
> Setter方法注入：Setter方法注入是容器通过调用无参构造器或无参static工厂 方法实例化bean之后，调用该bean的setter方法，即实现了基于setter的依赖注入。

##### 哪种依赖注入方式你建议使用，构造器注入，还是 Setter方法注入？
> 你两种依赖方式都可以使用，构造器注入和Setter方法注入。最好的解决方案是用构造器参数实现强制依赖，setter方法实现可选依赖。

##### 解释Spring框架中bean的生命周期。
> Spring容器 从XML 文件中读取bean的定义，并实例化bean。
> Spring根据bean的定义填充所有的属性。
> 如果bean实现了BeanNameAware 接口，Spring 传递bean 的ID 到 setBeanName方法。
> 如果Bean 实现了 BeanFactoryAware 接口， Spring传递beanfactory 给setBeanFactory 方法。
> 如果有任何与bean相关联的BeanPostProcessors，Spring会在postProcesserBeforeInitialization()方法内调用它们。
> 如果bean实现IntializingBean了，调用它的afterPropertySet方法，如果bean声明了初始化方法，调用此初始化方法。
> 如果有BeanPostProcessors 和bean 关联，这些bean的postProcessAfterInitialization() 方法将被调用。
> 如果bean实现了 DisposableBean，它将调用destroy()方法。

##### Spring框架的事务管理有哪些优点？
> 它为不同的事务API  如 JTA，JDBC，Hibernate，JPA 和JDO，提供一个不变的编程模式。
> 它为编程式事务管理提供了一套简单的API而不是一些复杂的事务API如
> 它支持声明式事务管理。
> 它和Spring各种数据访问抽象层很好得集成。