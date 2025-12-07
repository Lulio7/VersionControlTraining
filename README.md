# 🚀 Power BI + Git: Guía práctica para versionar reportes y modelos

El objetivo de esta guía es aprender de forma rápida y directa cómo integrar **Power BI** con **Git**, sin explicaciones largas ni teoría innecesaria.  
Nos enfocamos en el *20% esencial* que produce el *80% del resultado*.

---

# 📦 Contenido
1. Por qué usar Git con Power BI  
2. Requisitos  
3. Crear o clonar un repositorio  
4. Agregar archivos y realizar commits  
5. Configuración en Power BI (PBIP + TMDL)  
6. Guardar el proyecto como PBIP  
7. Integración con Power BI Service  
8. Revertir un commit o cambio incorrecto  
9. Recursos adicionales  

---

# 💡 1. ¿Por qué usar Git con Power BI?

Git agrega una capa profesional al desarrollo en Power BI:

- Control de versiones del reporte y el modelo
- Revertir errores sin romper el archivo
- Historial detallado de qué cambió y quién lo cambió
- Trabajo en ramas (features, fixes) sin afectar producción
- Facilita revisiones (pull requests) y auditorías
- Ordena el proyecto (adiós al “Dashboard_FINAL_v3_REAL.pbix”)
- Permite comparar cambios en texto gracias a PBIP + TMDL
- **Modelo centralizado ideal para usar IA:**
  - Optimizar DAX
  - Analizar relaciones
  - Generar documentación automática
  - Detectar dependencias o errores
- Integración con DevOps para procesos más escalables

---

# 🧩 2. Requisitos

Asegurate de tener:

- Una cuenta en **GitHub** o **Azure Repos**
- Git instalado en tu computadora  
- Visual Studio Code (VS Code)
- Extensiones recomendadas:
  - GitHub Pull Requests
  - Repositories
  - Azure Repos

Configuración inicial de Git (solo una vez):

Ingresa a la terminal individualmente los siguientes comandos:
git config --global user.name "Tu Nombre"
git config --global user.email "tuemail@example.com"

# 🧭 Pasos del 3 al 9 — Power BI + Git

## 3. Crear o clonar un repositorio

### ➤ Crear un repositorio nuevo
1. Ir a GitHub o Azure Repos.
2. Crear un repositorio vacío.
3. Copiar la URL HTTPS/SSH del repo.

### ➤ Clonar un repositorio existente
En Visual Studio Code:

1. Presionar `Ctrl + Shift + P`.
2. Buscar **Git: Clone**.
3. Pegar la URL del repositorio.
4. Elegir la carpeta local donde se guardará.

Esto crea una carpeta **vinculada automáticamente** al repositorio remoto.

---

## 4. Agregar archivos y realizar commits

### ➤ Agregar archivos
- Arrastrar los archivos a la carpeta del repositorio.
- VS Code los mostrará como **Untracked** (verde).

### ➤ Hacer commit
1. Ir a la sección **Source Control**.
2. Escribir un mensaje de commit claro.
3. Click en **Commit**.

### ➤ Sincronizar cambios
- **Push** = enviar cambios al repositorio.
- **Pull** = traer cambios desde el servidor.

---

## 5. Configuración en Power BI (PBIP + TMDL)

En Power BI Desktop:

**File → Options → Preview features**

Activar:
- **Power BI Project (PBIP)**
- **TMDL (Tabular Model Definition Language)**

### ➤ ¿Por qué PBIP?
Convierte el PBIX en un proyecto en carpetas: ideal para ser versionado con Git.

### ➤ ¿Por qué TMDL?
Expone el modelo semántico (DAX, relaciones, tablas) como texto, lo que permite:
- Revisiones
- Comparación de versiones
- Colaboración en PRs
- Consultas asistidas con IA

---

## 6. Guardar el proyecto como PBIP

1. `File → Save As → Power BI Project (.PBIP)`
2. Guardarlo **dentro de la carpeta del repositorio Git**.

### Estados en Git:
- **Verde = Untracked (nuevo)**
- **M = Modified (modificado)**

### Buenas prácticas:
- Commit por cada cambio relevante.
- Mensajes descriptivos.
- Evitar commits grandes sin detalle.

---

## 7. Integración con Power BI Service

En el Workspace:

1. Ir a **Settings**.
2. Habilitar **Git Integration**.
3. Conectar el repositorio (GitHub o Azure DevOps).
4. Seleccionar la branch a sincronizar.

Esto permite desplegar el reporte desde Git hacia Power BI Service.

---

## 8. Revertir un commit o cambio incorrecto

### ➤ En Azure Repos (método fácil)
1. Repositorio → Commits  
2. Seleccionar el commit  
3. Click en **Undo**

### ➤ Con Git en terminal (si sos la única persona en la branch)

⚠️ Solo si nadie más está usando esa branch.

Volver al commit anterior desde la terminal:

git reset --hard HEAD~1
git push origin <branch> --force

## 9. Recursos adicionales

Archivo con comandos básicos: git-commands.md
