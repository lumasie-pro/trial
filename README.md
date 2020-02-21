Shiro定制Kisso登录

定义AuthenticationToken继承UsernamePasswordToken，增加需要的参数

定义Realm实现类，在这个方法中实现登录逻辑protected AuthenticationInfo doGetAuthenticationInfo(AuthenticationToken token) throws AuthenticationException 

在登录的实现方法中，SimpleAuthenticationInfo类中的 principal 封装登录关键信息（比如，用户ID，机构ID等）

返回前，处理一下Kisso，？？？ Shiro处理单点登录的问题

在Realm的protected AuthorizationInfo doGetAuthorizationInfo(PrincipalCollection principal) 这个方法中，参数principal就是登录Set进去的Session User对象，再根据系统对于用户角色的关系，查找角色权限数据





参考：https://my.oschina.net/qwzhang01/blog/1620564



​        https://github.com/yz-java/shiro-parent

https://github.com/zhangkaitao/shiro-example

https://github.com/zhangdaiscott/jeecg-boot

