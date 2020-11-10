# rancher-monitoring-v2-demo

## create a namespace example
kubectl create ns example

The following new target should show in Prometheus → Status → Targets:

  example/example-app-pod-monitor

  example/example-app-service-monitor
 
## Configure Alert Manager config to set the notifiers. 
### Edit the secret alertmanager-rancher-monitoring-alertmanager in the namespace cattle-monitoring-system using the dashboard
  webhook for testing purpose for free: https://webhook.site 

# rancher-logging-v2-demo
create a nginx workload in default ns.
install efk first before logging demo.
