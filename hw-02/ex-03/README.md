# Questions

## 3.Crea un objeto de tipo service para exponer la aplicación del ejercicio anterior

3.1. Exponiendo el servicio hacia el exterior (crea service1.yaml)

Este caso de uso no se puede implementar con Minikube, se debe utilizar un tipo de servicio LoadBalancer el cual únicamente se puede utilizar mediante plataformas Cloud debido a que expone el servicio al exterior mediante una IP Pública.


3.2. De forma interna, sin acceso desde el exterior (crea service2.yaml)

```console
kubectl create -f rs.yaml
kubectl create -f service2.yaml
```
http://localhost:8080/

3.3. Abriendo un puerto especifico de la VM (crea service3.yaml)

```console
kubectl create -f rs.yaml
kubectl create -f service3.yaml

minikube service nginx-hw02 --url
```
http://192.168.64.2:30000