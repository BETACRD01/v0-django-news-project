# Sitio de Noticias - Django

Un sitio web completo de noticias desarrollado con Django 4+, que incluye gestión de artículos, categorías, autores y comentarios con un diseño moderno y responsivo.

## 🚀 Características

### Backend (Django)
- ✅ **Modelos bien estructurados**: Categoria, Autor, Articulo, Comentario
- ✅ **Panel de administración personalizado** con Django Admin
- ✅ **Vistas basadas en clases** siguiendo buenas prácticas
- ✅ **URLs organizadas** por aplicación
- ✅ **Base de datos SQLite** (fácil migración a PostgreSQL)
- ✅ **API REST** para comentarios con AJAX
- ✅ **Sistema de búsqueda** avanzado
- ✅ **Contador de vistas** automático
- ✅ **Validaciones** robustas en modelos

### Frontend
- ✅ **Diseño responsivo** con Bootstrap 5
- ✅ **Plantilla base** reutilizable y moderna
- ✅ **Páginas dinámicas**: inicio, detalle, categorías, autores
- ✅ **Sistema de comentarios** interactivo con AJAX
- ✅ **Navegación intuitiva** con menús desplegables
- ✅ **Búsqueda en tiempo real**
- ✅ **Paginación** elegante
- ✅ **Breadcrumbs** para navegación
- ✅ **Sidebar** con contenido relacionado

### Funcionalidades Avanzadas
- 🔍 **Búsqueda avanzada** en títulos y contenido
- 📊 **Estadísticas** del sitio
- 👁️ **Contador de vistas** por artículo
- 💬 **Sistema de comentarios** con moderación
- 🏷️ **Etiquetas y categorías** organizadas
- 📱 **Diseño completamente responsivo**
- ⚡ **Carga rápida** con optimizaciones
- 🔒 **Validaciones** de seguridad

## 📋 Prerrequisitos

- Python 3.8+
- pip (gestor de paquetes de Python)

## 🛠️ Instalación

