1. Записать, что означает:
```java
ChannelFuture future = bootstrap.bind().sync();  
log.info("Server started");  
future.channel().closeFuture().sync();
```
в классе запуска ServerBootstrap

2. Методы fireChannel... как и для чего используются (fireChannelRead - передает сообщение следующему обработчику в метод channelRead0)

