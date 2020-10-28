# rancher-monitoring-v2-demo

## Demo resource for custom metrics configuration of ServiceMonitors and PodMonitors.
create a namespace example

deploy the following files to the namespace

  example-app-service.yaml

  example-app-service-monitor.yaml

  example-app-deployment.yaml

  example-app-pod-monitor.yaml

The following new target should show in Prometheus → Status → Targets:

  example/example-app-pod-monitor

  example/example-app-service-monitor
  
scale up/down the deployment example-app

 the number of elements of the target increases/decreases reflecting the changing of the number of pods
 
 
## Configure Alert Manager config to set the notifiers. 
### Edit the secret alertmanager-rancher-monitoring-alertmanager in the namespace cattle-monitoring-system using the dashboard
  webhook for testing purpose for free: https://webhook.site 
  
### Configure additional alert by creating a new CRD. 
 ”kubectl create -f alert.yml”

 Validate additional alert is configured and fired
 
 Verify notification is received: the alert alert-to-webhook should go to the webhook website, the rest should go to Slack  

## Configure additional alerts and group them using the sample below:
 ”kubectl create -f alert.yml”
 
  Validate additional alert is configured and fired. Verify the alerts are grouped correctly in the alert manager browser console 
  
  Verify notification is received

## additional info RBAC

k get clusterrole | grep -i grafa


k get clusterrole | grep -i moni



# rancher-logging-v2-demo

install efk first before logging demo
