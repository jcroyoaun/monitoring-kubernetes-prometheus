# monitoring-kubernetes-prometheus
Este repositorio contiene los archivos de configuracion y los pasos para monitorear un cluster de Kubernetes usando Kubernetes dashboard, Prometheus y Grafana

# Instalacion de dependencias
https://kind.sigs.k8s.io/docs/user/quick-start/#installation
https://docs.docker.com/engine/install/

# Estructura del proyecto
El proyecto completo está dividido de la siguiente manera :

* Introducción a creación de clusters
* Creando un deployment
* Deployeando el Kubernetes Dashboard (Web-ui)
* Usando prometheus
* Usando dashboards de grafana


# Pasos para crear el cluster
* Paso 1. creamos un cluster usando :

`kind create cluster`

* Paso 2. Checamos el cluster

`kind get clusters`

* Paso 3. Obtenemos info del cluster

`kubectl cluster-info`

* Paso 4. Checamos los nodos..

`kubectl get nodes`

* Paso 5. para checar la informacion completa del cluster

`kubectl get all -A`
