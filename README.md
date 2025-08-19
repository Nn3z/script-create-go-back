# backend-go
### Script para inicializar rápidamente un proyecto backend en Go con Fiber v2 y soporte de PostgreSQL, incluyendo:
- Estructura de carpetas recomendada.
- Configuración de .env para base de datos con postgresQL y JWT.
- Hot reload con Air.
- Utilidades para generar consultas SQL (INSERT y UPDATE dinámicas).

## REQUISITOS
- <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/go/go-original.svg" width="20" height="20"> **Go 1.24+** — [Instalar](https://go.dev/dl/)
- <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/postgresql/postgresql-original.svg" width="20" height="20"> **PostgreSQL** — [Instalar](https://www.postgresql.org/download/)
- <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/git/git-original.svg" width="20" height="20"> **Git** — Para clonar el repositorio

## INSTALACION

Sigue estos pasos para instalar y ejecutar **proyect-go**:

1. **Clona el repositorio:**
    ```bash
    git clone https://github.com/Nn3z/script-create-go-back.git
    cd script-create-go-back
    ```

2. **Mueve el script a /usr/local/bin para poder usarlo globalmente:**  
    ```bash
    sudo mv backend-go /usr/local/bin/
    sudo chmod +x /usr/local/bin/backend-go
    ```

3. **Actualizar el script cuando haya cambios**
    como seguimos en fase de prueba, la actualizacion se hara de la forma mas sencilla

    directamente en el repo donde clonaste el repositorio
    ```bash
    git pull
    sudo cp backend-go /usr/local/bin/
    sudo chmod +x /usr/local/bin/backend-go
    ```
## USO DEL SCRIPT
Inicia el script
```bash
backend-go init
```
Entra a la carpeta del proyecto generado
```bash
cd NOMBRE_DE_LA_CARPETA
```
Instalar las dependencias de Go y asegurarse de que go.sum esté completo:
```bash
go mod tidy
```
Ejecutar el proyecto con Air:
```bash
air
```


# GRACIAS EL APOYO
