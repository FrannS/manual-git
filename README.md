📘 Introducción

Git es un sistema de control de versiones que permite registrar los cambios en los archivos de un proyecto y colaborar con otras personas.
A continuación, detallo los comandos básicos que usé y su propósito.

🧭 1. git init

Inicializa un nuevo repositorio local en la carpeta actual.

Uso:
git init

Ejemplo:
mkdir manual-git
cd manual-git
git init

Este comando crea una carpeta oculta llamada .git, donde se almacenará toda la información del repositorio.

📥 2. git clone

Clona un repositorio remoto (por ejemplo, desde GitHub) a tu computadora.

Uso:
git clone <url-del-repositorio>

Ejemplo:
git clone https://github.com/mi-usuario/manual-git.git

Esto descarga todos los archivos y el historial del proyecto.

🗂️ 3. git add

Agrega archivos al área de preparación antes de hacer un commit.

Uso:
git add <archivo>
O para agregar todos los archivos modificados:
git add .

Ejemplo:
git add README.md

💾 4. git commit

Guarda los cambios preparados en el historial del repositorio con un mensaje descriptivo.

Uso:
git commit -m "Mensaje del commit"

Ejemplo:
git commit -m "Agrega manual de comandos básicos de Git"

Cada commit representa una versión del proyecto que puedo recuperar más adelante.

📜 5. git log

Muestra el historial de commits del repositorio.

Uso:
git log

Ejemplo:
git log --oneline

Muestra de forma resumida los commits realizados.

🔄 6. git checkout

Permite cambiar entre ramas o versiones específicas del proyecto.

Uso:
git checkout <nombre-de-rama>
O para revisar un commit antiguo:
git checkout <id-del-commit>

Ejemplo:
git checkout main

🌿 7. git branch

Sirve para crear, listar o eliminar ramas.

Usos comunes:
git branch             # Lista ramas
git branch <nombre>    # Crea una nueva rama
git branch -d <nombre> # Elimina una rama

Ejemplo:
git branch desarrollo

🚀 8. git push
Envía los commits locales al repositorio remoto (por ejemplo, en GitHub).

Uso:
git push origin <nombre-de-rama>

Ejemplo:
git push origin main

⬇️ 9. git pull

Descarga y fusiona los cambios desde el repositorio remoto al local.

Uso:
git pull origin <nombre-de-rama>

Ejemplo:
git pull origin main

🔗 10. git merge

Fusiona los cambios de una rama con otra.

Uso:
git merge <rama-a-fusionar>

Ejemplo:
git merge desarrollo

Este comando combina los cambios de la rama desarrollo con la rama actual (por ejemplo, main).

🧩 Ejemplo práctico del flujo de trabajo

# Crear o clonar el repositorio
git init
git remote add origin https://github.com/mi-usuario/manual-git.git

# Agregar y confirmar cambios
git add .
git commit -m "Primer commit del proyecto"

# Subir los cambios
git branch -M main
git push -u origin main

# Crear una rama de desarrollo
git branch desarrollo
git checkout desarrollo

# Hacer cambios, confirmarlos y fusionar
git add .
git commit -m "Actualiza README con explicaciones"
git checkout main
git merge desarrollo
git push origin main

🏁 Conclusión

Con estos comandos, puedo controlar versiones, colaborar con otros desarrolladores y mantener un historial claro de mi proyecto.
Este manual me permitió reforzar mi comprensión del funcionamiento de Git y GitHub, aplicando en la práctica cada uno de los comandos vistos en clase.

✍️ Autor: Francisco Javier Aguilar Barrera
📅 Fecha de creación: 6 de noviembre de 2025