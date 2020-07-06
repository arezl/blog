SpringInAction

# 内容提要

本书是经典的、畅销的Spring学习和实践指南。
第4版针对Spring4进行了全面更新。全书分为4部分。第l部分介绍Spring框架的核心知识。第2部分在此基础上介绍了如何使用Spring构建Web应用程序。第3部分告别前端，介绍了如何在应用程序的后端使用Spring。第4部分描述了如何使用Spring与其他的应用和服务进行集成。
本书适用于已具有一定Java编程基础的读者，以及在Java平台下进行各类软件开发的开发人员、测试人员，尤其适用于企业级Java开发人员。本书既可以被刚开始学习Spring的读者当作学习指南，也可以被那些想深入了解Spring某方面功能的资深用户作为参考用书。

# 关于本书

Spring框架是以简化JavaEE应用程序的开发为目标而创建的。同样，本书是为了帮助读者更容易地使用Spring而编写的。我的目标不是为读者详细地列出Spring API，而是希望通过现实中的实际示例代码来为JavaEE开发人员展现Spring框架。因为Spring是一个模块化的框架，所以这本书也是按照这种方式编写的。我们知道并不是所有的开发人员都有相同的需求，有些人想从头学习Spring，而有的可能只想排出几个主题，然后按照自己的节奏来学习。所以，本书既可以被刚开始学习Spring的读者当作学习指南，也可以被那些想深入了解某方面功能的读者作为参考。
本书适用于所有的Java开发人员，企业级Java开发人员将会发现更有帮助。我将会循序渐进地指导读者浏览本书中每章复杂的示例代码，但Spring的真正强大之处在于它能够使企业级应用程序的开发更简单。因此，企业级应用程序的开发人员会更加欣赏本书的示例代码。因为Spring的绝大部分内容都是提供企业级服务的，所以这里包含了许多Spring和EJB的比较。
路线图
本书分为4部分。第1部分介绍Spring框架的核心知识。第2部分在此基础上介绍如何使用Spring构建Web应用程序。第3部分告别前端，介绍如何在应用程序的后端使用Spring。第4部分描述如何使用Spring与其他的应用和服务进行集成。
在第1部分中，读者将会学习到Spring容器、依赖注入（dependency injection，DI）和面向切面编程（aspect-oriented programming，AOP），也就是Spring框架的核心。
这能让读者很好地理解Spring的基础原理，而这些原理将会在本书各个章节都会用到。
■第1章将会概要地介绍Spring，包括DI和AOP的一些基本样例。同时，读者还会了解到更大的Spring生态系统的整体情况。
■第2章更为详细地介绍DI，展现应用程序中的各个组件（bean）如何装配在一起。这包括基于XML装配、基于Java装配以及自动装配。

■在掌握了基本的bean装配后，第3章会介绍几种高级装配技术，读者可能并不会经常用到这些技术，但是如果用到的话，本章的内容将会告诉读者如何发挥Spring容器最强大的威力。
■第4章介绍如何使用Spring的AOP来为对象解耦那些对其提供服务的横切性关注点。这一章也为后面各章提供基础，在后面读者将会使用AOP来提供声明式服务，如事务、安全和缓存。
在第2部分中，读者将会看到如何使用Spring来构建Web应用程序。
■第5章介绍使用Spring MVC的基础知识，这是Spring中的基础Web框架。读者将会看到如何编写控制器来处理请求，并使用模型数据产生响应。
■当控制器的工作完成后，模型数据必须要使用一个视图来进行渲染。第6章将会探讨在Spring中可以使用的各种视图技术，包括JSP、Apache Tiles 以及Thymeleaf。
■第7章的内容不再是Spring MVC的基础知识了，在本章中，读者将会学习到如何自定义Spring MVC配置、处理multipart类型的文件上传、处理在控制器中可能会出现的异常并且会通过flash属性在请求之间传递数据。
■第8章将会介绍Spring Web Flow，这是Spring MVC的一个扩展，能够开发会话式的Web应用程序。在本章中，读者将会学习到如何构建引导用户完成特定流程的Web应用程序。
■第9章读者将会学到如何使用Spring Security为自己的应用程序Web层实现安全性。
第3部分所关注的内容不再是应用程序的前端了，而是关注于如何处理和持久化数据。

