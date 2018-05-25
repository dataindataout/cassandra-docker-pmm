# cassandra-docker-pmm
Dockerfile with Cassandra and pmm-client

Best to start these separately:

`docker-compose up -d pmm-data pmm-server`

Then the seeds:

`docker-compose up -d DC1C1 DC1C2 DC2C1 DC2C2`

On the Cassandra nodes:

`/usr/local/bin/configure-pmm-client.sh`

In Grafana, choose the Advanced Data Exploration tab from the upper left.

Import a good dashboard into Grafana from here:

https://github.com/fipar/docker-cassandra-prometheus/blob/master/cassandra_rev3.json