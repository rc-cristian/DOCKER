# 📌 Informe de práctica: Uso de Docker y contenedores

**Autor:** Cristian Dario Rojas

**Base:** Videos:  
- DOCKER De NOVATO a PRO! (Curso completo) — YouTube: https://youtu.be/CV_Uf3Dq-EU  
- Aprende Docker ahora! curso completo gratis desde cero — YouTube: https://youtu.be/4Dko5W96WHg

---

<img src="https://media2.dev.to/dynamic/image/width=1000,height=420,fit=cover,gravity=auto,format=auto/https%3A%2F%2Fdev-to-uploads.s3.amazonaws.com%2Fuploads%2Farticles%2Fxi0h4am3e43vrtead7fy.png" width="590"/>

---
## 📝 Resumen - Video 1: DOCKER De NOVATO a PRO!

**✅ Contenido principal (resumen experto):**
- Introducción a qué es Docker y para qué se usan contenedores.  
- Diferencias entre contenedores e imágenes; imágenes inmutables y contenedores efímeros.  
- Flujo básico: escribir un `Dockerfile`, construir una imagen (`docker build`), y ejecutar contenedores (`docker run`).  
- Comandos esenciales: `docker ps`, `docker images`, `docker rm`, `docker rmi`, `docker logs`, `docker exec`.  
- Buenas prácticas: usar `.dockerignore`, reducir el tamaño de la imagen, usar usuarios no-root, organizar capas para caché eficiente.  

---
## 📝 Resumen - Video 2: Aprende Docker ahora! (curso desde cero)

**✅ Contenido principal (resumen experto):**
- Instalación y configuración básica de Docker (Windows/Mac/Linux) y uso de Docker Desktop.  
- Uso de Docker Compose para orquestar múltiples servicios (por ejemplo app + base de datos).  
- Volúmenes para persistencia de datos y mapeo de puertos para exponer servicios.  
- Tips de debugging: ver logs, conectar a un shell dentro del contenedor (`docker exec -it <container> /bin/sh`).  
- Ejemplos prácticos: contenerizar una app simple (web API) y levantarla con `docker-compose up`.

---
## 📚 Reflexiones personales (ventajas, desafíos, uso práctico)

**✅ Ventajas**
- Reproducibilidad: el entorno se define como código (Dockerfile), lo que evita el clásico "en mi máquina funciona".  
- Ligereza frente a VMs: los contenedores comparten kernel y arrancan muy rápido.  
- Integración con CI/CD: imágenes versionables facilitan pipelines de despliegue.

**✅ Desafíos**
- Seguridad y mantenimiento: las imágenes base deben mantenerse actualizadas para evitar vulnerabilidades.  
- Tamaño de imágenes y eficiencia: escribir Dockerfiles optimizados es una habilidad necesaria.  
- Entornos de Windows/mac vs Linux: algunos comportamientos de montaje y permisos difieren.

**✅ Uso práctico**
- Desarrollo local de microservicios, entornos de pruebas, despliegues en servidores o en Kubernetes.  
- Facilita la colaboración en equipos: todos usan la misma imagen/entorno.

---
## 🚨 Mini-proyecto práctico: Flask simple en Docker

Estructura del proyecto creada en `/mnt/data/mi-app-docker/`:

```
mi-app-docker/
├── app/
│   ├── main.py
│   └── requirements.txt
├── Dockerfile
└── docker-compose.yml
```

Archivo ya generado:
- `app/main.py` — aplicación Flask mínima.
- `app/requirements.txt` — dependencias.
- `Dockerfile` — para construir la imagen.
- `docker-compose.yml` — para orquestar el servicio.

---
###🔔 Instrucciones para ejecutar localmente

1. Clona o copia la carpeta `mi-app-docker` a tu máquina
2. Abre una terminal en la carpeta raíz (`mi-app-docker`) y ejecuta:

```bash
docker-compose build
docker-compose up -d
```

3. Abre tu navegador en `http://localhost:5000` — deberías ver: _"¡Hola desde Docker y Flask!"_  
4. Para ver logs:
```bash
docker-compose logs -f
```
5. Para detener y remover contenedores:
```bash
docker-compose down
```

---
## 💹 Recursos adicionales consultados

- Documentación oficial de Docker: https://docs.docker.com/  
- Docker Compose: https://docs.docker.com/compose/  
- Curso (YouTube): DOCKER De NOVATO a PRO! — https://youtu.be/CV_Uf3Dq-EU  
- Curso (YouTube): Aprende Docker ahora! — https://youtu.be/4Dko5W96WHg  
- Guía práctica en DigitalOcean: https://www.digitalocean.com/community/tutorials/how-to-use-docker-compose  

---

