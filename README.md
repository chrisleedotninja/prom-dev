# Config
Update Alertmanager config with a valid Slack `api_url`




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


## Configure YACE
Update YACE env.list file with valid AWS creds:
```
AWS_ACCESS_KEY_ID=KEYHERENOQUOTES
AWS_SECRET_ACCESS_KEY=SECRETACCESSKEYHERENOQUOTES
AWS_SESSION_TOKEN=AWSSESSIONTOKENHEREWITHNOQUOTES
```

## Configure pg_exporter
pg_exporter has the default queries turned off, so it will not pull postgres server
stats. Use only to test your custom queries by adding them to queries.yaml

Update pg_exporter env.list file with valid DB creds
```
DATA_SOURCE_URI=DATABASEHOST/tablename
DATA_SOURCE_USER=DBUSER
DATA_SOURCE_PASS=DBUSERPASSWORD
```

## URLS
Prometheus: http://localhost:9090  
Alertmanager: http://localhost:9093  
Grafana: http://localhost:3000  
- User: admin
- Pass: admin  

YACE: http://localhost:5000/metrics  
pg_exporter: http://localhost:9187/metrics  
WebMetrics: http://localhost:9080/metrics  



