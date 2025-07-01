Este curso me proporcionó una comprensión profunda y práctica del sistema de control de versiones Git y su integración con GitHub, cubriendo desde conceptos básicos hasta flujos de trabajo colaborativos avanzados. A continuación, detallo los aprendizajes clave y habilidades adquiridas.

---

### ⚙️ Fundamentos de Git

- **Inicialización del repositorio** con `git init`.
    
- Seguimiento de archivos mediante `git add`, `git commit` y `git status`.
    
- Exploración del historial con `git log`, `git show`, `git diff`, y variantes avanzadas (`--oneline`, `--stat`, `--graph`).
    
- Visualización de archivos con `cat`, `ls`, `pwd`, `history`.
    

---

### 📦 Estados y flujo de trabajo

- **Working Directory**, **Staging Area** y **.git Directory**.
    
- Estados de archivo: `untracked`, `staged`, `tracked`, `unstaged`.
    
- Uso de `git stash` para guardar cambios temporalmente y retomarlos después (`stash list`, `stash pop`, `stash apply`).
    
- Limpieza de archivos no deseados con `git clean`.
    

---

### 🔀 Manejo de ramas (Branches)

- Creación de ramas (`git branch`, `git checkout -b`).
    
- Cambio entre ramas (`git checkout`).
    
- Fusión de ramas (`git merge`), solución de conflictos y cancelación con `git merge --abort`.
    
- Flujo de trabajo con ramas como `main`, `development`, y `hotfix`.
    

---

### 📡 Trabajo con repositorios remotos

- Conexión y sincronización con GitHub u otros servidores:
    
    - `git clone`, `git push`, `git pull`, `git fetch`, `git remote add`.
        
- Flujo de trabajo colaborativo con ramas remotas (`origin`, `upstream`).
    
- Protección de ramas principales (como `main`) y gestión mediante revisiones de código.
    

---

### 📌 Pull Requests y colaboración

- Proceso completo para crear un **Pull Request** (PR), recibir retroalimentación, hacer correcciones y fusionar cambios.
    
- Roles como **DevOps** y flujos de trabajo con revisión de código antes del merge.
    
- Diferencia entre colaborar como **contribuidor** o mediante un **fork** con PRs externos.
    

---

### 🔖 Etiquetas y versiones

- Uso de `git tag` para asignar versiones a commits importantes.
    
- Tipos de tags: **ligeros** y **anotados**.
    
- Compartir (`git push origin --tags`) y eliminar etiquetas (`git tag -d` y `git push origin :refs/tags/<tag>`).
    

---

### 🔃 Git Rebase

- Rebase como alternativa a `merge`, con advertencias sobre su uso en repositorios públicos.
    
- Comandos: `git rebase master`, `git rebase feature`, `git rebase --abort`.
    

---

### 🧪 Cherry Pick

- Selección de commits específicos para integrarlos a otras ramas sin fusionar todo el historial (`git cherry-pick SHA`).
    
- Manejo de conflictos con `git cherry-pick --abort`.
    

---

### 🔐 Seguridad con SSH

- Generación y configuración de llaves SSH (`ssh-keygen`, `ssh-add`) para autenticación segura con GitHub.
    

---

### 🔁 Recuperación y reescritura de historial

- `git reset`: revertir a estados anteriores (`--soft`, `--mixed`, `--hard`).
    
- `git commit --amend`: modificar el último commit.
    
- `git reflog`: ver referencias anteriores para recuperar estados perdidos.
    

---

### 👥 Comandos colaborativos

- `git shortlog`: ver aportes por autor.
    
- `git blame`: identificar línea por línea quién hizo qué en un archivo.
    
- `git branch -a/-r`: ver ramas locales y remotas.
    

---

### ☁️ Deployment

- Flujo básico para hacer deploy desde GitHub a un servidor web.
    
- Recomendaciones sobre el uso de `.gitignore` para proteger archivos sensibles como `.env` o carpetas como `node_modules`.
    

---

## ✅ Conclusión

Este curso me permitió dominar Git como herramienta esencial para el control de versiones, y GitHub como plataforma de colaboración profesional. Entendí cómo gestionar proyectos de forma individual y en equipo, optimizar el historial del repositorio, resolver conflictos, implementar flujos de trabajo colaborativos, aplicar versiones con tags y manejar seguridad con SSH.