■第10章首先会介绍如何使用Spring对JDBC的抽象实现关系型数据库中的数据持久化。
■第11章从另外一个角度介绍数据持久化，也就是使用Java持久化API（JPA）存储关系型数据库中的数据。
■第12章将会介绍如何将Spring与非关系型数据库结合使用，如MongoDB和Neotj。
■不管数据存储在什么地方，缓存都有助于性能的提升，这是通过只有在必要的时候才去查询数据库实现的。第13章将会为读者介绍Spring对声明式缓存的支持。
第14章重新回到Spring Security，将会介绍如何通过AOP将安全性应用到方法级别。
本书的最后一部分会介绍如何将Spring应用程序与其他系统进行集成。
■第15章将会学习如何创建与使用远程服务，包括RMl、Hessian、Burlap以及基于SOAP的服务。

 ■第16章将会再次回到Spring MVC，我们将会看到如何创建RESTful服务，在这个过程中所使用的编程模型与之前在第5章中所描述的是一致的。
■第17章将会探讨Spring对异步消息的支持，本章将会包括Java消息服务（Java Message Service，JMS）以及高级消息队列协议（Advanced Mesage Queuing Protocol，AMQP）。
■在第18章中，异步消息有了新的花样，在这一章中读者会看到如何将Spring与WebSocket和STOMP结合起来，实现服务端与客户端之间的异步通信。
第19章将会介绍如何使用Spring发送E-mail。
■第20章会关注于Spring对Java管理扩展（Java Management Extensions，JMX）
功能的支持，借助这项功能可以对Spring应用程序进行监控和修改运行时配置。
■最后，在第21章，读者将会看到一个全新并且会改变游戏规则的Spring使用方式，名为Spring Boot。我们将会看到Spring Boot如何将Spring应用中样板式的配置移除掉，这样就能让读者更加专注于业务功能。
代码规范与下载
本书中有大量的示例代码。这些代码将会使用固定宽度的代码字体。本书正文中的类名、方法名或XML片段也都使用代码字体。
很多Spring类和包的名字很长（不过会有较强的表达性）。鉴于此，我们有时候会用到换行符（=）。
本书中的示例代码并不都是完整的。为了关注某个主题，我有时候只会展示类的一个或两个方法。本书所构建的应用程序完整代码可以在出版社站点上下载，地址是www.manning.com/SpringinActionFourthEdition。
**作者在线**
购买了本书，读者就可以免费访问Manning出版社提供的在线论坛，在这里读者可以给本书写评论，问一些技术问题并可以得到作者和其他用户的帮助。要进入这个论坛或订阅它，读者可以在浏览器中访问www.manning.com/SpringinActionFourthEdition。这个页面会告诉读者注册后怎样进入论坛，能够得到什么帮助以及论坛的规则。
Manning对读者的许诺是为读者提供一个交流平台，在这里读者之间以及读者和作者之间可以进行有意义的交流。对于作者来说，对论坛进行多少次的访问不是强制的，他们对本书论坛的贡献是自愿和免费的。我们建议读者尽量向作者问一些有挑战性的问题，以保持他们的兴趣！
只要本书还在发售，读者就可以访问作者在线论坛以及以前讨论的归档信息。

**作者简介**
Craig Walls是Pivotal的高级工程师，是Spring Social和Spring Sync的项目领导者，同时也是Manning 出版社各版Spring lIn Action的作者，目前这本书已经更新到了第4版。他非常热心于Spring框架的推广，经常在当地的用户组和会议上演讲并在博客上撰写Spring相关的内容。在不琢磨代码的时候，Craig Walls会尽可能多地陪伴他的妻子和两个女儿。
**封面插图简介**
《Spring实战》第4版的封面人物是“Le Caraco”，也就是约旦西南部卡拉克（Karak）
省的居民。该省的首府是Al-Karak，那里的山顶有座古城堡，对死海和周边的平原有着极佳的视野。这幅图出自1796年出版的法国旅游图书，Encyclopediedes Voyages，该书由J.G.St.Sauveur编写。在那时，为了娱乐而去旅游还是相对新鲜的做法，而像这样的旅游指南是很流行的，它能够让旅行家和足不出户的人们了解法国其他地区和国外的居民。
Encyclopediedes oyages中多种多样的图画生动描绘了200年前世界上各个城镇和地区的独特魅力。在那时，相隔数十千米的两个地区着装就不相同，可以通过着装判断人们究竟属于哪个地区。这本旅行指南展现了那个时代和其他历史时代的隔离感和距离感，这与我们这个运动过度的时代是截然不同的。
从那以后，服装风格发生了改变，富有地方特色的多样性开始淡化。现在，有时很难说一个洲的居民和其他洲的居民有什么不同。从积极的方面来看，我们或许是用原来文化和视觉上的多样性换来了个人风格的多变性，或者可以说是更为多样化和有趣的知识科技生活。
这本旅行指南中的图片反映了两个世纪前各个地区生活的多样性，我们现在用图书封面的方

式对其进行了再现。Manning出版社的员工都认为这是计算机行业中一个很有意思的创意。

## 2.2自动化装配bean

