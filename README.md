# 🎮 Platformer

![Godot](https://img.shields.io/badge/Godot_4-478CBF?logo=godotengine&logoColor=white)
![GDScript](https://img.shields.io/badge/GDScript-478CBF?logo=godotengine&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white)
![Django](https://img.shields.io/badge/Django-092E20?logo=django&logoColor=white)
![Estado](https://img.shields.io/badge/Estado-Completado-blue)

# 📖 Índice

1. [Descripción del Proyecto](#descripción-del-proyecto)  
2. [Estado del Proyecto](#estado-del-proyecto)  
3. [Demostración de funciones](#-demostración-de-funciones)  
4. [Acceso al Proyecto](#-acceso-al-proyecto)
5. [Tecnologías utilizadas](#%EF%B8%8F-tecnologías-utilizadas)
6. [Autor](#autor)

## Descripción del Proyecto

Este proyecto consiste en un juego de plataformas 2D desarrollado como práctica académica. Su objetivo principal es aplicar la lógica de Godot Engine combinada con una arquitectura de servidor backend. El juego cuenta con mecánicas de plataformeo clásicas, enemigos básicos y recolección de *power-ups*, destacando por la integración de un sistema de registro asíncrono para eventos del jugador.

## 📌 Estado del Proyecto

Este proyecto se encuentra en estado **Completado**, sirviendo como demostración de integración Cliente-Servidor y desarrollo de lógicas base de videojuegos.

## 🎯 Demostración de funciones

- ✅ **Mecánicas Clásicas:** Controles de movimiento, saltos y físicas adaptadas al entorno 2D.
- 👾 **Entorno Interactivo:** Generación de enemigos básicos y recolección de *power-ups* interactivos.
- 💀 **Rastreo de Muertes (Backend):** Sistema de persistencia asíncrono. Cada vez que el jugador muere, el cliente envía las coordenadas exactas al servidor Django. Al recargar la escena, el juego lee estos datos y posiciona una calavera en el mapa señalando el punto del fracaso anterior.
- 🧹 **Reinicio de Estados:** Endpoint dedicado en la API para resetear las marcas de muerte mediante peticiones POST.

## 🚀 Acceso al proyecto

### 🔧 Requisitos previos
- **Godot Engine** (versión 4.x).
- **Python 3.x** y **Django** instalados en el entorno local.

### 📦 Ejecución del Entorno
Para que el registro de muertes funcione correctamente, el servidor debe inicializarse siguiendo estos pasos:

1. Clona este repositorio: `git clone [TU_URL_AQUI]`
2. Abre la consola de comandos (CMD) y navega hasta la carpeta `server` donde se encuentra **GodotApi**.
3. Levanta el servidor local ejecutando el siguiente comando: 
   `python manage.py runserver 0.0.0.0:8000`
4. Abre el proyecto del cliente gráfico utilizando Godot Engine.
5. Ejecuta la escena principal (`F5`) para iniciar el juego y conectar con el servidor.

### 🗑️ Limpiar el registro de muertes
Para borrar todas las marcas del mapa desde el CMD, debes enviar una petición POST al localhost apuntando a la dirección de limpieza:
`http://localhost:8000/limpiar_coordenadas`

## 🛠️ Tecnologías utilizadas

- **Godot Engine & GDScript:** Motor y lenguaje nativo para la lógica del cliente y físicas 2D.
- **Python & Django:** Creación de la API y servidor para el registro de eventos y persistencia de datos.

## Autor

Desarrollado por Kevin Cancelo.
