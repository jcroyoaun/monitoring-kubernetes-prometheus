# Dashboard de Kubernetes 
El dashboard de kubernetes es una interfas web. Se puede utilizar para ver estadisticas de las aplicaciones corriendo en nuestro cluster, asi como para crear o modificar recursos de Kubernetes individuales


## Configuracion
* Deployeamos el Dashboard :

`kubectl apply -f https://raw.githubusercontent.com/kubernetes/dashboard/v2.0.0/aio/deploy/recommended.yaml`

* Corremos :

`kubectl apply -f dashboard-adminuser.yml`

* Corremos lo siguiente para acceder al UI del dashboard : 

`kubectl proxy`

Debe aparecer en : http://localhost:8001/api/v1/namespaces/kubernetes-dashboard/services/https:kubernetes-dashboard:/proxy/

* Obtenemos un token (password) corriendo el siguiente comando y copiando el token ** Asegurate de no perderlo ** :

`kubectl -n kubernetes-dashboard get secret $(kubectl -n kubernetes-dashboard get sa/admin-user -o jsonpath="{.secrets[0].name}") -o go-template="{{.data.token | base64decode}}"`

* Paste the token into the login screen and you can then sign in to the dashboard.


Para crear un nuevo recurso para el dashboard :
presionamos + y luego subimos el archivo llamado newDeploy.yml.

Referencias : 

https://kubernetes.io/docs/tasks/access-application-cluster/web-ui-dashboard/#deploying-the-dashboard-ui
https://github.com/kubernetes/dashboard/