###    2.2.1　创建可被发现的 bean

@ComponentScan 和 @Component 



@Configuration

@ComponentScan

public class CDPlayerConfig { 

}

### 2.2.2　为组件扫描的 bean 命名

 Spring 会根据类名为其指定一个 ID。具体来讲，这个 bean 所给定的 ID 为 sgtPeppers，也就是将类名的第一个字母变为小写 

@Componet("lonelyHeartsClub")

public class SgtPeppers implements CompactDisc

 Spring 支持将 @Named 作为 @Component 注解的替代方案。两者之间有一些细微的差异，但是在大多数场景中，它们是可以互相替换的。  @Named…… 怎么说呢，我感觉它的名字起得很不好。 

#### 2.2.3　设置组件扫描的基础包
@ComponentScan(basePackages="soundsystem")
@ComponentScan(basePackages={"soundsystem", "video"})
@ComponentScan(basePackageClasses={CDPlayer.class, DVDPlayer.clas}) typesafe
这些类所在的包将会作为组件扫描的基础包。但是你可以考虑在包中创建一个用来进行扫描的空标记接口（marker interface）
### 2.2.4　通过为 bean 添加注解实现自动装配
@Autowired
  public CDPlayer(CompactDisc cd) {
    this.cd = cd;
  }
  @Autowired 注解不仅能够用在构造器上，还能用在属性的 Setter 方法上。比如说，如果 CDPlayer 有一个 setCompactDisc() 方法，那 么可以采用如下的注解形式进行自动装配：
  @Autowired 注解可以用在类的任何方法上。假设 CDPlayer 类有一个 insertDisc() 方法， 那么 @Autowired 能够像在 setCompactDisc() 上那样，发挥完全相同的作用
@Autowired(required=false)
public CDPlayer(CompactDisc cd) {
  this.cd = cd;
}

required 属性设置为false 时
## 2.3　通过 Java 代码装配 bean
###　2.3.1　创建配置类
@Configuration 注解表明这个类是一个配置类，该类应该包含在 Spring 应用上下文中如何创建 bean 的细节
声明简单的 bean
@Bean(name="lonelyHeartsClubBand")
public CompactDisc sgtPeppers() {
  return new SgtPeppers();
}
@Bean
public CompactDisc randomBeatlesCD() {
  int choice = (int) Math.floor(Math.random() * 4);
  if (choice == 0) {
    return new SgtPeppers();
  } else if (choice == 1) {
    return new WhiteAlbum();
  } else if (choice == 2) {
    return new HardDaysNight();
  } else {
    return new Revolver();
  }
}
cdPlayer() 的方法体与 sgtPeppers() 稍微有些区别。在这里并没有使用默认的构造器构建实例，而是调用了需要传入 CompactDisc 对象的构造器来创建 CDPlayer 实例。
<constructor-arg> 和 c- 命名空间的功能是相同的
<constructor-arg value="Sgt. Pepper's Lonely Hearts Club Band" />
<bean id="cdPlayer" class="soundsystem.CDPlayer" c:_-ref="compactDisc" />
<constructor-arg><null/></constructor-arg>

<bean id="compactDisc"
        class="soundsystem.BlankDisc"
        c:_0="Sgt. Pepper's Lonely Hearts Club Band"
        c:_1="The Beatles">
    <constructor-arg>
      <list>
        <value>Sgt. Pepper's Lonely Hearts Club Band</value>
        <value>With a Little Help from My Friends</value>
        <value>Lucy in the Sky with Diamonds</value>
        <value>Getting Better</value>
        <value>Fixing a Hole</value>
        <!-- ...other tracks omitted for brevity... -->
      </list>
    </constructor-arg>
  </bean>

  也可以使用 <ref> 元素替代 <value>

  如果是 Set 的话，所有重复的值都会被忽略掉，存放顺序也不会得以保证。不过无论在哪种情况下，<set> 或 <list> 都可以用来装配 List、Set 甚至数组。
  <constructor-arg> 比 c- 命名空间的属性更有优势。目前，使用 c- 命名空间的属性无法实现装配集合的功能。

###  2.4.4　设置属性
作为一个通用的规则，我倾向于对强依赖使用构造器注入，而对可选性的依赖使用属性注入。
<bean id="cdPlayer" class="soundsystem.CDPlayer" >
  <property name="compactDisc" ref="compactDisc" />
</bean>

<util:list id="trackList">
  <value>Sgt. Pepper's Lonely Hearts Club Band</value>
  <value>With a Little Help from My Friends</value>
  <value>Lucy in the Sky with Diamonds</value>
  <value>Getting Better</value>
  <value>Fixing a Hole</value>
  <!-- ...other tracks omitted for brevity... -->
