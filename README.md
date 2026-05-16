# Glamour Bisutería — Sistema de Inventario y Tienda Web

**SIGPROD · Sistema Integral de Gestión de Proyectos de Desarrollo de Software**
Unidades Tecnológicas de Santander · Desarrollo de Aplicaciones Empresariales · Grupo E192
TechSoft Solutions S.A.S. · Bucaramanga, Colombia · 2026

-----

## 👥 Equipo

|Integrante |Roles |
|------------------|-------------------------------------------------------------|
|**Marlón Gélvez** |Product Owner · Scrum Master · Desarrollador Frontend |
|**Jesús González**|Analista de Negocio · Diseñador UI/UX · Desarrollador Backend|

-----

## 📋 Descripción del Proyecto

Sistema web para **Glamour Bisutería**, empresa bucaramanguesa que necesitaba digitalizar su catálogo, gestionar pedidos y controlar inventario de forma centralizada. La solución es una aplicación web con tienda, carrito de compras, checkout, factura, panel cliente y panel administrador.

**Problema:** Glamour Bisutería gestionaba su inventario y ventas manualmente, sin trazabilidad ni control de stock en tiempo real.

**Solución:** Aplicación web con arquitectura API REST — frontend en HTML/CSS/JS (Sprint 1) y backend Python/Flask con JWT y base de datos (Sprint 2+).

-----

## 🚀 Demo en Producción

