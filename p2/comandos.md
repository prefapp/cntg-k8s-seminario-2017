kubectl apply -f pod.yml

kubectl expose po/mi-nginx --type=NodePort

kubectl get svc
