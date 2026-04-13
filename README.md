# 🌙 Arch Hyprland Dotfiles (Noctalia)

Este repositorio contiene mi configuración personal de **Arch Linux** con **Hyprland**, optimizada para un flujo de trabajo rápido, estética oscura y temática de Samuráis (Vagabond).

---

## 📸 Vista Previa (Mi Configuración)

Aquí puedes ver cómo queda la estética "Noctalia Samurai" en acción:

<p align="center">
  <img src="https://github.com/user-attachments/assets/e855c0a5-141a-4464-bef0-086fd9eec6ab" height="250" alt="Login" />
  <img src="https://github.com/user-attachments/assets/bddf194d-1531-4cf8-8274-d3d0cbcc5b95" height="250" alt="Terminal" />
</p>
<p align="center">
  <img src="https://github.com/user-attachments/assets/77c99c35-d3b4-462d-b489-5d0ec9141605" height="250" alt="Widgets" />
  <img src="https://github.com/user-attachments/assets/e04f62d4-973d-486d-9351-ce876bd24f2c" height="250" alt="Limpio" />
</p>

---

## 🛠️ Componentes Principales

- **WM:** [Hyprland](https://hyprland.org/)
- **Terminal:** [Kitty](https://sw.kovidgoyal.net/kitty/)
- **Shell:** [Fish](https://fishshell.com/) (con Starship prompt)
- **Gestor de Archivos:** Thunar & [Yazi](https://yazi-rs.github.io/)
- **Barra:** Waybar
- **Extras:** MangoHud, Fastfetch, Spotify, Btop

---

## 📁 Estructura del Repo

- `hypr/`: Configuración del gestor de ventanas (atajos, monitores, animaciones).
- `minimaLinux/`: Scripts base y recursos de instalación.
- `fish/`: Alias, funciones y personalización de la shell.
- `kitty/`: Estética y fuentes de la terminal.
- `noctalia/`: Temas, colores y plugins propios.
- `fastfetch/`: Configuración del logo y la info del sistema.

---

## 🚀 Guía de Instalación (Paso a Paso)

Si vas a replicar este setup en una máquina nueva (especialmente en la Torre con Nvidia), sigue estos pasos:

### 1. Clonar el repositorio

```bash
cd ~
git clone https://github.com/camu-al/arch-hypr-dotfiles.git temp_dots
cp -r temp_dots/* ~/.config/
rm -rf temp_dots
```

---

### 2. Ejecutar instalador base

Entra en la carpeta de instalación incluida y lanza el script:

```bash
cd ~/.config/minimaLinux
chmod +x install.sh
./install.sh
```

---

### 3. Configuración para Nvidia

- Instalar drivers:

```bash
sudo pacman -S nvidia nvidia-utils nvidia-settings
```

- Añadir a parámetros del kernel (GRUB o cmdline):

```
nvidia_drm.modeset=1
```

- Asegurar variables en `~/.config/hypr/hyprland.conf`:

```
env = LIBVA_DRIVER_NAME,nvidia
env = XDG_SESSION_TYPE,wayland
env = GBM_BACKEND,nvidia-drm
env = __GLX_VENDOR_LIBRARY_NAME,nvidia
env = WLR_NO_HARDWARE_CURSORS,1
```

---

### 4. Toques Finales

- Cambiar shell a Fish:

```bash
chsh -s /usr/bin/fish
```

- Nota: La carpeta `animesp/` debe gestionarse manualmente por su tamaño.

---

## ❤️ Créditos

Mantenido por **camu-al** con ❤️ tras el rescate de 2026.

---

## 📌 Cómo subir cambios a GitHub

Ejecuta estos comandos en tu terminal para actualizar el README correctamente:

```bash
nano ~/.config/README.md
```

(Pega el contenido y guarda)

```bash
git add README.md
git commit -m "Update: README completo con galería e instalación paso a paso"
git pull origin main --rebase
git push origin main
```

---

✨ ¡Repositorio listo, documentado y con estilo Noctalia Samurai!
