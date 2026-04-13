# 🌙 Arch Hyprland Dotfiles (Noctalia)

Este repositorio contiene mi configuración personal de **Arch Linux** con **Hyprland**, está optimizada para un flujo de trabajo rápido, estética oscura y minimalista.

---

## 📸 Showcase (Mi Setup)

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
* **WM:** [Hyprland](https://hyprland.org/)
* **Terminal:** [Kitty](https://sw.kovidgoyal.net/kitty/)
* **Shell:** [Fish](https://fishshell.com/) (con Starship prompt)
* **Gestor de Archivos:** Thunar & [Yazi](https://yazi-rs.github.io/) (terminal)
* **Hardware Monitor:** Btop & MangoHud
* **Lanzador:** Rofi / Wofi
* **Barra:** Waybar

## 📁 Estructura del Repo
El repositorio incluye configuraciones para:
* `hypr/`: Atajos, monitores y animaciones.
* `fish/`: Alias y funciones personalizadas.
* `kitty/`: Estética de la terminal.
* `noctalia/`: Configuración de temas y plugins.
* `fastfetch/`: Personalización de la info del sistema.
* `mangaHud/` & `goverlay/`: Configuración para juegos.
* `gtk-3.0/` & `gtk-4.0/`: Temas visuales de las ventanas.

---

## 🚀 Guía de Instalación (Para la Torre)

Si vas a replicar este setup en una máquina nueva con **Nvidia**, sigue estos pasos:

### 1. Clonar el repositorio
```bash
cd ~
git clone [https://github.com/camu-al/arch-hypr-dotfiles.git](https://github.com/camu-al/arch-hypr-dotfiles.git) temp_dots
cp -r temp_dots/* ~/.config/
rm -rf temp_dots
