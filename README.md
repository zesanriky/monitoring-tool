### How to run this monitoring tool

#### We can run the homepage under localhost
```
http://localhost:8080/actuator
```
#### For checking the /metrics endpoint of the Actuator we should navigate to the following

```
http://localhost:8080/actuator/metrics
```
 
#### We can try to retreive the JVM usage information as follows: 
 
```
http://localhost:8080/actuator/metrics/jvm.memoery.used
```

#### Prometheus is used as time series database. We can see the result of new endpoint as follows:

```http://localhost:8080/actuator/prometheus
```



#### Prometheus is used as time series database. We can see the result of new endpoint as follows:

```http://localhost:8080/actuator/prometheus
```



####  The Prometheus database wil store the metric data after pulling it over HTTP. 


#### For running the Prometheus suing Docker command
```
$ docker run -d -p 9090:9090 -v <path-to-prometheus.yml>:/etc/prometheus/prometheus.yml prom/prometheus
```


#### While opening the Prometheus dashboard, use this URL 
```
http://localhost:9090

```

#### Is Prometheus istening to our Spring app? let's check it 
```
http://localhost:9090/targets

```


#### Is Prometheus istening to our Spring app? let's check it 
```
http://localhost:9090/targets

```


#### Is Prometheus istening to our Spring app? let's check it 
```
http://localhost:9090/targets

```

Let's go back to the home page and select a metric from the list and click Execute:




