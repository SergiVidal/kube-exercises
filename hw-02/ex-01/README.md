# How To

* Crear el pod mediante el fichero pod.yaml:
```console
kubectl create -f pod.yaml
```

# Questions

## 1. Crea un pod de forma declarativa.

* ¿Cómo puedo obtener las últimas 10 líneas de la salida estándar (logs
generados por la aplicación)?
  * kubectl logs -f --tail 10 nginx-hw02
  * NOTA: Mirar imagen "ex1.1.png"

* ¿Cómo podría obtener la IP interna del pod? Aporta capturas para indicar
el proceso que seguirías.
  * kubectl get pods -o wide
  * NOTA: Mirar imagen "ex1.2.png"

* ¿Qué comando utilizarías para entrar dentro del pod?
  * kubectl port-forward nginx-hw02 8080:80  
  * NOTA: Mirar imagen "ex1.3.png"

* Necesitas visualizar el contenido que expone NGINX, ¿qué acciones
debes llevar a cabo?
  * http://localhost:8080/
  * NOTA: Mirar imagen "ex1.4.png"

* Indica la calidad de servicio (QoS) establecida en el pod que acabas de
crear. ¿Qué lo has mirado?
  * k get pod nginx-hw02 --output=yaml
  * Guaranteed
  * NOTA: Mirar imagen "ex1.5.png"


## 2. Crear un objeto de tipo replicaSet a partir del objeto anterior.


