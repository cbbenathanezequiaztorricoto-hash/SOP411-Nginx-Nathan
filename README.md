# 🐳 SOP411 - Administración, Respaldo y Migración de Servidor Docker

Este repositorio contiene los artefactos, respaldos y documentación técnica correspondientes al **Hito 4 (Evaluación Práctica)** de la materia **Sistemas Operativos** de la Universidad Franz Tamayo.

## 📌 Objetivo del Proyecto
Implementar, administrar y respaldar un servidor web **Nginx** desplegado en un contenedor **Docker** sobre una máquina virtual **Alpine Linux**, preparando el servicio para una migración futura a otra infraestructura.

## 🛠️ Tecnologías Utilizadas
* **Alpine Linux** (Sistema Operativo base en la VM)
* **Docker** (Motor de contenedores)
* **Nginx** (Servidor Web)
* **WinSCP** (Transferencia de archivos vía SFTP)
* **Tailscale** (Red VPN para acceso remoto)
* **ActivityWatch** (Registro de actividad para auditoría)

## 📂 Contenido del Repositorio
* `index.html` y `50x.html`: Código fuente del sitio web personalizado alojado en Nginx.
* `nginx-examen-nathan.tar`: Imagen de Docker empaquetada (respaldo completo del entorno operativo y del sitio web).

## 🚀 Guía de Restauración y Migración
Para desplegar este servidor web en una nueva máquina Linux, siga estos pasos:

1. **Cargar la imagen respaldada en el nuevo servidor:**
   ```bash
   docker load -i nginx-examen-nathan.tar
