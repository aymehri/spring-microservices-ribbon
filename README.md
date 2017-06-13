```
\\ 1) Run Eureka Server
\\ 2) Run 2 'ribbon-time-service' instances see README.MD in 'ribbon-time-service' ( in this example the two services run without service discovery)
\\ 3) Run 'ribbon-time-app' and hit localhost:8080 and you will see the server sometimes call instance 1 and sometimes instance 2 ( runs with a client custom configuration)

IRule : to choose a custom balancing rule ( RoundRobbin is default), in this example : i changed it to RandomRule
IPing : to choose the choose the strategy or the avaibility : (DummyPing or PingUrl : make http call to the service, NIWSDiscoveryPing : automatic by eureka)
```