## [MPWAR] - Principios y herramientas de desarrollo: Entregable 2 – Kubernetes (Parte I)

[2 ptos] Crea un pod de forma declarativa con las siguientes especificaciones:

- Imagen: nginx
- Version: 1.19.4
- Label: app: nginx-server
- Limits
  CPU: 100 milicores
  Memoria: 256Mi
- Requests
  CPU: 100 milicores
  Memoria: 256Mi

```bash
apiVersion: v1
kind: Pod
metadata:
  name: nginx
  labels:
    app: nginx-server
spec:
  containers:
  - name: nginx
    image: nginx:1.19.4
    ports:
    - containerPort: 80
    resources:
      limits:
        cpu: "100"
        memory: 256Mi
      requests: 
        cpu: "100"
        memory: 128Mi
```

Realiza un despliegue en Kubernetes, y responde las siguientes preguntas:

# ¿Cómo puedo obtener las últimas 10 líneas de la salida estándar (logs generados por la aplicación)?
# ¿Cómo podría obtener la IP interna del pod? Aporta capturas para indicar el proceso que seguirías. ¿Qué comando utilizarías para entrar dentro del pod?
# Necesitas visualizar el contenido que expone NGINX, ¿qué acciones debes llevar a cabo?
# Indica la calidad de servicio (QoS) establecida en el pod que acabas de crear. ¿Qué lo has mirado?
