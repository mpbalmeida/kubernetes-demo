    kubectl create -f local-volumes.yaml     
    kubectl create -f ghost-deployment.yaml
    kubectl autoscale deployment wordpress --cpu-percent=50 --min=1 --max=5