</util:list>

### JavaConfig 中引用 XML 配置的 bean

假设 BlankDisc 定义在名为 cdconfig. xml 的文件中，该文件位于根类路径下，那么可以修改 SoundSystemConfig，让它使用 @ImportResource 注解，如 下所示
@Configuration
@Import(CDPlayerConfig.class)
@ImportResource("classpath:")
public class SoundSystemConfig {

### 在 XML 配置中引用 JavaConfig

< import resource ="cd-config.xml">



 <bean class="soundsystem.CDConfig" /> 

 不管使用 JavaConfig 还是使用 XML 进行装配，我通常都会创建一个根配置（root configuration），也就是这里展现的这样，这个配置会将两个或更多的装配类或 XML 文件组合起来。我也会在根配置中启用组件扫描 

 我也会在根配置中启用组件扫描（通过 `` 或 @ComponentScan）。你会在本书的很多例子中看到这种技术。 

## 3高级装配

### 环境profile

<beans xmlns="http://www.springframework.org/schema/beans"

  xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:jdbc="http://www.springframework.org/schema/jdbc"

  xmlns:jee="http://www.springframework.org/schema/jee" xmlns:p="http://www.springframework.org/schema/p"

  xsi:schemaLocation="

​    http://www.springframework.org/schema/jdbc

​    http://www.springframework.org/schema/jdbc/spring-jdbc.xsd

​    http://www.springframework.org/schema/beans

​    http://www.springframework.org/schema/beans/spring-beans.xsd"

profile ="dev ">

激活

 spring.profiles.active 

 spring.profiles.default 

```
 <servlet>
    <servlet-name>appServlet</servlet-name>
    <servlet-class>
      org.springframework.web.servlet.DispatcherServlet
    </servlet-class>
    <init-param>
      <param-name>spring.profile.default</param-name>
      <param-value>dev</param-value>
    </init-param>
    <load-on-startup>1</load-on-startup>
  </servlet>
```

 e。在集成测试时，通常想要激活的是开发环境的 profile。例如，下面的测试类片段展现了使用 @ActiveProfiles 激活 dev profile： 

```
@RunWith(SpringJUnit4ClassRunner.class)
@ContextConfiguration(classes={PersistenceTestConfig.class})
@ActiveProfile("dev")
public class PersistenceTest {
  ...
}
```
## 3.2　条件化的 bean

@Bean

@Conditioal(MagicExistsCondition.class)

public MagicBean magicBean() {

  return new MagicBean();

}



```
public class MagicExistsCondition implements Condition {

  @Override
  public boolean matches(ConditionContext context, AnnotatedTypeMetadata metadata) {
    Environment env = context.getEnvironment();
    return env.containsProperty("magic");
  }
  
}
```

## 3.3　处理自动装配的歧义性

### 3.3.1　标示首选的 bean

```
ceCream.java
@Component
@Primary
public class IceCream implements Dessert { ... }
```

#### 3.3.2　限定自动装配的 bean

```
@Autowired
@Qualifier("iceCream")
public void setDessert(Dessert dessert) {
  this.dessert = dessert;
}
```

  @Qualifier 注解所设置的参数就是想要注入的 bean 的 ID 

 并且 bean 的 ID 为首字母变为小写的类名 

 如果没有指定其他的限定符的话，所有的 bean 都会给定一个默认的限定符，这个限定符与 bean 的 ID 相同 

 创建自定义的限定符 

@Component

@Qualifier("cold")

public class IceCream implements Dessert { ... }

```
@Target({ElementType.CONSTRUCTOR, ElementType.FIELD,
         ElementType.METHOD, ElementType.TYPE})
@Retention(RetentionPolicy.RUNTIME)
@Qualifier
public @interface Cold { }
```

##  bean 的作用域
Spring 应用上下文中所有 bean 都是作为以单例（singleton）的形式创建的
单例（Singleton）：在整个应用中，只创建 bean 的一个实例。
原型（Prototype）：每次注入或者通过 Spring 应用上下文获取的时候，都会创建一个新的 bean 实例。
会话（Session）：在 Web 应用中，为每个会话创建一个 bean 实例。
请求（Rquest）：在 Web 应用中，为每个请求创建一个 bean 实例。
单例是默认的作用域，但是正如之前所述，对于易变的类型，这并不合适
```
@Component
@Scop(ConfigurableBeanFactory.SCOPE_PROTOTYPE)
public class Notepad { ... }
```

```
@Component
@Scope(value=WebApplicationContext.SCOPE_SESSION,
       proxyMode=ScopedProxyMode.INTERFACES)
public ShoppingCart cart() { ... }
```

