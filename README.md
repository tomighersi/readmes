# Virtuales

Proyecto de Aprendizaje para la materia Ingenieria de Software llevado a cabo con Python.

## Instalacion y Ejecucion

1. Clonar Repositorio:
```
git clone https://github.com/matiasluceroitec/virtuales.git
cd virtuales
```
2. Crear Entorno Virtual y Activarlo:

`Linux:`
```
python3 -m venv env
source env/bin/activate
```
`Windows:`
```
python -m venv env
env\Scripts\activate
```
3. Instalar Dependencias:
```
pip install -r requirements.txt
```
4. Acceder a la carpeta de nuestro proyecto:
```
cd itec2025
```
5. Ejecutar el Programa:
```
python manage.py runserver
```

## Estructura de Carpetas

- `itec2025/` (Carpeta de Proyecto)
   - itec2025/ (Aplicacion principal)
     - __pycache__/
     - __init.py__
     - asgi.py
     - context_processors.py (Funciones creadas para tenerlas disponibles en cualquier template, revisar settings.py)
     - settings.py (Diferentes configuraciones de nuestro proyecto)
     - urls.py (Donde se define el enrutado principal)
     - wsgi.py
   - home/ (Aplicacion referente a home)
   - products/ (Aplicacion referente a products)
     - repositories/ (Es para trabajar por capas y no cargar toda la logica en views. Este tiene funciones, clases que interactuan con la base de datos. Leen y escriben modelos)
     - services/ (Tambien para trabajar por capas. Este contiene logica para validaciones, calculos, etc. Usa funciones del repositorio pero no interactua con la bd)
     - migrations/
     - templates/ (Carpeta donde estan los templates 'html' dependiendo la ruta)
     - __init.py__
     - admin.py (Aca se define lo que puede realizar un admin desde la interfaz de admin que nos da django)
     - apps.py
     - models.py (Es donde creamos los modelos)
     - tests.py
     - urls.py (Define el enrutado relacionado a nuestra app)
     - views.py (Donde realizamos la logica. Creando funciones, clases, etc. para poder mostrar algo)
   - db.sqlite3 (Archivo de base de datos, actualizada al hacer un migrate)
   - manage.py (Archivo py para realizar comandos de nuestro proyecto)
