# Logging with EFK in Kubernetes

This workshop shows how to install the EFK (Elasticsearch, Fluentd and Kibana) stack in Kubernetes using Helm, to get application logs.

<img src="https://github.com/HoussemDellai/EFK-Kubernetes/blob/master/images/efk-lightboard.jpg?raw=true" width="80%">

And these are the amin commands used to install EFK:

$ helm install elasticsearch stable/elasticsearch 
wait for few minutes..

$ kubectl apply -f .\fluentd-daemonset-elasticsearch.yaml

$ helm install kibana stable/kibana -f kibana-values.yaml

$ kubectl apply -f .\counter.yaml

Open Kibana dashboard.