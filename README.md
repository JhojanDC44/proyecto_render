# 📌 Proyecto Render

## 📝 Descripción
Este es un proyecto desarrollado en Django que ha sido configurado para ser desplegado en **Render**. Incluye una estructura modular con aplicaciones, bases de datos y una configuración optimizada para producción.

## 🚀 Tecnologías Utilizadas
- Python 3.x
- Django
- HTML, CSS, JavaScript
- PostgreSQL (opcional para producción)
- Render (para despliegue)
- Git & GitHub

## 📂 Estructura del Proyecto
```plaintext
proyecto_render/
│-- manage.py
│-- requirements.txt
│-- README.md
│-- .gitignore
│-- app/  # Aplicación principal
│   ├── migrations/
│   ├── static/
│   ├── templates/
│   ├── views.py
│   ├── urls.py
│   ├── models.py
│   ├── forms.py
│   ├── admin.py
│-- settings/  # Configuración modular
│   ├── base.py
│   ├── production.py
│   ├── development.py
```

## 🔧 Instalación y Configuración
1. **Clonar el repositorio**
   ```bash
   git clone https://github.com/JhojanDC44/proyecto_render.git
   cd proyecto_render
   ```

2. **Crear y activar un entorno virtual**
   ```bash
   python -m venv venv
   source venv/bin/activate  # En Mac/Linux
   venv\Scripts\activate  # En Windows
   ```

3. **Instalar dependencias**
   ```bash
   pip install -r requirements.txt
   ```

4. **Configurar variables de entorno**
   Crea un archivo `.env` y define tus variables necesarias:
   ```ini
   SECRET_KEY=tu_secreto
   DEBUG=True  # Cambiar a False en producción
   DATABASE_URL=postgres://usuario:password@localhost:5432/tu_bd
   ```

5. **Ejecutar migraciones y servidor local**
   ```bash
   python manage.py migrate
   python manage.py runserver
   ```
   Accede a `http://127.0.0.1:8000/`

## 🌍 Despliegue en Render
1. **Subir cambios a GitHub**
   ```bash
   git add .
   git commit -m "Inicialización del proyecto"
   git push origin master
   ```

2. **Configurar Render**
   - Ve a [Render.com](https://render.com/)
   - Crea un nuevo servicio web
   - Conéctalo con tu repositorio
   - Configura el comando de inicio:
     ```bash
     gunicorn settings.wsgi:application
     ```

3. **Agregar variables de entorno** en Render
   - `SECRET_KEY`
   - `DATABASE_URL`

4. **Finalizar el despliegue** y acceder a la URL generada 🚀

## ✨ Características
✅ Sistema de autenticación integrado<br>
✅ Panel de administración en `/admin/`<br>
✅ Rutas y vistas configuradas<br>
✅ Estilos con Bootstrap o Tailwind (según preferencia)<br>
✅ Configuración para producción y desarrollo

## 📌 Contribución
Si deseas contribuir:
1. Haz un fork del proyecto.
2. Crea una nueva rama: `git checkout -b feature-nueva`.
3. Realiza tus cambios y haz commit: `git commit -m "Añadir nueva funcionalidad"`.
4. Haz push a tu fork: `git push origin feature-nueva`.
5. Abre un **Pull Request**.

## 📄 Licencia
Este proyecto está bajo la **MIT License**.

---
🚀 *¡Gracias por visitar este repositorio!*
