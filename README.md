# efk-docker
EFK Stack in Docker


This is a work in progress complete stack of monitoring and logging running on top of Docker.

The components are 

- Logging: EFK (Elasticsearch, Fluentd, Kibana)
- Performance metrics: Graphite, Grafana
- Monitoring: Sensu

To run, execute: docker-compose -f logging.yml -f performance.yml -f monitoring.yml up
