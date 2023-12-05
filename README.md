# labs-k8s
# labs-k8s

## Configurar kubeconfig
```
export KUBECONFIG=$(pwd)/k8s.yml
```
***
## Crear pod por linea de comando
```
kubectl run  podtest --image=nginx:alpine
```
***
## cambiar contexto
```
kubectl config set-context --current --namespace=<insert-namespace-name-here>
```
***
## Obtener todos los pods
```
kubectl get pods
```
***
## Obtener Yaml
```
kubectl get pod podtest -o yaml
```
***
## Enviar a Archivo 
```
kubectl get pod podtest -o yaml >> pod.yml
```
***
## Generar error
```
kubectl run  podtest1 --image=nginx:alpine2de
```
***
## Describir un pod
```
kubectl describe pod [nombre-pod]
```
***
## Ver todos los recursos de kubernetes que podemos usar
```
kubectl api-resources
```
***
## Como ver los Logs
```
kubectl logs -f [nombre-pod]
```
***
## Eliminar pods
```
kubectl delete pod [nombre-pod]
```
***
## Eliminar pods
```
kubectl delete pod [nombre-pod]
```
***
## ngresar a los contenedores
```
kubectl exec -it podtest -- sh

cd /usr/share/nginx/html"
echo "Modificando el index dentro del contenedor" > index.html
```
***
## Instalar Curl
```
apk add curl
```
***
## Instalar Curl
```
apk add curl
```
***
## Como hacer un manifiesto

***
## Realizar busquedas con filtros segun labels
```
kubectl get pods -l env=dev
```
***
## Problemas de trabajar con Pods directamente
```
kubectl get pods -l env=dev
```
## Crear Replicas sets
## Explicar OwnerReferences




kubectl rollout status deployments

Crear Deployment dep.yaml

Explicar Owner References

Describir un Deployment

Historico y Revisiones
Hacer get rs
kubectl rollout history deployment
kubectl rollout undo deployment nombre --to-revision=3

Que es un servicio 
Crear un servicio -> service.yaml
Describir Servicio
Mostrar Endpoints
Get endpoints

Explicar ClusterIP
Explicar NodePort

Aplicar nodeport
demostrar nodeport

Explicar Balanceador de Carga


## Actualizar sts
kubectl rollout status statefulset/<nombre-del-StatefulSet>