# [Asp.Net Core轻量级Aop解决方案：AspectCore](https://www.cnblogs.com/liuhaoyang/p/aspectcore-introduction-1.html)



```c#

ProxyGeneratorBuilder proxyGeneratorBuilder = new ProxyGeneratorBuilder();
        IProxyGenerator proxyGenerator = proxyGeneratorBuilder.Build();
        SampleInterface sampleInterface = proxyGenerator.CreateInterfaceProxy<SampleInterface,SampleClass>();
        Console.WriteLine(sampleInterface);
        sampleInterface.Foo();
        Console.ReadKey();

```

# [AspectCore.Extension.Reflection : .NET Core反射扩展库](https://www.cnblogs.com/liuhaoyang/p/aspectcore_extension_reflection.html)

 [AspectCore.Extension.Reflection](https://github.com/dotnetcore/AspectCore-Framework/tree/dev/reflection) 

# [AspectCore中的IoC容器和依赖注入](https://www.cnblogs.com/liuhaoyang/p/dependencyinjection-in-aspectcore.html)

# [使用AspectCore动态代理](https://www.cnblogs.com/liuhaoyang/p/aspectcore-getting-started.html)

# [聊聊AspectCore动态代理中的拦截器](https://www.cnblogs.com/liuhaoyang/p/interceptor-in-aspectcore-part-1.html)

 特性拦截器  我们继承AbstractInterceptorAttribute来实现一个自己的特性拦截器 

 全局拦截器配置。我们继承AbstractInterceptor来实现一个自己的特性拦截器（除不能作为`Attribute`标记在口，类或者方法上之外 

### 使用通配符或者委托配置拦截器

在AspectCore中配置全局拦截器时，可以使用通配符或者委托来限定拦截器的作用范围。
内置提供了`Predicates.ForMethod`,`Predicates.ForService`,`Predicates.ForNameSpace`三个通配符函数：

```c#
 services.AddDynamicProxy(config =>
 {
     config.Interceptors.AddTyped<CustomInterceptor>(Predicates.ForMethod("*Query")); //拦截所有Query后缀的方法
     config.Interceptors.AddTyped<CustomInterceptor>(Predicates.ForService("*Repository")); //拦截所有Repository后缀的类或接口
     config.Interceptors.AddTyped<CustomInterceptor>(Predicates.ForNamespace("AspectCoreDemo.*")); //拦截所有AspectCoreDemo及其子命名空间下面的接口或类
 });
```

# [Apache SkyWalking 为.NET Core带来开箱即用的分布式追踪和应用性能监控](https://www.cnblogs.com/liuhaoyang/p/skywalking-dotnet-v02-release.html)

<img src="F:\Code\github\document\blog\tech\csharp\分析aopFramwork\aop framework.assets\image-20200706223034421.png" alt="image-20200706223034421" style="zoom:200%;" />

