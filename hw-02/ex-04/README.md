# How To

* Crear el service mediante el fichero service.yaml:

```console
kubectl create -f service.yaml
```

# Questions

## 4.Crear un objeto de tipo deployment

4.1. Despliega una nueva versión de tu nuevo servicio  mediante la técnica “recreate”

```console
kubectl create -f deployment1.yaml
```

4.2. Despliega una nueva versión haciendo “rollout deployment”

```console
kubectl create -f deployment2.yaml
```

4.3. Realiza un rollback a la versión generada previamente


```console
kubectl create -f deployment2.yaml

kubectl set image deployments.apps/nginx-hw02 nginx-hw02-ctr=nginx:1.19.3

kubectl rollout history deployment.v1.apps/nginx-hw02

kubectl rollout undo deployment.v1.apps/nginx-hw02 --to-revision=1
```

* (NOTA: Mirar imagen "ex4.3.png")