# 🧠 Manual de Comandos de Git y GitHub

**Autor:** Francisco Javier Aguilar Barrera
**Fecha:** 5 de Noviembre de 2025

---

## 📘 Introducción

Este documento es un **manual explicativo sobre los comandos básicos de Git**, elaborado como parte de la tarea *“Manual de comandos Git en GitHub”*.

Mi objetivo es demostrar mi comprensión del funcionamiento de Git mediante explicaciones claras, ejemplos prácticos y una estructura ordenada.

Git es una herramienta de **control de versiones distribuido** que permite registrar cambios, colaborar con otros desarrolladores y mantener el historial completo de un proyecto.
GitHub, por su parte, es una plataforma en línea que aloja repositorios y facilita el trabajo colaborativo.

---

## ⚙️ Preparación inicial

Antes de empezar a usar los comandos, realicé la configuración básica de Git en mi computadora.

```bash
git config --global user.name "Mi Nombre"
git config --global user.email "mi-correo@ejemplo.com"
```

Esto permite que cada commit quede registrado con mi nombre y correo.

Verifiqué la configuración con:

```bash
git config --list
```

---

## 🏗️ Flujo general de trabajo en Git

El ciclo básico de Git consiste en estos pasos:

1. **Inicializar** o **clonar** un repositorio.
2. **Agregar cambios** al área de preparación.
3. **Confirmar (commit)** los cambios.
4. **Enviar (push)** al repositorio remoto en GitHub.
5. **Actualizar (pull)** para obtener los cambios más recientes.
6. **Fusionar (merge)** ramas cuando sea necesario.

---

## 🔰 Comandos principales de Git

### 1️⃣ `git init` — Inicializar un repositorio

Crea un repositorio vacío en la carpeta actual.

**Uso:**

```bash
git init
```

**Ejemplo:**

```bash
mkdir manual-git
cd manual-git
git init
```

👉 Este comando genera una carpeta oculta `.git` que almacena toda la información del proyecto.

---

### 2️⃣ `git clone` — Clonar un repositorio remoto

Descarga un repositorio existente de GitHub a tu computadora.

**Uso:**

```bash
git clone <url-del-repositorio>
```

**Ejemplo:**

```bash
git clone https://github.com/mi-usuario/manual-git.git
```

👉 Esto crea una copia completa del proyecto, incluyendo historial y ramas.

---

### 3️⃣ `git add` — Añadir archivos al área de preparación

Indica qué archivos serán incluidos en el próximo commit.

**Uso:**

```bash
git add <archivo>
```

O para agregar todos los archivos modificados:

```bash
git add .
```

**Ejemplo:**

```bash
git add README.md
```

💡 *El área de preparación (staging area) es donde selecciono los archivos que quiero guardar definitivamente.*

---

### 4️⃣ `git commit` — Guardar los cambios en el historial

Crea un nuevo punto en el historial del repositorio con los cambios preparados.

**Uso:**

```bash
git commit -m "Mensaje descriptivo"
```

**Ejemplo:**

```bash
git commit -m "Agrega manual de comandos básicos de Git"
```

📌 *Cada commit representa una versión específica del proyecto.
Es recomendable usar mensajes claros y breves.*

---

### 5️⃣ `git log` — Ver historial de commits

Muestra una lista de los commits realizados, junto con su autor, fecha e identificador (hash).

**Uso:**

```bash
git log
```

**Ejemplo:**

```bash
git log --oneline
```

📖 *El historial me permite revisar los cambios realizados y regresar a versiones anteriores si es necesario.*

---

### 6️⃣ `git checkout` — Cambiar de rama o versión

Permite moverse entre ramas o versiones específicas de un commit.

**Uso:**

```bash
git checkout <nombre-de-rama>
```

O para ver un commit anterior:

```bash
git checkout <id-del-commit>
```

**Ejemplo:**

```bash
git checkout main
```

🚀 *Es muy útil para trabajar en diferentes versiones del proyecto sin afectar la rama principal.*

---

### 7️⃣ `git branch` — Crear o listar ramas

Las ramas permiten desarrollar nuevas funcionalidades sin alterar el código principal.

**Usos más comunes:**

```bash
git branch             # Lista ramas locales
git branch <nombre>    # Crea una nueva rama
git branch -d <nombre> # Elimina una rama
```

**Ejemplo:**

```bash
git branch desarrollo
git checkout desarrollo
```

🌿 *Cada rama es como una línea paralela de trabajo.
Al final puedo fusionarla con la rama principal (`main`) mediante `git merge`.*

---

### 8️⃣ `git push` — Enviar cambios al repositorio remoto

Sube los commits locales a GitHub.

**Uso:**

```bash
git push origin <nombre-de-rama>
```

**Ejemplo:**

```bash
git push origin main
```

💡 *El primer push puede requerir autenticación con GitHub (token o SSH).*

---

### 9️⃣ `git pull` — Descargar y fusionar cambios del remoto

Actualiza el repositorio local con los cambios del remoto.

**Uso:**

```bash
git pull origin <nombre-de-rama>
```

**Ejemplo:**

```bash
git pull origin main
```

🔄 *Combina “fetch” (descargar) y “merge” (fusionar) en un solo paso.*

---

### 🔟 `git merge` — Fusionar ramas

Combina los cambios de una rama con otra.

**Uso:**

```bash
git merge <rama-a-fusionar>
```

**Ejemplo:**

```bash
git merge desarrollo
```

📌 *Después de fusionar, puedo eliminar la rama que ya no necesito:*

```bash
git branch -d desarrollo
```

---

## 🧩 Ejemplo práctico del flujo completo

A continuación muestro un flujo real que seguí para este proyecto:

```bash
# 1. Inicializo el repositorio local
git init

# 2. Agrego el repositorio remoto
git remote add origin https://github.com/mi-usuario/manual-git.git

# 3. Creo y agrego el README
git add README.md
git commit -m "Crea README con manual de comandos básicos"

# 4. Envío los cambios a GitHub
git branch -M main
git push -u origin main

# 5. Creo una nueva rama para mejoras
git branch desarrollo
git checkout desarrollo
# (realizo cambios)
git add .
git commit -m "Agrega secciones adicionales al manual"

# 6. Fusiono los cambios en la rama principal
git checkout main
git merge desarrollo
git push origin main
```

---

## 💡 Buenas prácticas que aprendí

✔️ Usar mensajes de commit claros y en tiempo presente.
✔️ Hacer `git pull` antes de empezar a trabajar cada día.
✔️ Crear ramas para cada nueva funcionalidad o corrección.
✔️ Revisar `git status` y `git log` frecuentemente.
✔️ No subir archivos innecesarios (usar `.gitignore` cuando sea necesario).

---

## 🏁 Conclusión

Este manual reúne los **comandos fundamentales de Git** y explica su uso dentro de un flujo de trabajo real con **GitHub**.
Gracias a este ejercicio, comprendí mejor cómo controlar versiones, trabajar con ramas y mantener un historial limpio y organizado.

---
