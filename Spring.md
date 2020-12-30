# Spring

## 1. Add history router support in backend
```java
public class ApplicationConfig extends WebMvcConfigurerAdapter {
    @Override
    public void addResourceHandlers(ResourceHandlerRegistry registry) {
        registry.addResourceHandler("/vue", "/vue/", "/vue/**")
                .addResourceLocations("/vue_dist/")
                .resourceChain(true)
                .addResolver(new PathResourceResolver() {
                    @Override
                    protected Resource getResource(String resourcePath, Resource location) throws IOException {
                        Resource requestedResource = location.createRelative(resourcePath);
                        return requestedResource.exists() && requestedResource.isReadable() ? requestedResource
                                : resourceLoader.getResource("/vue_dist/index.html");
                    }
                });
    }
}
```

Say you have `/vue_dist/` as vue/react/angular build folder, and the target path is `/vue/**`, you can use this pattern in .
