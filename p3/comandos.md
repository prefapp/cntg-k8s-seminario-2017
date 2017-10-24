
# creamos despliegue
kubectl apply -f despliegue.yml

# estatus
kubectl rollout status deploy/escalar

# recoger
kubectl get deployments 

# mostrar
kubectl get all -l app=escalar

# exponer puerto para mostrar
kubectl expose deploy/escalar --type=NodePort && kubectl get svc

# editar
kubectl edit deploy/escalar 

# estatus
kubectl rollout status deploy/escalar
