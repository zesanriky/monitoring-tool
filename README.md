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
Setup a webpage that shows a moving average value in table or graph of response time for
every 10 second, 1 minute and 1-hour

#### We can now redirect to our home page and select a metric from the list and click Execute. Here we can set teh time for every 10 second, 1 minute and 1-hour for the graphical response. 
  

Grafana offers a rich UI where you can build up custom graphs quickly and create a dashboard out of many graphs in no time. 

#### If we want to have individual graphs then Grafna can pull data from various sources like, Prometheus or InfluxDB. THe Grafna also helps us for producing custom graphs. 


### For lauching the grafana using docker image we run the following:


```
$ docker run -d -p 3000:3000 grafana/grafana

```

### Now we can visit 
```
http://localhost:3000
```

#### We can choose admin as username and password by dafult. After logging in let's choose the Prometheus as our data source. To make sure wheather the Prometheus is running we can check by caling the URL 

```
http://localhost:9090
```

### On the GUI we should select the access through a browser and setting up HTTP method as GET.

### If everything is working fine then it would displays the message called "Data source is working"    

### There are some pre-built dashboards. But for Spring Boot projects, JVM can be used.
```
https://grafana.com/grafana/dashboards/4701
```



