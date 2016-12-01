Application resilliency is a complex, but extremely important topic, especially for distributed applications. Resilliency of distributed systems is influenced by many charachteristics but one of the most important of these is the ability to detect and recover from application failure. Docker Swarm has a full suite of features that can be used to monitor application health and also react appropriately to failure. 

There are two policies in the Docker Engine and Swarm that govern failure & recovery - __health policy__ and __restart policy__. Each of these policies is a group of configurable items that influence how containers & services are monitored and recovered.

####Health Policy

```
curl --fail http://localhost:5000/health
--interval=30s
--timeout=30s 
--retries=3
```

####Restart Policy
```
--restart-condition always
--stop-grace-period 60s
--restart-max-attempts 3
```

####Application Failure and Recovery
![Recovery](./img/recover.png)

####Application Failure and Reschedule
![Recovery](./img/reschedule.png)



 