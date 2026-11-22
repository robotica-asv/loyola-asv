# 🚤 ASV Loyola

Proyecto de desarrollo de un **Autonomous Surface Vehicle (ASV)** para participar en la competición [**Njord**](https://www.njordchallenge.com/).

El proyecto utiliza **ROS 2 Jazzy** y **Docker** para proporcionar un entorno de desarrollo común a todos los integrantes del equipo.

## 🎯 Objetivo

Desarrollar una plataforma ASV modular basada en ROS 2 que permita integrar simulación, control, comunicaciones y futuros sistemas de navegación autónoma.

---

## 📂 Estructura del repositorio

```text
.
├── README.md
├── docker
│   ├── Dockerfile
│   └── compose.yaml
├── docs
│   └── lanzamiento_asv.pdf
├── sim
└── src
    ├── asv_bringup
    ├── asv_comms
    ├── asv_control
    └── asv_description
```

### Paquetes ROS 2

| Paquete | Descripción |
|----------|------------|
| asv_bringup | Lanzamiento y configuración del sistema |
| asv_comms | Comunicaciones y arquitectura ROS 2 |
| asv_control | Control y navegación |
| asv_description | Descripción y simulación del ASV |

---

## ⚡ Instalación

### 1. Clonar el repositorio

```bash
git clone https://github.com/robotica-asv/loyola-asv.git
cd loyola-asv
```

### 2. Construir la imagen Docker

```bash
cd docker
docker compose build
```

### 3. Levantar el contenedor

```bash
docker compose up -d
```

### 4. Entrar al contenedor

```bash
docker exec -it asv-dev bash
```

---

## 🤖 Comprobar ROS 2

Dentro del contenedor ejecutar:

```bash
ros2 --version
```

También puedes comprobar la distribución instalada:

```bash
echo $ROS_DISTRO
```

Resultado esperado:

```text
jazzy
```

Si ambos comandos funcionan correctamente, el entorno está listo para desarrollar.

---

## 📚 Documentación

La documentación del proyecto se encuentra en:

```text
docs/
```

## 🌿 Flujo de trabajo Git

Antes de comenzar:

```bash
git pull
```

Guardar cambios:

```bash
git add .
git commit -m "Descripción de cambios"
git push
```

Crear una nueva funcionalidad:

```bash
git checkout -b feature/nueva-funcionalidad
```