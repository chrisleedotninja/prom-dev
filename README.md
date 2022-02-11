# Config
Update Alertmanager config with a valid Slack `api_url`


Update YACE env.list file with valid AWS creds:
```
AWS_ACCESS_KEY_ID=KEYHERENOQUOTES
AWS_SECRET_ACCESS_KEY=SECRETACCESSKEYHERENOQUOTES
AWS_SESSION_TOKEN=AWSSESSIONTOKENHEREWITHNOQUOTES
```


# Running
Start:
`HOSTNAME=$(hostname) docker stack deploy -c docker-stack.yml prom`

Status:
`docker stack ps prom`

View services:
`docker service ls`

View Logs:
`docker service logs prom_<service name>`

Kill stack:
`docker stack rm prom`



Prometheus: http://localhost:9090  
Alertmanager: http://localhost:9093  
Grafana: http://localhost:3000  
- User: admin
- Pass: admin  

YACE: http://localhost:5000/metrics  
WebMetrics: http://localhost:9080/metrics  



