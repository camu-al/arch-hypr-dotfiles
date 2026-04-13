# 🌙 Arch Hyprland Dotfiles (Noctalia)

Mi configuración personal de **Arch Linux** usando **Hyprland**. Optimizado para flujo de trabajo rápido, estética oscura y minimalista.

---

## 🛠️ Componentes Principales
* **WM:** [Hyprland](https://hyprland.org/)
* **Terminal:** [Kitty](https://sw.kovidgoyal.net/kitty/)
* **Shell:** [Fish](https://fishshell.com/) (con Starship prompt)
* **Gestor de Archivos:** Thunar
* **Lanzador:** Rofi / Wofi
* **Barra:** Waybar

## 📁 Estructura del Repo
* `hypr/`: Configuración del Window Manager (atajos, monitores, animaciones).
* `fish/`: Alias y funciones de la shell.
* `kitty/`: Estilo de la terminal.
* `noctalia/`: Archivos de configuración de temas y plugins propios.
* `Thunar/`: Preferencias del gestor de archivos.

## 🚀 Notas para la Torre (Nvidia)
Para usar estos archivos en un PC con Nvidia, recordar:
1. Instalar drivers: `sudo pacman -S nvidia nvidia-utils`
2. Añadir `nvidia_drm.modeset=1` al kernel.
3. Asegurar que las variables de entorno en `hyprland.conf` estén activas:
   ```text
   env = LIBVA_DRIVER_NAME,nvidia
   env = WLR_NO_HARDWARE_CURSORS,1

## 🛠️ Guía de Instalación (Paso a Paso)

Si estás instalando esto en una máquina nueva, sigue estos pasos:

### 1. Clonar el repositorio
```bash
cd ~
git clone [https://github.com/camu-al/arch-hypr-dotfiles.git](https://github.com/camu-al/arch-hypr-dotfiles.git) temp_dots
cp -r temp_dots/* ~/.config/
rm -rf temp_dots   
