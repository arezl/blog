```

return services.AddAbp<JosenWebHostModule>(
                // Configure Log4Net logging
                options => options.IocManager.IocContainer.AddFacility<LoggingFacility>(
                    f => f.UseAbpLog4Net().WithConfig("log4net.config")
                )
            );
```

```
  [DependsOn(
       typeof(JosenWebCoreModule))]
    public class JosenWebHostModule: AbpModule
```

```
    [DependsOn(
        typeof(JosenCoreModule), 
        typeof(AbpAutoMapperModule))]
    public class JosenApplicationModule : AbpModule
```

```
    [DependsOn(typeof(AbpZeroCoreModule))]
    public class JosenCoreModule : AbpModule
```