|Recurso |URL |
|-------------------------|-------------------------------------------------------------------------------------------|
|**Tienda Web (Sprint 1)**|[proyecto-production-079f.up.railway.app](https://proyecto-production-079f.up.railway.app/)|
|**Repositorio** |[github.com/jess-1304/proyecto](https://github.com/jess-1304/proyecto) |

-----

## 🛠️ Stack Tecnológico

|Capa |Sprint 1 |Sprint 2+ |
|------------------------|------------------------------|-----------------------------|
|**Frontend** |HTML5 · CSS3 · JavaScript puro|React + integración API REST |
|**Backend** |— (datos simulados en JS) |Python 3.x · Flask · API REST|
|**Base de Datos** |Objeto JS local (simulado) |MySQL / MongoDB Atlas |
|**Autenticación** |Simulada en JS por rol |JWT (JSON Web Token) real |
|**Documentación API** |— |Swagger / OpenAPI 3.0 |
|**Deploy** |Railway (sitio estático) |Render.com + Docker |
|**CI/CD** |GitHub Actions (push → deploy)|GitHub Actions completo |
|**Control de versiones**|Git + GitHub (ramas main/dev) |Git + GitHub |

-----

## 📦 Estado del Proyecto — Sprint 1 ✅ COMPLETADO

**Objetivo:** Frontend completo desplegado en producción con autenticación simulada, tienda, carrito, checkout, paneles cliente y admin.

### Funcionalidades implementadas

|Módulo |Estado |Descripción |
|-------------------|------------------|------------------------------------------------------------------------------------------|
|Vista Tienda |✅ Funcional |Grid de 15 productos con emoji, precio COP, categoría y badge de stock dinámico |
|Filtros y Búsqueda |✅ Funcional |Pastillas por categoría + búsqueda con debounce 300ms; intersección de filtros |
|Carrito de Compras |✅ Funcional |Panel lateral deslizable, control de cantidades, validación de stock, total en tiempo real|
|Checkout y Factura |✅ Funcional |Simulación visual de checkout + factura con número único (FAC-timestamp) + impresión PDF |
|Login y Registro |⚠️ Simulado en JS |Autenticación contra objeto DB local; redirección por rol (admin/cliente) |
|Panel Cliente |⚠️ Solo en sesión |Historial de pedidos, gráfico mensual, perfil editable durante la sesión activa |
|Panel Administrador|⚠️ Sin persistencia|Dashboard con KPIs, gestión de pedidos y stock (en memoria, sin BD real) |
|Deploy en Railway |✅ Activo |HTTPS habilitado; push a main activa deploy automático |


> **Nota:** La autenticación real con JWT, la persistencia en base de datos y los endpoints REST se implementarán en Sprint 2 con Python/Flask.

-----

## 📖 Historias de Usuario — Sprint 1 (16 HUs)

|HU |Resp.|Prior.|Historia |
|-----|-----|------|------------------------------------------------------------------|
|HU-01|MG |Alta |Repositorio GitHub con ramas main/dev |
|HU-02|MG |Alta |Estructura HTML base y Design System CSS |
|HU-03|MG |Alta |Header sticky con navegación entre vistas |
|HU-04|JG |Alta |Objeto DB local en JS (usuarios, productos, pedidos) |
|HU-05|JG |Alta |Modal de login/registro con validación local y redirección por rol|
|HU-06|MG |Alta |Grid de 15 productos con emoji, precio COP y badge de stock |
|HU-07|JG |Alta |Filtros por categoría y búsqueda en tiempo real |
|HU-08|MG |Alta |Carrito lateral con control de cantidades y total en tiempo real |
|HU-09|MG |Alta |Formulario de checkout con prerelleno de datos |
|HU-10|MG |Alta |Factura con número único e impresión PDF |
|HU-11|JG |Alta |Panel cliente con historial y gráfico mensual |
|HU-12|JG |Media |Edición de perfil personal durante la sesión activa |
|HU-13|MG |Alta |Dashboard admin con KPIs desde DB local |
|HU-14|JG |Alta |Despachar/cancelar pedidos pendientes (en memoria) |
|HU-15|JG |Alta |Editar stock y precios desde modal |
|HU-16|MG |Media |Sección del equipo y confirmación de deploy en Railway |

**Resultado: 16/16 HUs completadas ✅**

-----

## 🗓️ Planificación de Sprints

|Sprint |Objetivo |Entregables Clave |
|--------------|--------------------------------------------------|------------------------------------------------------------------------------------|
|**Sprint 1** ✅|Frontend completo en producción |Tienda funcional, carrito, checkout, factura, paneles, deploy Railway |
|**Sprint 2** |Backend Python/Flask + JWT real + MongoDB Atlas |API REST funcional, autenticación real, CRUD de productos con endpoints documentados|
|**Sprint 3** |Dashboard, Kanban, Swagger/OpenAPI, CI/CD completo|Dashboard con gráficas dinámicas, todos los endpoints en Swagger, pipeline CI/CD |
|**Sprint 4** |Pruebas, reportes, sistema completo en Render.com |Suite PyTest ≥70% cobertura, reportes PDF/Excel, deploy final en Render.com + Docker|

-----

## 🏗️ Arquitectura (Sprint 2+)

```
Frontend (HTML/CSS/JS → React)
↓ HTTP requests
Backend Python/Flask → API REST endpoints → Swagger /api/docs
↓
Base de Datos (MySQL / MongoDB Atlas)
↓
Deploy: Docker + Render.com ← GitHub Actions CI/CD
```

-----

## 📂 Estructura del Repositorio

```
proyecto/
├── index.html # App frontend completa (Sprint 1)
├── README.md # Este archivo
└── .github/
└── workflows/ # CI/CD GitHub Actions
```

> En Sprint 2 se añadirán: `backend/`, `frontend/`, `Dockerfile`, `requirements.txt`, `docker-compose.yml`

-----

## ⚙️ Cómo ejecutar localmente

### Sprint 1 (Frontend estático)

```bash
# Clonar el repositorio
git clone https://github.com/jess-1304/proyecto.git
cd proyecto

# Abrir en el navegador (sin servidor necesario)
open index.html
# o simplemente hacer doble clic en index.html
```

### Sprint 2+ (Backend Python/Flask)

```bash
# Instalar dependencias
pip install -r requirements.txt

# Variables de entorno
cp .env.example .env
# Configurar DB_URL, JWT_SECRET, etc.

# Ejecutar
python app.py
# API disponible en http://localhost:5000
# Swagger en http://localhost:5000/api/docs
```

-----

## 🔄 Flujo CI/CD

```
Código local (VS Code)
→ git commit (rama dev)
→ Pull Request a main (revisión cruzada)
→ GitHub Actions detecta push
→ Deploy automático a Railway/Render.com
→ URL HTTPS activa en producción
```

-----

## 📊 Métricas del Sprint 1

- **16/16** historias de usuario completadas
- **10** impedimentos detectados y resueltos dentro del sprint
- **5** jornadas de trabajo (Lunes a Viernes)
- **100%** del frontend en producción

-----

## 👨‍💻 Convención de Commits

```
feat: nueva funcionalidad
fix: corrección de bug
docs: actualización de documentación
style: cambios de formato/CSS
refactor: refactorización de código
test: añadir o modificar pruebas
chore: tareas de mantenimiento
```

-----

**Marlón Gélvez · Jesús González | Grupo E192 · UTS Bucaramanga 2026**
