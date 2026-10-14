# Guía de Instalación y Puesta en Marcha — Proyecto Lista de Tareas

Esta guía describe paso a paso cómo preparar tu entorno de desarrollo instalando **Node.js** e inicializar el proyecto localmente utilizando **Vite**.

---

## 1. Requisitos Previos: Instalación de Node.js

Para ejecutar este proyecto necesitas tener instalado **Node.js** (versión recomendada LTS 18 o superior), el cual incluye automáticamente **npm** (Node Package Manager).

### A. En Windows
1. Ingresa al sitio oficial: [https://nodejs.org](https://nodejs.org/)
2. Descarga el instalador recomendado **LTS** (`.msi`).
3. Ejecuta el archivo descargado y sigue el asistente de instalación asegurándote de mantener seleccionada la opción *"Add to PATH"*.
4. *Alternativa por terminal (PowerShell con Winget):*
   ```powershell
   winget install OpenJS.NodeJS.LTS
   ```

### B. En Linux (Ubuntu / Debian / derivados)
Abre tu terminal y ejecuta:
```bash
# Actualizar repositorios e instalar Node.js y npm
sudo apt update
sudo apt install nodejs npm -y
```
*(Opcional recomendado)* Si requieres la versión LTS más reciente mediante NodeSource:
```bash
curl -fsSL https://deb.nodesource.com/setup_lts.x | sudo -E bash -
sudo apt install -y nodejs
```

### C. En macOS
- Descarga el paquete `.pkg` desde [nodejs.org](https://nodejs.org/), o bien usando Homebrew:
  ```bash
  brew install node
  ```

---

## 2. Verificación de la Instalación

Abre una terminal nueva (PowerShell, Git Bash, Bash o Zsh) y comprueba que Node y npm se encuentren disponibles en tu ruta del sistema:

```bash
node -v
npm -v
```

*Deberías ver la versión instalada de cada herramienta (por ejemplo: `v20.x.x` o superior para Node, y `10.x.x` o superior para npm).*

---

## 3. Clonar el Repositorio

Si aún no tienes el código en tu equipo, clónalo mediante Git y accede al directorio de trabajo:

```bash
git clone https://github.com/anthra123x/tareas.git
cd tareas
```

---

## 4. Instalación de Dependencias

Dentro de la carpeta raíz del proyecto, instala los módulos requeridos (incluyendo el servidor Vite):

```bash
npm install
```

Este comando creará la carpeta local `node_modules` y verificará el archivo `package-lock.json`.

---

## 5. Inicialización del Entorno de Desarrollo

Para poner en marcha el servidor local con recarga en caliente (*Hot Module Replacement*):

```bash
npm run dev
```

Una vez ejecutado, la terminal mostrará la URL de acceso local (por defecto [http://localhost:5173/](http://localhost:5173/)). Abre dicha dirección en tu navegador para ver la aplicación en funcionamiento.

---

## 6. Scripts Disponibles

En el archivo `package.json` dispones de los siguientes comandos:

| Comando | Acción |
| :--- | :--- |
| `npm run dev` | Inicia el servidor de desarrollo local con Vite. |
| `npm run build` | Compila y optimiza el código para producción en la carpeta `dist/`. |
| `npm run preview` | Previsualiza localmente el resultado de la compilación de producción. |

---

## 7. Estructura del Proyecto

```text
├── index.html          # Estructura principal de la aplicación
├── style.css           # Hoja de estilos de la interfaz
├── package.json        # Definición de dependencias y scripts de Vite
├── package-lock.json   # Árbol exacto de dependencias bloqueadas
├── .gitignore          # Archivos y carpetas ignorados por Git
└── README.md           # Guía de instalación y documentación
```
