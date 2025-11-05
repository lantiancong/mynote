# AOP

## 动态代理

```java
package com.lan.demo3proxy;

import java.lang.reflect.InvocationHandler;
import java.lang.reflect.Method;
import java.lang.reflect.Proxy;

public class ProxyInvocationHandler implements InvocationHandler {

    Object target;
    
    public ProxyInvocationHandler(Object target) {
        this.target = target;
    }
    
    public Object getProxy(){
        return Proxy.newProxyInstance(this.getClass().getClassLoader(), target.getClass().getInterfaces(), this);
    }

    @Override
    public Object invoke(Object proxy, Method method, Object[] args) throws Throwable {
        log(method.getName());
        Object result = method.invoke(target, args);
        return result;
    }

    public void log(String msg) {
        System.out.println("执行了"+msg+"方法");
    }
}

```

主函数

```java
public class Client {
    public static void main(String[] args) {
        UserService userService = new UserServiceImpl();
        ProxyInvocationHandler handler = new ProxyInvocationHandler(userService);
        UserService proxy= (UserService) handler.getProxy();

        proxy.query();
    }
}
```

