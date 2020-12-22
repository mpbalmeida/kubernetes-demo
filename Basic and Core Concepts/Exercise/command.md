    kubectl apply -f ./deployment.yaml
    kubectl expose deployment mongo-deployment --type=LoadBalancer --port=27017 --target-port=27017 --name mongo-load-balancer
    minikube service mongo-load-balancer --url
    
     
    kubectl describe services mongo-load-balancer