    # run below commands under the kubernetes-demo/Advanced Kubernetes Usage/Volumes folder.
    kubectl delete -f ./mysql-deployment.yaml
    kubectl delete -f ./wordpress-deployment.yaml
    minikube stop
    minikube start
    kubectl create secret generic mysql-pass --from-literal=password=BetterWayToStoreAPassword
    kubectl apply -f ./mysql-deployment.yaml
    kubectl apply -f ./wordpress-deployment.yaml
    