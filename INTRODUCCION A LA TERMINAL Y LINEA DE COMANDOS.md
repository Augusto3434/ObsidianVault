Durante este curso aprendí a interactuar directamente con el sistema operativo a través de la terminal, utilizando la shell de Linux (Bash) dentro del Subsistema de Windows para Linux (WSL). Aquí algunos de los aprendizajes clave y habilidades adquiridas:

#### ⚙️ **Variables de entorno y personalización del entorno**

- Comprendí la utilidad de variables de entorno como `PATH`, `HOME`, `SHELL`, y cómo visualizarlas con `echo $VARIABLE`.
    
- Edición del archivo `.bashrc` para definir variables personalizadas y crear **alias** para automatizar tareas (ej. abrir carpetas o ejecutar VS Code con un solo comando).
    
- Uso de `ls -la` para visualizar archivos ocultos como `.bashrc`.
    

#### 🔍 **Comandos de búsqueda de archivos**

- **`find`**: búsqueda de archivos por nombre, tipo (`-type f/d`), tamaño (`-size`), permisos (`-perm`) o tiempo de modificación (`-mtime`). También aprendí a ejecutar acciones con `-exec`, como copiar archivos modificados a un directorio de respaldo.
    
- **`locate`** y **`updatedb`**: búsqueda rápida basada en una base de datos indexada del sistema.
    
- **`whereis`** y **`which`**: búsqueda de binarios o rutas de comandos dentro del sistema (`which` revisa rutas del `PATH`).
    

#### 📂 **Manipulación y navegación de archivos**

- Comandos como `pwd`, `cd`, `touch`, `mkdir`, `cp -r`, `rm`, `ls`, y `cat` fueron parte del flujo habitual de trabajo.
    
- Uso de redirección de salidas (`>`, `>>`) y **pipes** (`|`) para encadenar comandos.
    
- Operadores lógicos para ejecutar comandos en paralelo (`&`) o condicionales (`&&`, `||`).
    

#### 📄 **Uso de `grep` para búsquedas avanzadas dentro de archivos**

- Búsqueda de texto con expresiones regulares usando `grep`.
    
- Uso de flags como:
    
    - `-i` para ignorar mayúsculas/minúsculas.
        
    - `-c` para contar coincidencias.
        
    - `-v` para excluir resultados.
        
    - `-m` para limitar el número de líneas encontradas.
        

#### ✍️ **Editor de texto Vim**

- Uso básico de `vim` para crear, editar y guardar archivos desde la terminal.
    
- Comandos clave: `i` (modo inserción), `:w` (guardar), `:q` (salir), `dd` (borrar línea), `/` (buscar texto).
    
- Practiqué con ejercicios como crear una calculadora en Vim para reforzar el uso del editor.
    

#### 🛠️ **Administración básica del sistema**

- Monitoreo de procesos con `top`.
    
- Consulta de configuración de red con `ifconfig`.
    
- Uso de `chmod` para asignar permisos a archivos (lectura, escritura y ejecución para usuario, grupo u otros).