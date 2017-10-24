
# desplegamos la bbdd
kubectl apply -f despliegue-mongo.yml

# creamos un servicio interno para mongo
kubectl apply -f servicio-mongo.yml

# desplegamos la aplicacion
kubectl apply -f despliegue.yml

# creamos un servicio externo
kubectl apply -f servicio.yml

# esperamos
kubectl get all

# borramos y recreamos la bbdd
kubectl delete -f despliegue-mongo.yml && kubectl apply -f despliegue-mongo.yml



