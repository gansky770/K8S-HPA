HPA - Exercise 
---------------

### Step 01
    
- Create deployment and autoscale by number of request in the last 30 seconds
  Write yourself the yaml files (practice) - 
   - Namespace
   - Deployment
   - Service
   - HPA

### Step 02

- Install Prometheus in your cluster ( custom metrics )
- Copnfigure Metrics

### Step 03

- Add Prometheus HPA query based upon request. 
  (you can test it with curl -v http://<ip>:port
	 
```
# Prometheus query:
sum(rate(http_server_requests_seconds_count[1m])
```

### Pre set
 - install [helm]  curl -L https://raw.githubusercontent.com/helm/helm/master/scripts/get-helm-3 | bash
 - get repo for prometheus   helm repo add prometheus-community https://prometheus-community.github.io/helm-charts
   helm repo update
 - install adapter helm install [RELEASE_NAME] prometheus-community/prometheus-adapter
   - example (https://github.com/luxas/kubeadm-workshop)
 - 