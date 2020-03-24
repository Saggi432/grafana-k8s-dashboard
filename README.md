# grafana-k8s-dashboard
This is an alternative dashboard option from https://github.com/grafana/kubernetes-app, if you do not need not want to install the app and just use the dashboards. Although you may lose few panels.

The grafana app seems to have few issues while working on k8s cluster in cloud env atleast when i tried. 

- The endpoint it refers to the node exporters are changed.
- The auth works for TLS/Basic not for webhook which we dont have for the cloud k8s deployment like gcloud..etc;
- The cluster config is not able to add any more clusters as the UI seems to be broken.
 - I had few issues rendering the panels


However these dashboards capture most of the information an ops person needs to monitor the cluster at a very high level. So i worked on the dashboard source code alone by making changes to the datasources, variables so that you can use these dashboards if you are running a grafana instance on your cloud environment.

Pre-requisites:
--------------
Install  prometheus operator or just prometheus which includes node-exporter so that you need those metrics.
Configure the prometheus datasource on your grafana instance.
