Redis Session Manager for Apache Tomcat (Supports JedisCluster)
=======================================

Config Sample

Add the following into your Tomcat context.xml (or the context block of the server.xml if applicable.)
Password is optional.

```
    <Valve className="com.orangefunction.tomcat.redissessions.RedisSessionHandlerValve" />
    <Manager className="com.orangefunction.tomcat.redissessions.RedisSessionManager"
         redisNodes="192.168.1.81:7001,192.168.1.81:7002,192.168.1.81:7003,192.168.1.82:7004,192.168.1.82:7005,192.168.1.82:7006"
         password="redis_password"
         timeout="300000"
         maxRedirections="6"
         maxWaitMillis="-1"
         maxTotal="1000"
         minIdle="8"
         maxIdle="100"
         maxInactiveInterval="60"/>
```
