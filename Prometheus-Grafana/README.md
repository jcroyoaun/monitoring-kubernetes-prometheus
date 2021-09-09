# Ejemplo de kube-state-metrics con Grafana

* Corremos el siguiente comando para crear un espacio de monitoreo (namespace)

`kubectl create namespace monitoring`

* Corremos lo siguiente para tener los recursos kube-state-metrics, Grafana y Prometheus en el lugar apropiado :
`kubectl create -f ./ -R` 

* Checamos NODEIP usando :
`kubectl get nodes --selector=kubernetes.io/role!=master -o jsonpath={.items[*].status.addresses[?\(@.type==\"InternalIP\"\)].address}`

* Entramos http://[NODEIP]:30000 para acceder a Prometheus

* Aqui podemos dar click en Graph, seleccionar una metrica del menu drop down , luego presionamos el boton ejecutar. Se puede cambiar entre Graph view y Console view.


NOTA: El archivo yml para las metricas puede ser modificado.

# Para remover recursos
Para remover los recursos de monitoreo podemos correr :

`kubectl delete -f ./ -R`


