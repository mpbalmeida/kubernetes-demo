     # since the latest minikube doesn't enable metrics-server by default
    minikube addons enable metrics-server  
     
    kubectl apply -f ./wordpress-deployment.yaml
     
    kubectl autoscale deployment wordpress --cpu-percent=50 --min=1 --max=5

In other terminal
    kubectl run -i --tty load-generator --image=busybox --generator=run-pod/v1 /bin/sh
    
    while true; do wget -q -O- http://wordpress.default.svc.cluster.local; done