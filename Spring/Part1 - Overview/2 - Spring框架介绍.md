Spring框架是一个基于Java平台的框架，为开发Java应用提供了全面的基础架构支持。在Spring的帮助下，你可以更加关注于你的应用本身。

Spring使你可以基于"plain old java objects"来构建应用，并且在其上非侵入地使用企业服务。这种能力可以使用在Java SE模型上，也可以部分或全部地使用在Java EE模型上。

作为一个开发者，下面是一些你能从Spring框架中获得的优势:

*   让一个Java方法无需处理事务API就能在数据库事务环境下执行
*   让一个本地Java方法无需处理远程API就能成为一个远程方法
*   让一个本地Java方法无需处理JMX API就能成为(**Management Operation**)
*   让一个本地Java方法无需处理JMS API就能成为(**Message Handler**)

### 依赖注入与控制反转

#### 背景

"问题是，他们反转了哪方面的控制"，Martin Fowler于2014年在其网站上针对控制反转提出了这个问题。Fowler建议将控制反转这个理念换个名字来让其更加具有自解释性，于是**依赖注入**这个概念诞生了。

想进一步了解控制反转和依赖注入，可以参考下Fowler的这篇文章[http://martinfowler.com/articles/injection.html](http://martinfowler.com/articles/injection.html)

Java应用可以指代简单的Applet，也可以指代n层结构的服务端企业级应用，不过简单来说，他们都是由各种各样的对象通过合作来组成最终的应用，也就是说应用中的对象通常依赖于其他对象。

虽然Java平台提供了很多应用开发时需要的功能，但它却缺乏一种可以组织各个基本构建块(building block)的方式，而是由架构师和开发人员自行管理。是的，你会想到在应用中使用设计模式来组织各种各样的类和对象实例，比如工厂模式、抽象工厂模式、构建者模式、装饰者模式和服务定位模式。但是，设计模式只描述了：模式名字，做了什么，什么时候应用，解决了什么问题等等，它们只是一个十分形式化的最佳实践描述，作为开发人员你还是得自己在应用中实现它们。

Spring框架的控制反转组件解决了这个问题，它提供了一种形式化的方式来组织各个分散的组件，并将其组装成一个可以立即投入使用的应用。Spring框架将设计模式看成一等对象，并让其可以集成在你的应用中。现在有很多组织和机构通过这种方式使用Spring框架来开发强壮，可维护的应用。

### 模块

Spring框架的特征大概是由20个模块组织起来的。这些模块又聚集在Core Container，Data Access/Integration，Web，AOP，Instrumentation，Messaging和Test这些组中。下面这张图描述了Spring框架中的模块组织形式。

![Module Structure](https://raw.githubusercontent.com/zhouhaibing089/translation/master/Spring/Part1%20-%20Overview/module-structure.png)

接下来几小节列出了每个特征下可用的模块，以及他们的制品名称(对于依赖管理工具有用)

**核心容器(Core Container)**

由*spring-beans*，*spring-context*，*spring-expression*这几个模块组成。

spring-core和spring-beans模块是整个框架中最基本的部分，包括控制反转和依赖注入两个重要的功能，`BeanFactory`是工厂模式的一个精细实现，它可以让你不必使用单例模式，并且实现了将依赖对象的配置和规格进行分离。

spring-context模块基于core和beans模块建立，它为对象的访问提供了框架式的访问方式，就像JNDI那样。context模块继承了beans模块中的功能，并添加了国际化支持(比如说，资源包)，事件传播，资源加载和context的透明化创建(比如说在Servlet环境中)。context模块还支持Java EE的种种特征，比如EJB，JMX和基本的远程。`ApplicationContext`是context模块中的关键接口。
