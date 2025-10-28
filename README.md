# Electron-Vite-React-TS-Boilerplate
Boilerplate code for a base Electron app serving a React frontend with Vite. TypeScript is pre-configured.

---

## Table of Contents
* [Features](#features)
* [Getting Started](#getting-started)
* * [Prerequisites](#prerequisistes)
  * [Installation](#installation)
  * [Development Mode](#development-mode)
  * [Production Build](#production-build)
* [Project Structure](#project-structure)
* [Configuration](#configuration)
* * [```vite.config.ts```](#viteconfigts)
  * [```electron-builder.json```](#electron-builderjson)
  * [tsconfig files](#tsconfig-files)
* [Usage Tips](#usage-tips)
* [Contributing](#contributing)
* [Licence](#license)

---
  
## Features  
- ⚡ **Vite** for ultra-fast frontend builds and hot reload  
- ⚛️ **React** for modern UI components  
- 🧠 **TypeScript** with strict type safety  
- 💻 **Electron** for cross-platform desktop apps (Windows, macOS, Linux)  
- 📦 **Electron-Builder** for one-command packaging and installers  
- 🧱 Clean, modular file structure — easy to extend and customize 

---

## 🛠️ Getting Started  

### Prerequisites  
Ensure you have the following installed:  
- Node.js (v14 or newer)  
- npm or yarn  
- Git  

> 📝 **Note:** If you plan to distribute your app for macOS, you may need Apple Developer credentials and code signing tools.

### Installation
```bash
  git clone https://github.com/ShayCerny/Electron-Vite-React-TS-Boilerplate.git
  cd Electron-Vite-React-TS-Boilerplate

  npm install
  # or
  yarn install
```

### Development Mode
Run the app with live reload for both the main and renderer processes:
``` bash
  npm run dev
  # or
  yarn dev
```
This launches Electron and Vite in watch mode, so UI and backend changes will reload automatically.

### Production Build
To build and pack the app:
``` bash
  npm run build:win
  # or
  yarn build:win
```
```Build:(os)``` compiles and packages the app for the os provided. replace (os) with ```win``` ```mac``` or ```linux```

---

## Project Structure
```pgsql
Electron-Vite-React-TS-Boilerplate/
|-src/
|  |-renderer/
|  |- main/
project-folder/
├── src/
│   ├── main/
│   │   ├── main.ts
│   │   ├── events.ts
│   │   ├── preload.cts
│   │   └── tsconfig.json
│   ├── renderer/
│   │   ├── styles/
│   │   │   └── app.scss
│   │   ├── App.tsx
│   │   └── main.tsx
│   └── assets/
│       ├── icon.png
│       └── react.svg
├── index.html
├── vite.config.ts
├── electron-builder.json
├── tsconfig.json
├── tsconfig.node.json
├── tsconfig.app.json
├── package.json
├── .gitignore
└── README.md
```

### Key Directories:
* ```src/main/``` → Electron main process
* ```src/renderer``` → React frontend
* ```src/assets/``` → icons and static files

---

## Configuration
### ```vite.config.ts```
Handles bundling, aliasing, and HMR setup for the React Renderer
Customize build output, aliases, and other Vite Options here

### ```electron-builder.json'''
Defines how the app is packaged - includes product name, version, icons, and build targets.
Update this file to reflect your project's name, description, and target platforms

### tsconfig files
* ```tsconfig.json``` → shared base config
* ```tsconfig.node.json``` → settings for the Electron main process
* ```tsconfig.app.json``` → settings for the Vite/React renderer

---

## 💡 Usage Tips
* Use ```ipcMain``` / ```ipcRenderer``` for safe communication between main and renderer processes.
* Keep environment variables separate using ```.env``` and ```import.meta.env``` for the renderer.
* Test builds for each platform you plan to distribute to (Windows, macOS, Linux).
* If you use native Node modules, rebuild them for Electron's runtime version.
* Consider auto-update integration (supported by **electron-builder**) for production apps.

  ---

## 🤝 Contributing
Contributions are welcome!
1. Fork the repo
2. Create a feature branch
  ```bash
  git checkout -b feature/my-awesome-feature
  ```
3. Commit your changes
  ```bash
  git commit -m "Added some awesome feature"
  ```
4 Push the branch and open a Pull Request

Please make sure all code builds successfully and adheres to the existing structure before submitting.

---

## License
This project is licensed under the MIT License
  ```yaml
  MIT License
  © 2025 Shay Cerny
  ```

---

## Summary
This boilerplate gives you a production-ready foundation for creating a modern desktop app using:
`Electron + Vite + React + TypeScript`
Start building your app with zero setup hassle - just clone, install, and code. 🚀

---

Last updated: October 2025
  
  