 ```
@Component
public class StoreService {
  @Autowired
  public void setShoppingCart(ShoppingCart shoppingCart) {
    this.shoppingCart = shoppingCart;
  }
}
 ```



ScopedProxyMode.INTERFACES。这个属性解决了将会话或请求作用域的 bean注入到单例 bean 中所遇到的问题 

 Spring 并不会将实际的 ShoppingCart bean 注入到 StoreService 中， Spring 会注入一个到 ShoppingCart bean 的代理，如图 3.1 所示。这个代理会暴露与 ShoppingCart 相同的方法，所以 StoreService 会认为它就是一个购物车。但是，当 StoreService 调用 ShoppingCart 的方法时，代理会对其进行懒解析并将调用委托给会话作用域内真正的 ShoppingCart bean 

 现在，我们带着对这个作用域的理解，讨论一下 proxyMode 属性。如配置所示，proxyMode 属性被设置成了 ScopedProxyMode.INTERFACES，这表明这个代理要实现 ShoppingCart 接口，并将调用委托给实现 bean。 



 果 bean 类型是具体类的话，我们必须要将 proxyMode 属性设置为 ScopedProxyMode.TARGET_CLASS， 

 ![img](https://blobs.gitbook.com/assets%2F-LmcjU5gG__lBrRbUxBO%2F-LmiQ61862BoBNRvox70%2F-LmiSJlApcjq0dtWq1Vz%2F3.1%20%E4%BC%9A%E8%AF%9D%E4%BD%9C%E7%94%A8%E5%9F%9F.jpg?alt=media&token=e5340648-1cc1-4fdb-af72-c9893f795efa) 

```
<bean id="cart" class="com.myapp.ShoppingCart" scope="session">
  <aop:scoped-proxy />
</bean>
```

## 3.5　运行时值注入
Spring提供了两种在运行时求值的方式：
属性占位符（Property placeholder）。
Spring 表达式语言（SpEL）。

```
@Configuration
@PropertySource("classpath:/com/soundsystem/app.properties")
public class ExpressiveConfig {
  
  @Autowired
  Environment env;
  
  @Bean
  public BlankDisc disc() {
    return new BlankDisc(
      env.getProperty("disc.title"),
      env.getProperty("disc.artist")
    );
  }
}
```

 @PropertySource 引用了类路径中一个名为 app.properties 的文件 

```
disc.title=Sgt. Peppers Lonely Hearts Club
disc.artisc=The Beatles
```

 指定属性不存在的时候，会使用一个默认值： 

```
@Bean
public BlankDisc disc() {
  env.getProperty("disc.title", "Rattle and Hum"),
  env.getProperty("disc.artist", "U2")
}
```

```
int connectionCount = env.getProperty("db.connection.count", Integer.class, 30);
```

```
@Bean
public BlankDisc disc() {
  env.getRequiredProperty("disc.title");
  env.getRequiredProperty("disc.artist");
}
```

```
boolean titleExists = env.containsProperty("disc.title");
```

```
Class<CompactDisc> cdClass = env.getPropertyAdClass("disc.class", CompactDisc.class);
```

 占位符的形式为使用 `${ ... }` 包装的属性名称 

```
<bean id="sgtPeppers" class="soundsystem.BlankDisc"
      c:_title="${disc.titlte}"
      c:_artist="${disc.artist}" />
```

```
public BlankDisc(
  @Value("${disc.title}") String title,
  @Value("${disc.artist}") String artist) {
    this.title = title;
    this.artist = artist;
}
```

```
@Bean
public PropertySourcesPlaceholderConfigurer placeholderConfigurer() {
  return new PropertySourcesPlaceholderConfigurer();
}
```

 如果你想使用 XML 配置的话，Spring context 命名空间中的 `` 元素将会为你生成 PropertySourcesPlaceholderConfigurer bean 

 <context:property-placeholder /> 

### 3.5.2　使用 Spring 表达式语言进行装配

SpEL样例

 \#{1} 

 \#{systemProperties['disc.title']} 

```
public BlankDisc(
  @Value("#{systemProperties['disc.title']}") String title,
  @Value("#{systemProperties['disc.artist']}") String artist) {
    this.title = title;
    this.artist = artist;
}
```

```
<bean id="sgtPeppers" class="soundsystem.BlankDisc"
      c:_title="#{systemProperties['disc.title']}"
      c:_artist="#{systemProperties['disc.artist']}" />
```

 SpEL 所能做的另外一件基础的事情就是通过 ID 引用其他的 bean 

```
#{artistSelector.selectArtist()?.toUpperCase()}
```

 如果要在 SpEL 中访问类作用域的方法和常量的话，要依赖 `T()` 这个关 键的运算符。例如，为了在 SpEL 中表达 Java 的 Math 类，需要按照如下的方式使用 `T()` 运算符 

 但是 `T()` 运算符的真正价值在于它能够访问目标类型的静态方法和常量。

```
T(java.lang.Math).PI
```

```
#{disc.title + ' by ' + disc.artist}
```



 ```
#{disc.title ? : 'Rattle and Hum'}
 ```

```
#{admin.email matches '[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\\.com'}
```

```
#{jukebox.songs[T(java.lang.Math).random()
                * jukebox.songs.size()].title}
```

 它还可以从 String 中获取一个字符 

```
#{'This is a text'[3]}
```

 SpEL 还提供了查询运算符 `.?[]` 

  jukebox 中 artist 属性为 Aerosmith 的所有歌曲 

```
#{jukebox.songs.?[artist eq 'Aerosmith']}
```

 `.^[]` 和 `.$[]`，它们分别用来在集合中查询第一个匹配项和最后一个匹配项。 

 它会查找列表中第一个 artist 属性为 Aerosmith 的歌曲 

```
#{jukebox.songs.^[artist eq 'Aerosmith']}
```

 投影运算符 `.![]` 

```
#{jukebox.songs.![title]}
```

  比如，我们可以使用如下的表达式获得 Aerosmith 所有歌曲的名称列表： 

```
#{jukebox.songs.?[artist eq 'Aerosmth'].![title]}
```



SpEL 毕竟只是 String 类型的值，可能测试起来很困难。鉴于这一点，我建议尽可能让表达式保持简洁，这样测试不会是什么大问题 

# 第 4 章　面向切面的 Spring

### 4.2.1　编写切点

```
package concert;

public interface Performance {
  public void perform();
}
```

 ![img](https://blobs.gitbook.com/assets%2F-LmcjU5gG__lBrRbUxBO%2F-LmlwvpSFQKBStsU1vhe%2F-LmlxffhI8KN5-LcDT6J%2F4.4%20aop%20perform().jpg?alt=media&token=0fcf3849-7e53-475b-8f2a-5fc7fe39a8a0) 

 ![img](https://blobs.gitbook.com/assets%2F-LmcjU5gG__lBrRbUxBO%2F-LmlwvpSFQKBStsU1vhe%2F-LmlyBCR2SrunZF2A344%2F4.5%20aop%20within%E6%8C%87%E7%A4%BA%E5%99%A8.jpg?alt=media&token=297cdf21-761e-4d13-bd80-c112bb6d0266) 

 需要配置的切点仅匹配 concert 包。在此场景下，可以使用 within() 指示器来限制匹配 

### 4.2.2　在切点中选择 bean

execution(* concert.Performance.perform()) and bean('woodstock')

```
package concert;

import org.aspect.lang.annotation.AfterReturning;
import org.aspect.lang.annotation.AfterThrowing;
import org.aspect.lang.annotation.Aspect;
import org.aspect.lang.annotation.Before;

@Aspect
public class Audience {

  @Before("execution(** concert.Performance.perform(..))")
  public void silenceCellPhones() {
    System.out.println("Silencing cell phones");
  }
  
  @Before("execution(** concert.Performance.perform(..))")
  public void takeSeats() {
    System.out.println("Taking seats");
  }
  
  @AfterReturning("execution(** concert.Performance.perform(..))")
  public void applause() {
    System.out.println("CLAP CLAP CLAP!!!");
  }
  
  @AfterThrowing("execution(** concert.Performance.perform(..))")
  public void demandRefund() {
    System.out.println("Demanding a refund");
  }
}
```

```
package concert;

import org.aspect.lang.annotation.AfterReturning;
import org.aspect.lang.annotation.AfterThrowing;
import org.aspect.lang.annotation.Aspect;
import org.aspect.lang.annotation.Before;
import org.aspect.lang.annotation.Pointcut;

@Aspect
public class Audience {

  @Pointcut("execution(** concert.Performance.perform(..))")
  public void performce() { }

  @Before("performce()")
  public void silenceCellPhones() {
    System.out.println("Silencing cell phones");
  }
  
  @Before("performce()")
  public void takeSeats() {
    System.out.println("Taking seats");
  }
  
  @AfterReturning("performce()")
  public void applause() {
    System.out.println("CLAP CLAP CLAP!!!");
  }
  
  @AfterThrowing("performce()")
  public void demandRefund() {
    System.out.println("Demanding a refund");
  }
}
```

```
package concert;

import org.springframework.context.annotation.Bean;
import org.springframework.context.annotation.Component;
import org.springframework.context.annotation.Configuration;
import org.springframework.context.annotation.EnableAspectJAutoProxy;

@Configuration
@EnableAspectJAutoProxy
@Component
public class ConcertConfig {

  @Bean
  public Audience audience() {
    return new Audience();
  }
}
```

 使用 XML 来装配 bean 的话，那么需要使用 Spring aop 命名空间中的 <aop:aspectj-autoproxy> 元素。 

### 4.3.2　创建环绕通知
```
package concert;

import org.aspect.lang.annotation.ProceedingJoinPoint;
import org.aspect.lang.annotation.Around;
import org.aspect.lang.annotation.Aspect;
import org.aspect.lang.annotation.Pointcut;

@Aspect
public class Audience {

  @Pointcut("execution(** concert.Performance.perform(..))")
  public void performce() { }

  @Around("performce()")
  public void watchPerformance(ProceedingJoinPoint jp) {
    try {
      System.out.println("Silencing cell phones");
      System.out.println("Taking seats");
      jp.procee();
      System.out.println("CLAP CLAP CLAP!!!");
    } catch (Throwable e) {
      System.out.println("Demanding a refund");
    }
  }
}
```

 有意思的是，你可以不调用 proceed() 方法，从而阻塞对被通知方法的访问，与之类似，你也可以在通知中对它进行多次调用。要这样做的一个场景就是实现重试逻辑，也就是在被通知方法失败后，进行重复尝试。 

```
package soundsystem;

import java.util.HashMap;
import java.util.Map;
import org.aspect.lang.annotation.Aspect;
import org.aspect.lang.annotation.Before;
import org.aspect.lang.annotation.Pointcut;

@Aspect
public class TrackCounter {

  private Map<Integer, Integer> trackCounts = new HashMap<>();
  
  @Pointcut("execution(* soundsystem.CompactDisc.playTrack(int) " +
            "&& args(trackNumber)")
  public void trackPlayed(int trackNumber) { }

  @Before("trackPlayed(trackNumber)")
  public void countTrack(int trackNumber) {
    int currentCount = getPlayCount(trackNumber);
    trackCounts.put(trackNumber, currentCount + 1);
  }
  
  public int getPlayCount(int trackNumber) {
    return trackCounts.containsKey(trackNumber) ? trackCounts.get(trackNumber) : 0;
  }
}
```

  ![img](https://blobs.gitbook.com/assets%2F-LmcjU5gG__lBrRbUxBO%2F-LmmGo_dGbf1__H-brHH%2F-LmmGqlzHuH0x9Ab4YL-%2F4.6%20%E5%88%87%E7%82%B9%E5%8F%82%E6%95%B0.jpg?alt=media&token=eed595cd-50b9-42c3-b764-dca966c82571)  

### 4.3.4　通过注解引入新功能

```
package concert;

import org.aspectj.lang.annotation.Aspect;
import org.aspectj.lang.annotation.DeclareParents;

@Aspect
public class EncodeableIntroducer {

  @DeclareParents(value="concert.Performce+",
                  defaultImpl=DefaultEncoreable.class)
  public static Encoreable encoreable;
}
```

@DeclareParents 注解由三部分组成：

- value 属性指定了哪种类型的 bean 要引入该接口。在本例中，也就是所有实现 Performance 的类型。（标记符后面的加号表示是 Performance 的所有子类型，而不是 Performance 本身。）

- defaultImpl 属性指定了为引入功能提供实现的类。在这里，我们指定的是 DefaultEncoreable 提供实现。

- @DeclareParents 注解所标注的静态属性指明了要引入了接口。在这里，我们所引入的是 Encoreable 接口。

- <bean class="concert.EncoreableIntroducer" />

  

  ## 在 XML 中声明切面

 例如，我们重新看一下 Audience 类，这一次我们将它所有的 AspectJ 注解全部移除掉 

```
package concert;

public class Audience {
  
  public void silenceCellPhones() {
    System.out.println("Silencing cell phones");
  }
  
  public void takeSeats() {
    System.out.println("Taking seats");
  }
  
  public void applause() {
    System.out.println("CLAP CLAP CLAP!!!");
  }
  
  public void demandRefund() {
    System.out.println("Demanding a refund");
  }
}
```

```
<aop:config>
  <aop:aspect ref="audience">
  
    <aop:before
      pointcut="execution(** concert.Performance.perform(..))"
      method="silenceCellPhones" />
    
    <aop:before
      pointcut="execution(** concert.Performance.perform(..))"
      method="takeSeats" />
      
    <aop:after-returning 
      pointcut="execution(** concert.Performance.perform(..))"
      method="applause" />
      
    <aop:after-throwing
      pointcut="execution(** concert.Performance.perform(..))"
      method="demandRefund" />
      
  </aop:aspect>
</aop:config>
```

  AOP 配置元素必须在 <aop:config> 元素的上下文内使用。 

 ![img](https://blobs.gitbook.com/assets%2F-LmcjU5gG__lBrRbUxBO%2F-Lmn2yf0HE0iEFjInXks%2F-Lmn377KqbI62C-LKH1L%2F4.8%20audience%20%E5%88%87%E9%9D%A2.jpg?alt=media&token=c40df0b0-1838-45a3-8f52-bb4cb963997c) 

```
<aop:config>
  <aop:aspect ref="audience">
    <aop:pointcut
      id="performance"
      expressions="execution(** concert.Performance.perform(..))" />
  
    <aop:before
      pointcut-ref="performance"
      method="silenceCellPhones" />
    
    <aop:before
      pointcut-ref="performance"
      method="takeSeats" />
      
    <aop:after-returning 
      pointcut-ref="performance"
      method="applause" />
      
    <aop:after-throwing
      pointcut-ref="performance"
      method="demandRefund" />
      
  </aop:aspect>
</aop:config>
```

### 4.4.2　声明环绕通知

```
package concert;

import org.aspectj.lang.ProceedingJoinPoint;

public class Audience {

  public void watchPerformance(ProceedingJoinPoint jp) {
    try {
      System.out.println("Silencing cell phones");
      System.out.println("Taking seats");
      jp.procee();
      System.out.println("CLAP CLAP CLAP!!!");
    } catch (Throwable e) {
      System.out.println("Demanding a refund");
    }
  }
}
```

 假设除了进场关闭手机和表演结束后鼓掌，我们还希望观众确保一直关注演出，并报告每个参赛者表演了多长时间。使用前置通知和后置通知实现该功能的唯一方式是在前置通知中记录开始时间并在某个后置通知中报告表演耗费的时间。但这样的话我们必须在一个成员变量中保存开始时间。因为 Audience 是单例的，如果像这样保存状态的话，将会存在线程安全问题。 

```
package concert;

import org.aspectj.lang.ProceedingJoinPoint;

public class Audience {

  public void watchPerformance(ProceedingJoinPoint jp) {
    try {
      System.out.println("Silencing cell phones");
      System.out.println("Taking seats");
      jp.procee();
      System.out.println("CLAP CLAP CLAP!!!");
    } catch (Throwable e) {
      System.out.println("Demanding a refund");
    }
  }
}
```

```
<aop:config>
  <aop:aspect ref="audience">
    <aop:pointcut
      id="performance"
      expression="execution(** concert.Performance.perform(..))" />
    
    <aop:around
      pointcut-ref="performance"
      method="watchPerformance" />
      
  </aop:aspect>
</aop:config>
```

参数

```
package soundsystem;

import java.util.HashMap;
import java.util.Map;

public class TrackCounter {

  private Map<Integer, Integer> trackCounts = new HashMap<>();
  
  public void trackPlayed(int trackNumber) { }

  public void countTrack(int trackNumber) {
    int currentCount = getPlayCount(trackNumber);
    trackCounts.put(trackNumber, currentCount + 1);
  }
  
  public int getPlayCount(int trackNumber) {
    return trackCounts.containsKey(trackNumber) ? trackCounts.get(trackNumber) : 0;
  }
}
```

```
<?xml version="1.0" encoding="UTF-8"?>
<beans xmlns="http://www.springframework.org/schema/beans"
  xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
  xmlns:aop="http://www.springframework.org/schema/aop"
  xmlns:util="http://www.springframework.org/schema/util"
  xsi:schemaLocation="
    http://www.springframework.org/schema/aop
    http://www.springframework.org/schema/aop/spring-aop.xsd
    http://www.springframework.org/schema/beans
    http://www.springframework.org/schema/beans/spring-beans.xsd" >
  
  <bean id="trackCounter" class="soundsystem.TrackCounter" />
  
  <bean id="cd" class="soundsystem.BlackDisc" >
    <property name="title" value="Sgt. Pepper's Lonelt Hearts Club Band" />
    <property name="artist" value="The Beatles" />
    <property name="tracks" >
      <list>
        <value>Sgt. Pepper's Lonely Hearts Club Band</value>
        <value>Lucy in the Sky with Diamonds</value>
        <value>Getting Better</value>
        <value>Fixing a Hole</value>
        <!-- ...other tracks omitted for brevity... -->
      </list>
    </property>
  </bean>
  
  <aop:config>
    <aop:aspect ref="trackCounter">
      <aop:pointcut
        id="trackPlayed"
        expression="execution(* soundsystem.CompactDisc.playTrack(int)) and args(trackNumber)" />
        
      <aop:before pointcut-ref="trackPlayed" method="countTrack" />
    </aop:aspect>
  </aop:config>
  
</beans>
```

