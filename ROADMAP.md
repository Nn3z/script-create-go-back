# 🗺️ Roadmap de Desarrollo

Este documento detalla los objetivos de las próximas versiones de `backend-go`, enfocándose en transformar este script de inicialización en una herramienta robusta y escalable, apta para equipos de desarrollo.

---

## 🛠️ v0.1 — Estabilidad Mínima (Próximamente)

El objetivo de esta versión es asegurar que el proyecto generado sea consistente y reproducible en cualquier máquina.

| Tarea | Impacto |
| :--- | :--- |
| Fijar versiones en dependencias (`go get ...@versión`) | Evitar *builds* rotos por cambios no deseados en dependencias *upstream*. |
| Agregar `.editorconfig` y `golangci-lint` preconfigurado | Establecer estándares de estilo y calidad de código desde el inicio. |
| `.gitignore` extendido | Incluir exclusiones comunes (*logs*, cobertura, binarios generados). |

**📌 Meta:** Que cualquier desarrollador pueda clonar y tener el mismo estado inicial de proyecto.

---

## ✅ v0.2 — Confianza Básica (Siguiente Prioridad)

Introducir la cultura de pruebas y optimizar el flujo de trabajo diario con comandos simplificados.

| Tarea | Impacto |
| :--- | :--- |
| Tests iniciales | Test básico para la conexión DB y el *endpoint* `/health`. |
| Agregar `Makefile` | Incluir comandos comunes de ejecución (`make run`, `make build`, `make test`, `make docker-up`). |

**📌 Meta:** Empezar con una cultura de pruebas y simplificar la ejecución de tareas diarias.

---

## 🌍 v0.3 — Entornos Múltiples

Dotar al proyecto de la capacidad de manejar configuraciones diferentes para desarrollo, *staging* y producción de manera limpia.

| Tarea | Impacto |
| :--- | :--- |
| Soporte multi-env | Implementar manejo de archivos `.env.dev`, `.env.staging`, `.env.prod`. |
| `docker-compose.override.yml` | Configurar puertos y volúmenes específicos para el flujo de desarrollo local. |
| Estandarizar variables sensibles | Garantizar un esquema consistente para variables clave (JWT, DB, API keys). |

**📌 Meta:** Que el mismo proyecto pueda vivir en diferentes entornos (dev/staging/prod) sin necesitar cambios en el código.

---

## 🧩 v0.4 — Starter API Real

Superar el "Hello World" y proporcionar una base API funcional para que los equipos puedan empezar a construir valor inmediatamente.

| Tarea | Impacto |
| :--- | :--- |
| Rutas de ejemplo | Añadir rutas comunes como `/auth/login` y `/users`. |
| Middlewares básicos | Incluir configuraciones para Logger, Recovery, CORS y JWT auth. |
| Logger centralizado | Implementar una librería de *logging* estándar (ej. `zerolog` o `log/slog`). |

**📌 Meta:** Proporcionar un *starter* que no sea un *hello world*, sino piezas de API listas para usar.

---

## 📦 v0.5 — Base de Datos Seria

Transicionar de archivos de esquema estáticos a un sistema de gestión de bases de datos profesional y reproducible.

| Tarea | Impacto |
| :--- | :--- |
| Migraciones | Reemplazar `schema.sql` plano por migraciones usando `golang-migrate`. |
| Seeders iniciales | Funciones para poblar la DB con datos de prueba al iniciar. |
| Conexión DB desacoplada | Refactorizar la lógica de DB con interfaces (`internal/repository`). |

**📌 Meta:** Flujos de migraciones reproducibles en desarrollo local, CI/CD y producción.

---

## 🔧 v0.6 — Trabajo en Equipo

Mejorar la experiencia de *onboarding* y garantizar la calidad del código mediante la automatización.

| Tarea | Impacto |
| :--- | :--- |
| Red Docker propia | Definir una red aislada en `docker-compose` para evitar conflictos con otros servicios locales. |
| Scripts de inicialización | Crear scripts de utilidad (`./scripts/setup.sh`, `./scripts/test.sh`). |
| Documentación Onboarding | Mejorar el `README` con un flujo de *onboarding* detallado. |
| GitHub Actions básico | Configurar un flujo de CI/CD mínimo (`lint` + `test` en PRs). |

**📌 Meta:** *Onboarding* rápido para nuevos miembros y CI/CD mínimo funcionando.

---

## 🔮 v0.7 — Escalabilidad y Opciones

El objetivo a largo plazo: transformar el script Bash en una herramienta CLI completa y expandir las opciones de *stack* inicial.

| Tarea | Impacto |
| :--- | :--- |
| CLI propio en Go | Sustituir el script Bash actual por una aplicación CLI compilada en Go. |
| Stack seleccionable | Permitir al usuario elegir DB (Postgres/MySQL/SQLite) y ORM (GORM/SQLx). |
| Plantilla multi-servicio | Opción para inicializar microservicios secundarios (`init service <nombre>`). |
| Devcontainers | Proporcionar configuración para entornos de desarrollo en contenedores (VSCode/JetBrains). |

**📌 Meta:** Convertir el *starter* en un *tooling* real y versátil para equipos grandes.