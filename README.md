# spring-boot-starter-batch-conflict-example

Here's a weird conflict if you're feeling bored.

Build this project and run it. It should work (it doesn't do much, it's a bog-standard Spring Batch example).

Now uncomment the spring-boot-starter-data-jpa dependency in the pom. Rebuild and rerun. You will get the following error:
`
Caused by: java.lang.NullPointerException: null
	at java.base/java.lang.reflect.Method.invoke(Method.java:557) ~[na:na]
	at org.springframework.aop.support.AopUtils.invokeJoinpointUsingReflection(AopUtils.java:333) ~[spring-aop-4.3.14.RELEASE.jar:4.3.14.RELEASE]
	at org.springframework.aop.framework.ReflectiveMethodInvocation.invokeJoinpoint(ReflectiveMethodInvocation.java:190) ~[spring-aop-4.3.14.RELEASE.jar:4.3.14.RELEASE]
	at org.springframework.aop.framework.ReflectiveMethodInvocation.proceed(ReflectiveMethodInvocation.java:157) ~[spring-aop-4.3.14.RELEASE.jar:4.3.14.RELEASE]
	at org.springframework.batch.core.configuration.annotation.SimpleBatchConfiguration$PassthruAdvice.invoke(SimpleBatchConfiguration.java:127) ~[spring-batch-core-3.0.8.RELEASE.jar:3.0.8.RELEASE]
  ...`

Do not pass go, do not collect $200, do not taunt happy fun ball...
