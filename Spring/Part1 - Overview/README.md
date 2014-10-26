Spring框架为构建企业级应用提供了一个轻量的、一站式的解决方案。另外一方面，Spring也是模块化的，它可以让你只使用你依赖的那些部分，比如说你可以使用Spring提供的IoC容器，并在其上使用任何web框架，你也可以只使用Hibernate的集成代码或者只使用JDBC的抽象层。Spring框架支持声明式的事务管理，支持通过RMI或者Web Services来远程访问你的逻辑代码，支持多样的数据持久化方式。Spring还提供了完整的MVC框架和AOP的透明化集成。

Spring被设计成非侵入式的，这意味着你的领域逻辑代码通常并不依赖Spring框架本身。不过就算有依赖(比如在数据访问层，你会依赖于Spring框架提供的一些类)，你也可以轻松地将这些代码与你的其他代码隔离开来。

本文档是针对Spring框架的参考指南，如果你有任何需求，评论或者疑问，请在用户邮件列表里发布. 针对框架本身的疑问，你可以在StackOverflow上寻求帮助.