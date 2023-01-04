
```
默认支持从nacos获取节点，但是需要明确配置了服务名的才会获取，本插件改动的规则是获取所有的服务节点，便于从路径中动态解析出服务名，例如
下一步改动点:
创建路由的“上游服务”的服务名称，需要改为动态的，例如：${servicename}，然后从路径中动态解析出来，
例如规则：/api/sso/${servicename} -> ${servicename}
访问路径：/api/sso/hello1/xxx -> 解析：hello1 -> 最终网关代理访问：http://hello1/xxx
```
## 修改过的nacos插件，可跟nacos-default文件夹对比看看改过哪些地方了
