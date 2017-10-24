
# creamos despliegue
kubectl apply -f despliegue.yml

# estatus
kubectl rollout status deploy/escalar

# recoger
kubectl get deployments 

# mostrar
kubectl get all -l app=escalar

# crear servicio
kubectl apply -f servicio.yml

# estatus
kubectl get svc

# aplicamos canary-release
kubectl apply -f despliegue-canary.yml

# comprobamos
kubectl rollout status deploy/escalar-canary

# borramos canary
kubectl delete -f despliegue-canary.yml

# aplicamos final
kubectl apply -f despliegue-fin.yml

# status
kubectl rollout status deploy/escalar


