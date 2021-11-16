# How To

* Crear el pod mediante el fichero pod.yaml:
```console
kubectl create -f pod.yaml
```

# Questions

## 1. Crea un pod de forma declarativa.

1.1. ¿Cómo puedo obtener las últimas 10 líneas de la salida estándar (logs
generados por la aplicación)?

```console
kubectl logs -f --tail 10 nginx-hw02
```
* (NOTA: Mirar imagen "ex1.1.png")

1.2. ¿Cómo podría obtener la IP interna del pod? Aporta capturas para indicar
el proceso que seguirías.
```console
kubectl get pods -o wide
```
* (NOTA: Mirar imagen "ex1.2.png")

1.3. ¿Qué comando utilizarías para entrar dentro del pod?
```console
kubectl port-forward nginx-hw02 8080:80  
```
* (NOTA: Mirar imagen "ex1.3.png")

1.4. Necesitas visualizar el contenido que expone NGINX, ¿qué acciones
debes llevar a cabo?
  * http://localhost:8080/

* (NOTA: Mirar imagen "ex1.4.png")

1.5. Indica la calidad de servicio (QoS) establecida en el pod que acabas de
crear. ¿Qué lo has mirado?
```console
kubectl get pod nginx-hw02 --output=yaml
```
* Guaranteed
  
* (NOTA: Mirar imagen "ex1.5.png")