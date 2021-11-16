# How To

* Crear el pod mediante el fichero rs.yaml:
```console
kubectl create -f rs.yaml
```

# Questions

## 2. Crear un objeto de tipo replicaSet a partir del objeto anterior

2.1 ¿Cúal sería el comando que utilizarías para escalar el número de replicas a
10?

```console
kubectl scale --replicas=10 rs nginx-hw02
```

2.2. Si necesito tener una replica en cada uno de los nodos de Kubernetes,
¿qué objeto se adaptaría mejor? (No es necesario adjuntar el objeto)

  * El objeto DaemonSet se adaptaría mejor que un ReplicaSet debido a que asegura que emplazará al menos 1 pod en cada uno de los nodos.