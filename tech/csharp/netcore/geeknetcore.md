configerwebhost();

startup只是代码结构更加合理。

configerservice是注册类

startup.configure注入中间件。



扩展方法实现  具体实现的隔离；

具体实现私有的然后扩展方式暴漏出去

configure<orderServiceoption>()// 有注入的意思



## log

  "IncludeScopes": true  



 var eventName = eventArgs.RoutingKey;



  var integrationEvent = JsonSerializer.Deserialize(message, eventType, new JsonSerializerOptions() { PropertyNameCaseInsensitive= true});                            
                          

### grpc

dotnet tool install dotnet-grpc -g-