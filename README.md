# Dockers-ELK


Run the latest version of the ELK (Elasticsearch, Logstash, Kibana) stack with Docker and Docker Compose.

It will give you the ability to analyze any data set by using the searching/aggregation capabilities of Elasticsearch
and the visualization power of Kibana.

Based on the official Docker images:

* [elasticsearch](https://github.com/elastic/elasticsearch-docker)
* [logstash](https://github.com/elastic/logstash-docker)
* [kibana](https://github.com/elastic/kibana-docker)


# How to setup 

 1.Clone this repository


2. Start the ELK stack using `docker-compose`:

```console
$ docker-compose up
```
# OR

You can also choose to run it in background (detached mode):

```console
$ docker-compose up -d


Give Kibana a few seconds to initialize, then access the Kibana web UI by hitting
[http://localhost:5601](http://localhost:5601) with a web browser.

By default, the stack exposes the following ports:
* 5000: Logstash TCP input.
* 9200: Elasticsearch HTTP
* 9300: Elasticsearch TCP transport
* 5601: Kibana


%{IP:client_ip} %{USER:ident} %{USER:auth} \[%{HTTPDATE:apache_timestamp}\] %{GREEDYDATA:url} \"%{WORD:method} %{GREEDYDATA:request_page} HTTP/%{NUMBER:http_version}\" %{NUMBER:server_response:int} %{NUMBER:bytes:int} %{QS:referer} %{GREEDYDATA:miss/hit} %{NUMBER:microsecond:int} %{NUMBER:second:float}

.es(q=server_response:200).label(200), .es(q=server_response:301).label(301), .es(q=server_response:302).label(302), .es(q=server_response:304).label(304), .es(q=server_response:404).label(404), .es(q=server_response:403).label(403), .es(q=server_response:429).label(429), .es(q=server_response:499).label(499), .es(q=server_response:500).label(500), .es(q=server_response:503).label(503)
