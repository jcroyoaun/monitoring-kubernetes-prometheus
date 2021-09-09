# Creando los deployments

* Analizamos el manifest yaml

`cat deployment.yml`

* Deployeamos el manifest

`kubectl apply -f deployment.yml`

* Checamos el deployment

`kubectl get deploy`

* Checamos los pods

`kubectl get pods`

* Creamos el servicio usando el service.yml

`kubectl apply -f service.yml`

* Checamos el servicio

`kubectl get svc`
