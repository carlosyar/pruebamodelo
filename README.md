# modelomultimedia

# Clasificador de Imágenes con Flask 

Este proyecto utiliza Flask para crear una aplicación web que permite a los usuarios subir imágenes de vegetales y clasificarlas utilizando un modelo de aprendizaje automático entrenado con TensorFlow. El modelo predice la clase de una imagen entre varias opciones.

## Requisitos previos

Antes de comenzar, asegúrate de tener instalado lo siguiente:

- [Python](https://www.python.org/downloads/) (3.6 o superior)
- [Render](https://render.com/) (para desplegar la aplicación en la nube)

## Instalación

### 1. Producción en servidor local - preparación del entorno

Primero, crea un entorno virtual para evitar conflictos con otras librerías de Python. Para hacerlo, ejecuta los siguientes comandos:
```
python -m venv venv
venv\Scripts\activate
conda create -n appmulti
onda activate appmulti
conda install python=3.9.20
$   pip install -r requirements.txt
$   streamlit run app.py
```
Instalar librerias necesarias
```
pip install -r requirements.txt
```
Ejecutamos
```
python run app.py
```
### 2. Desplegue a Render

1. Crea una cuenta en Render
Si no tienes una cuenta en Render, crea una en Render.

2. Conecta tu repositorio de GitHub
   
3.Inicia sesión en tu cuenta de Render.
4.Haz clic en el botón "New" y selecciona "Web Service".
5.Selecciona "Connect with GitHub" y autoriza la conexión con tu cuenta de GitHub.
6.Selecciona el repositorio que contiene tu proyecto de Flask.

7. Configura el servicio de Render
Render detectará automáticamente que tu proyecto es una aplicación web. En la sección de configuración:

Branch: Selecciona la rama que quieres desplegar (por lo general, main o master).
Build Command: 
```
pip install -r requirements.txt 
```
Start Command: Usa el siguiente comando para iniciar la aplicación Flask:
```
gunicorn "app:crear_app()"
```
Haz clic en "Create Web Service". Render comenzará a construir y desplegar tu aplicación.

8. Acceder a tu aplicación desplegada
Una vez que Render haya terminado el despliegue, se podra acceder en el siguiente enlace: https://modelomultimedia.onrender.com/