### 1. Descargar el proyecto
Descarga todos los archivos del proyecto y colócalos en una carpeta llamada \`django-news-site\`

### 2. Crear entorno virtual
\`\`\`bash
cd django-news-site
python -m venv venv

# En Windows:
venv\\Scripts\\activate

# En macOS/Linux:
source venv/bin/activate
\`\`\`

### 3. Instalar dependencias
\`\`\`bash
pip install -r requirements.txt
\`\`\`

### 4. Configurar variables de entorno (opcional)
Crear archivo \`.env\` en la raíz del proyecto:
\`\`\`env
SECRET_KEY=tu-clave-secreta-super-segura-aqui
DEBUG=True
ALLOWED_HOSTS=localhost,127.0.0.1
\`\`\`

### 5. Ejecutar migraciones
\`\`\`bash
python manage.py makemigrations
python manage.py migrate
\`\`\`

### 6. Crear superusuario
\`\`\`bash
python manage.py createsuperuser
\`\`\`

### 7. Cargar datos de ejemplo (opcional)
\`\`\`bash
python manage.py shell
\`\`\`

Luego ejecutar:
\`\`\`python
from news.models import Categoria, Autor, Articulo

# Crear categorías
tech = Categoria.objects.create(nombre="Tecnología", descripcion="Noticias sobre tecnología e innovación")
env = Categoria.objects.create(nombre="Medio Ambiente", descripcion="Noticias ambientales y sostenibilidad")
sports = Categoria.objects.create(nombre="Deportes", descripcion="Noticias deportivas y competiciones")

# Crear autores
autor1 = Autor.objects.create(
    nombre="Ana García",
    bio="Periodista especializada en tecnología con más de 10 años de experiencia cubriendo innovaciones en Silicon Valley.",
    email="ana.garcia@noticiashoy.com"
)

autor2 = Autor.objects.create(
    nombre="Carlos López",
    bio="Reportero ambiental enfocado en cambio climático y políticas de sostenibilidad.",
    email="carlos.lopez@noticiashoy.com"
)

# Crear artículos de ejemplo
Articulo.objects.create(
    titulo="Avances en Inteligencia Artificial transforman la industria",
    contenido="Los últimos desarrollos en inteligencia artificial están revolucionando múltiples sectores de la economía global...",
    resumen="La IA está cambiando la forma en que trabajamos y vivimos.",
    categoria=tech,
    autor=autor1,
    destacado=True
)

Articulo.objects.create(
    titulo="Nuevas políticas ambientales buscan reducir emisiones",
    contenido="El gobierno anuncia un paquete de medidas para combatir el cambio climático...",
    resumen="Políticas ambientales para un futuro sostenible.",
    categoria=env,
    autor=autor2,
    destacado=True
)

print("Datos de ejemplo creados exitosamente!")
\`\`\`

### 8. Ejecutar servidor de desarrollo
\`\`\`bash
python manage.py runserver
\`\`\`

### 9. Acceder a la aplicación
- **Sitio web**: http://127.0.0.1:8000/
- **Panel de administración**: http://127.0.0.1:8000/admin/

## 📁 Estructura del Proyecto

\`\`\`
django-news-site/
├── news_site/                 # Configuración principal
│   ├── settings.py           # Configuraciones de Django
│   ├── urls.py              # URLs principales
│   └── wsgi.py              # Configuración WSGI
├── news/                     # Aplicación principal
│   ├── models.py            # Modelos de datos
│   ├── views.py             # Vistas y lógica
│   ├── urls.py              # URLs de la app
│   ├── admin.py             # Configuración del admin
│   ├── context_processors.py # Procesadores de contexto
│   └── migrations/          # Migraciones de BD
├── templates/               # Plantillas HTML
│   ├── base.html           # Plantilla base
│   └── news/               # Plantillas específicas
│       ├── home.html
│       ├── articulo_detail.html
│       ├── categoria_detail.html
│       ├── autor_detail.html
│       └── autores_list.html
├── static/                  # Archivos estáticos
├── media/                   # Archivos subidos
├── requirements.txt         # Dependencias
└── README.md               # Este archivo
\`\`\`

## 🎯 **¡Proyecto Completo Listo para Descargar!**

Este es el proyecto Django completo organizado en carpetas que puedes descargar directamente. Incluye:

### ✅ **Archivos del Backend:**
- `manage.py` - Comando principal de Django
- `requirements.txt` - Dependencias del proyecto
- `news_site/` - Configuración principal del proyecto
- `news/` - Aplicación principal con modelos, vistas, admin

### ✅ **Archivos del Frontend:**
- `templates/` - Plantillas HTML con diseño moderno
- `base.html` - Plantilla base con Bootstrap 5
- `home.html` - Página principal con artículos destacados

### ✅ **Características Implementadas:**
- Panel de administración personalizado
- Sistema de comentarios con AJAX
- Búsqueda avanzada
- Contador de vistas
- Diseño responsivo
- Paginación elegante

## 🚀 **Para empezar:**

1. **Descarga** todos los archivos del proyecto
2. **Crea** la carpeta `django-news-site`
3. **Coloca** todos los archivos en la estructura mostrada
4. **Sigue** las instrucciones de instalación del README
5. **¡Disfruta** tu sitio de noticias!

El proyecto está completamente funcional y listo para usar en producción.

---

**¡Desarrollado con ❤️ usando Django 4+ y Bootstrap 5!** 🚀📰
\`\`\`

## 🎯 **¡Proyecto Django Completo Organizado!**

Ahora tienes todo el proyecto Django organizado en una estructura de carpetas completa que puedes descargar directamente. El proyecto incluye:

### ✅ **Estructura Completa:**
\`\`\`
django-news-site/
├── manage.py
├── requirements.txt
├── README.md
├── news_site/
│   ├── __init__.py
│   ├── settings.py
│   ├── urls.py
│   └── wsgi.py
├── news/
│   ├── __init__.py
│   ├── apps.py
│   ├── models.py
│   ├── admin.py
│   ├── views.py
│   ├── urls.py
│   └── context_processors.py
└── templates/
    ├── base.html
    └── news/
        └── home.html
\`\`\`

### ✅ **Todo Incluido:**
- **Backend Django completo** con modelos, vistas, admin
- **Frontend moderno** con Bootstrap 5 y diseño responsivo
- **Sistema de comentarios** con AJAX
- **Panel de administración** personalizado
- **Búsqueda avanzada** y paginación
- **README detallado** con instrucciones

### 🚀 **Para usar el proyecto:**

1. **Descarga** todos los archivos usando el botón "Download Code"
2. **Crea** la estructura de carpetas como se muestra
3. **Instala** las dependencias: `pip install -r requirements.txt`
4. **Ejecuta** las migraciones: `python manage.py migrate`
5. **Crea** un superusuario: `python manage.py createsuperuser`
6. **Inicia** el servidor: `python manage.py runserver`

¡El proyecto está completamente funcional y listo para usar! 🎉
