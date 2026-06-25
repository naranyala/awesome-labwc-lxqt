# Awesome LXQt [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated list of awesome LXQt desktop environment applications, window managers, themes, tools, and resources for X11 and Wayland.

[LXQt](https://lxqt-project.org/) is a lightweight, modular, and fast desktop environment using the Qt framework. It is the modern successor of LXDE, offering a classic desktop experience while remaining resource-efficient. LXQt 2.0+ supports **both X11 and Wayland** natively.

## Contents

- [Compositors & Window Managers](#compositors--window-managers)
  - [X11](#x11)
  - [Wayland](#wayland)
- [Core Components](#core-components)
- [Panel Plugins & Widgets](#panel-plugins--widgets)
- [Terminal Emulators](#terminal-emulators)
- [Software & Applications](#software--applications)
  - [Internet & Network](#internet--network)
  - [Multimedia](#multimedia)
  - [Graphics & Image](#graphics--image)
  - [Office & Productivity](#office--productivity)
  - [Utilities](#utilities)
  - [CLI & TUI Utilities](#cli--tui-utilities)
- [Compositing](#compositing)
  - [X11 Compositors](#x11-compositors)
  - [Wayland Compositing Features](#wayland-compositing-features)
- [Display Managers](#display-managers)
- [Screen Lockers](#screen-lockers)
- [Polkit Authentication Agents](#polkit-authentication-agents)
- [Clipboard Managers](#clipboard-managers)
- [Screenshot & Screen Recording](#screenshot--screen-recording)
- [OSD (On-Screen Display)](#osd-on-screen-display)
- [Notification Daemons](#notification-daemons)
- [Application Launchers](#application-launchers)
- [Alternative Panels & Bars](#alternative-panels--bars)
- [Dock Panels](#dock-panels)
- [Wallpapers & Backgrounds](#wallpapers--backgrounds)
- [Color Management & Dynamic Theming](#color-management--dynamic-theming)
- [XDG Desktop Portal](#xdg-desktop-portal)
- [GTK Integration & Theming](#gtk-integration--theming)
- [Service Integration](#service-integration)
  - [Audio](#audio)
  - [Network](#network)
  - [Bluetooth](#bluetooth)
  - [Printing](#printing)
  - [Power Management](#power-management)
- [How to Customize LXQt Desktop](#how-to-customize-lxqt-desktop)
- [Low-Level Dependencies & Libraries](#low-level-dependencies--libraries)
- [Building Custom GUI Apps](#building-custom-gui-apps)
- [Distributions](#distributions)
- [Resources & Tutorials](#resources--tutorials)
- [Community](#community)
- [Troubleshooting & FAQ](#troubleshooting--faq)

---

## Compositors & Window Managers

LXQt follows a modular design. It does not provide its own dedicated window manager or Wayland compositor, allowing users to choose the one that best fits their workflow.

### X11

- **[Openbox](http://openbox.org/wiki/Main_Page)** - The default and officially recommended X11 window manager for LXQt. Very lightweight, stable, and highly configurable via `obconf-qt` or raw XML.
- **[EXWM](https://github.com/emacs-exwm/exwm)** - Emacs X Window Manager. A full-featured X11 window manager built on top of Emacs. Run LXQt inside Emacs — use the panel, runner, and tray while EXWM manages windows with Emacs keybindings. Ideal for users who live in Emacs and want LXQt's desktop services.
- **[KWin (X11)](https://invent.kde.org/plasma/kwin)** - The KDE window manager. Provides excellent desktop effects, compositing, and integration, though it is heavier than Openbox.
- **[AwesomeWM](https://awesomewm.org/)** - A highly configurable, dynamic tiling window manager written in Lua. Combine with LXQt for a full DE experience with tiling.
- **[Bspwm](https://github.com/baskerville/bspwm)** - A tiling window manager that represents windows as the leaves of a full binary tree. Controlled via `bspc`.
- **[i3wm](https://i3wm.org/)** - A popular, simple, and well-documented tiling window manager with a text-based configuration.
- **[i3-gaps](https://github.com/Airblader/i3)** - A fork of i3 with gap support (visual gaps between windows). Superseded by i3 v4.22+ which added gaps natively.
- **[Herbstluftwm](https://herbstluftwm.org/)** - A manual tiling window manager using a tag-based workspace system. Fully controllable via IPC and shell scripts.
- **[dwm](https://dwm.suckless.org/)** - A dynamic tiling window manager from the suckless project. Extremely minimal; configured by editing source code.
- **[Qtile](https://qtile.org/)** - A full-featured, hackable tiling window manager written and configured in Python.
- **[Xfwm4](https://docs.xfce.org/xfce/xfwm4/start)** - The Xfce window manager, which works well in LXQt as a lightweight compositor alternative.
- **[Fluxbox](http://fluxbox.org/)** - A lightweight stacking window manager based on Blackbox. Very low resource usage.
- **[IceWM](https://ice-wm.org/)** - A fast, lightweight stacking window manager with a classic look and extensive theming support.
- **[JWM](https://joewing.net/projects/jwm/)** - Joe's Window Manager — a tiny, XML-configured stacking WM ideal for minimal setups.
- **[PekWM](https://github.com/pekdon/pekwm)** - A lightweight, Un*x-oriented window manager based on aewm++.
- **[FVWM](https://www.fvwm.org/)** - A powerful, highly extensible ICCCM-compliant window manager with virtual desktops.
- **[ctwm](https://github.com/ctwm/ctwm)** - Claude's Tab Window Manager — a derivative of twm with virtual desktops and configurability.
- **[2bwm](https://github.com/venam/2bwm)** - A very fast floating WM written in C with optional EWMH support and customizable borders.

### Wayland

LXQt 2.0+ has comprehensive native Wayland support, but it requires a third-party Wayland compositor to function. All compositors listed below are actively tested or confirmed working.

- **[Labwc](https://github.com/labwc/labwc)** - A wlroots-based window-stacking compositor heavily inspired by Openbox. The most recommended lightweight Wayland compositor for LXQt. Supports Openbox theme parsing.
- **[KWin (Wayland)](https://invent.kde.org/plasma/kwin)** - The KDE Wayland compositor. Offers robust integration with LXQt panel features, modern effects, and excellent compatibility with Qt apps.
- **[Wayfire](https://wayfire.org/)** - A 3D Wayland compositor based on wlroots. Supported by LXQt with specific backends for deep panel and taskbar integration.
- **[Sway](https://swaywm.org/)** - An i3-compatible tiling Wayland compositor. Highly stable, extensive documentation, and strong community.
- **[Hyprland](https://hyprland.org/)** - A highly customizable dynamic tiling Wayland compositor that emphasizes smooth animations, blur, rounded corners, and aesthetics.
- **[River](https://codeberg.org/river/river)** - A dynamic tiling Wayland compositor with a focus on simplicity and minimal configuration.
- **[dwl](https://codeberg.org/dwl/dwl)** - A dwm-inspired Wayland compositor. Minimal, suckless-style, configured by editing C source.
- **[Qtile (Wayland)](https://qtile.org/)** - The Qtile window manager also runs as a Wayland compositor, offering Python scripting.
- **[Niri](https://github.com/YaLTeR/niri)** - A scrollable-tiling Wayland compositor with unique window management (windows arranged in columns).
- **[Weston](https://gitlab.freedesktop.org/wayland/weston)** - The reference Wayland compositor. Lightweight and useful for testing, but less feature-rich.
- **[Hikari](https://hikari.acmelabs.space/)** - A compact, stacking Wayland compositor with an Openbox-like workflow.
- **[Cage](https://github.com/cage-kiosk/cage)** - A Wayland compositor designed for single-application kiosk mode, also usable as a minimal desktop.
- **[Cosmic (alpha)](https://github.com/pop-os/cosmic-epoch)** - Pop!_OS's Rust-based Wayland compositor (COSMIC). Pre-alpha but innovative; uses a tiling layout by default.

## Core Components

All official LXQt modules — the building blocks of the desktop.

- **[pcmanfm-qt](https://github.com/lxqt/pcmanfm-qt)** - The default file manager and desktop icon manager. Supports both X11 and Wayland desktop management.
- **[lxqt-panel](https://github.com/lxqt/lxqt-panel)** - The desktop panel. Supports X11 and Wayland (with compositor-specific backends). Hosts all panel plugins.
- **[lxqt-runner](https://github.com/lxqt/lxqt-runner)** - Quick launch tool used to run programs, open URLs, and calculate expressions.
- **[lxqt-session](https://github.com/lxqt/lxqt-session)** - The default LXQt session manager. Handles startup, autostart, and session lifecycle.
- **[lxqt-config](https://github.com/lxqt/lxqt-config)** - Central configuration center. Includes keyboard, mouse, monitor, appearance, and input settings.
- **[lxqt-about](https://github.com/lxqt/lxqt-about)** - A simple dialog showing information about LXQt.
- **[lxqt-admin](https://github.com/lxqt/lxqt-admin)** - A GUI for administrative tasks such as user and group management.
- **[lxqt-globalkeys](https://github.com/lxqt/lxqt-globalkeys)** - Global keyboard shortcuts daemon for LXQt.
- **[lxqt-notificationd](https://github.com/lxqt/lxqt-notificationd)** - The default LXQt notification daemon.
- **[lxqt-openssh-askpass](https://github.com/lxqt/lxqt-openssh-askpass)** - An OpenSSH askpass dialog for LXQt.
- **[lxqt-policykit](https://github.com/lxqt/lxqt-policykit)** - PolicyKit authentication agent for LXQt.
- **[lxqt-powermanagement](https://github.com/lxqt/lxqt-powermanagement)** - Power management handler — lid close, suspend, hibernate, etc.
- **[lxqt-qtplugin](https://github.com/lxqt/lxqt-qtplugin)** - Qt platform integration plugin. Provides native dialogs, LXQt theme integration, and Wayland support for Qt apps.
- **[lxqt-sudo](https://github.com/lxqt/lxqt-sudo)** - A GUI frontend for `sudo`/`su`/`doas`.
- **[lxqt-themes](https://github.com/lxqt/lxqt-themes)** - The default set of LXQt themes (Frost, Dark, Ambiance, etc.).
- **[lximage-qt](https://github.com/lxqt/lximage-qt)** - The default image viewer and screenshot tool.
- **[qterminal](https://github.com/lxqt/qterminal)** - A lightweight, feature-rich Qt-based terminal emulator.
- **[qtermwidget](https://github.com/lxqt/qtermwidget)** - The terminal widget used by QTerminal (also embeddable in other apps).
- **[screengrab](https://github.com/lxqt/screengrab)** - A cross-platform screenshot tool for LXQt.
- **[lxqt-archiver](https://github.com/lxqt/lxqt-archiver)** - A simple Qt archive manager (frontend for `libarchive`/`arj`/`7z`).

## Panel Plugins & Widgets

Built-in plugins that ship with `lxqt-panel`. Activate them in Panel Preferences.

- **Main Menu** - The standard application menu (LXQt logo button).
- **Quick Launch** - A bar with user-selected launcher icons.
- **Task Manager (X11)** - Classic taskbar showing open windows. Uses EWMH/NETWM.
- **Task Manager (Wayland)** - Wayland-native taskbar using compositor `wlr-foreign-toplevel` protocol.
- **Desktop Switch** - Virtual desktop pager/switcher.
- **System Tray** - Status notifier protocol / freedesktop system tray.
- **Volume Control** - ALSA/PulseAudio/PipeWire volume slider.
- **Network Monitor** - Real-time network traffic graph.
- **CPU Monitor** - CPU usage graph and frequency display.
- **Memory Monitor** - Memory and swap usage graph.
- **Sensors** - Hardware temperature, fan speed, and voltage (requires `lm-sensors`).
- **Mount** - Removable device mount/unmount plugin.
- **Keyboard Layout** - Switch between configured keyboard layouts.
- **Clock** - Date, time, and calendar (customizable format).
- **Space Filler** - Blank stretchable space for aligning panel items.
- **Show Desktop** - Minimize all windows / show desktop.
- **Screen Grab** - Quick screenshot button.
- **Screen Guard** - Lock screen / screen locker shortcut.
- **Fancy Menu** - An alternative searchable application menu with favorites, recent files, and browsing categories.
- **Status Notifier** - Modern system tray (SNI protocol) for applications like Discord, Telegram, etc.
- **World Clock** - Display time from multiple time zones.

## Terminal Emulators

- **[QTerminal](https://github.com/lxqt/qterminal)** - The default LXQt terminal. Lightweight, drop-down mode, tabs, and extensive customization.
- **[Konsole](https://konsole.kde.org/)** - KDE's powerful terminal emulator. Tabs, split views, profiles, and full Qt integration.
- **[Alacritty](https://alacritty.org/)** - GPU-accelerated terminal emulator with Vi mode. Works on both X11 and Wayland.
- **[Kitty](https://sw.kovidgoyal.net/kitty/)** - Fast, feature-rich GPU terminal with native Wayland support, tabs, and image rendering.
- **[Foot](https://codeberg.org/dnkl/foot)** - A lightweight Wayland-native terminal emulator. Minimal dependencies, fast.
- **[Sakura](https://launchpad.net/sakura)** - A GTK-based terminal using VTE. Lightweight and tabbed.
- **[Terminator](https://gnome-terminator.org/)** - GTK-based terminal with grid-based multi-terminal layouts.
- **[XTerm](https://invisible-island.net/xterm/)** - The classic X11 terminal. Extremely lightweight but lacks modern features.

## Software & Applications

Applications that integrate well with the LXQt ecosystem, preferably Qt-based or lightweight.

### Internet & Network

- **[Falkon](https://www.falkon.org/)** - A KDE web browser using QtWebEngine. Very lightweight and fast.
- **[qutebrowser](https://qutebrowser.org/)** - A keyboard-driven, vim-like browser based on QtWebEngine. Highly scriptable.
- **[Angelfish](https://invent.kde.org/network/angelfish)** - A mobile-focused QtWebEngine browser (works on desktop too).
- **[qBittorrent](https://www.qbittorrent.org/)** - A cross-platform BitTorrent client with a Qt interface.
- **[Transmission-qt](https://transmissionbt.com/)** - A lightweight, cross-platform BitTorrent client (Qt GUI version).
- **[Trojitá](https://trojita.flaska.net/)** - A fast Qt IMAP e-mail client.
- **[Thunderbird](https://www.thunderbird.net/)** - Full-featured email client (uses Qt integration via system theme).
- **[NetworkManager-qt](https://invent.kde.org/plasma/networkmanager-qt)** - Qt bindings for NetworkManager; used by `lxqt-config` for WiFi.
- **[Connman-qt](https://github.com/lxqt/connman-qt)** - Qt frontend for ConnMan (alternative lightweight network manager).
- **mu4e / notmuch** (Emacs) - Email clients inside Emacs. `mu4e` is a fast, modern email client built on the `mu` mail indexer; `notmuch` offers tag-based email organization. Both integrate with `afew` for auto-tagging and `msmtp` for sending. Ideal for keyboard-driven email without leaving Emacs.

### Multimedia

- **[VLC media player](https://www.videolan.org/vlc/)** - Free and open-source cross-platform multimedia player (Qt interface).
- **[SMPlayer](https://www.smplayer.info/)** - Qt frontend for mpv with advanced subtitle and playback controls.
- **[Strawberry](https://www.strawberrymusicplayer.org/)** - A music player and collection organizer aimed at audiophiles. Qt-based.
- **[Cantata](https://github.com/CDrummond/cantata)** - A graphical Qt client for MPD (Music Player Daemon).
- **[qmmp](https://qmmp.ylsoftware.com/)** - Qmmp is an audio player with Winamp/XMMS-like interface, Qt-based.
- **[Sayonara Player](https://sayonara-player.com/)** - A small, clear, and fast Qt audio player.
- **[Elisa](https://invent.kde.org/multimedia/elisa)** - KDE's music player with a modern Qt interface and Phonon/VLC backend.
- **[Kid3](https://kid3.kde.org/)** - Qt-based audio tag editor for MP3, FLAC, Ogg, etc.
- **[Audacious](https://audacious-media-player.org/)** - An audio player with GTK and Qt interfaces; very lightweight.
- **[Kdenlive](https://kdenlive.org/)** - A full-featured Qt-based video editor.
- **[mpv](https://mpv.io/)** - A powerful command-line video player with Qt-based GUI wrappers (like `mpv-qt` or `baka-mplayer`).
- **[Haruna](https://invent.kde.org/multimedia/haruna)** - A Qt/KDE mpv frontend with playlist support.
- **[QPWGraph](https://github.com/rncbc/qpwgraph)** - PipeWire graph manager (like pavucontrol but for PipeWire's routing graph). Qt-based.
- **EMMS** (Emacs) - Emacs Multimedia System. A music player inside Emacs that plays local files, streams, and playlists via external backends (mpv, vlc, mplayer). Integrates with `bongo` for a jukebox-style interface.
- **Elfeed** (Emacs) - A web feed reader for Emacs. Download and read RSS/Atom feeds entirely within Emacs. Supports filtering, tagging, and offline reading. Can be paired with `elfeed-org` for organized feed trees.

### Graphics & Image

- **[lximage-qt](https://github.com/lxqt/lximage-qt)** - Default image viewer; also handles screenshots.
- **[gwenview](https://invent.kde.org/graphics/gwenview)** - KDE's fast image viewer with basic editing.
- **[nomacs](https://nomacs.org/)** - A lightweight Qt image viewer with RAW support.
- **[Krita](https://krita.org/en/)** - A professional digital painting app (Qt-based).
- **[Inkscape](https://inkscape.org/)** - Vector graphics editor (uses GTK but works well).
- **[GIMP](https://www.gimp.org/)** - Raster graphics editor (GTK; runs fine on LXQt).
- **[digiKam](https://www.digikam.org/)** - Professional photo management (Qt-based).
- **[Flameshot](https://flameshot.org/)** - Powerful screenshot tool with annotation features (Qt-based). Works on X11 and Wayland.
- **[KolourPaint](https://invent.kde.org/graphics/kolourpaint)** - A simple drawing/paint application for KDE (Qt).
- **[KColorChooser](https://invent.kde.org/graphics/kcolorchooser)** - Simple color picker.
- **[ImComp](https://imcomp.sourceforge.io/)** - Qt image viewer and converter with batch processing.

### Office & Productivity

- **[FeatherPad](https://github.com/tsujan/FeatherPad)** - A lightweight Qt plain text editor with syntax highlighting.
- **[FeatherNotes](https://github.com/tsujan/FeatherNotes)** - A lightweight Qt hierarchical notes manager with Markdown and rich text support.
- **[QOwnNotes](https://www.qownnotes.org/)** - Open-source note-taking with Markdown support and NextCloud/OwnCloud integration (Qt).
- **[Joplin](https://joplinapp.org/)** - Note-taking and to-do app with Markdown. Desktop app uses Qt.
- **[Zettlr](https://zettlr.com/)** - Markdown editor for academic writing (works well on LXQt).
- **[Calibre](https://calibre-ebook.com/)** - E-book library manager and reader (Qt-based).
- **[Okular](https://okular.kde.org/)** - KDE's universal document viewer (PDF, ePub, DjVu, etc.).
- **[qpdfview](https://launchpad.net/qpdfview)** - A tabbed PDF viewer using Qt.
- **[LibreOffice](https://www.libreoffice.org/)** - Full office suite. Uses Qt integration via `libreoffice-qt5`/`libreoffice-qt6` for native look.
- **[TeXstudio](https://www.texstudio.org/)** - LaTeX editor with Qt interface.
- **[LyX](https://www.lyx.org/)** - Document processor using LaTeX backend, Qt interface.
- **[Zotero](https://www.zotero.org/)** - Reference management software (uses Qt for its standalone app).
- **Org-mode** (Emacs) - A powerful Emacs major mode for note-taking, task management, calendaring, and literate programming. Use org-capture for quick notes from LXQt global shortcuts, org-agenda for daily planning, and org-roam for interlinked knowledge management. Write your entire Emacs config as an Org file (`init.org` → `init.el`) for self-documenting dotfiles.

### Utilities

- **[Ark](https://invent.kde.org/utilities/ark)** - KDE's archive manager. Qt-based, handles zip/tar/7z/rar.
- **[KDiskMark](https://github.com/JonMagon/KDiskMark)** - A disk benchmark utility with a Qt GUI (like CrystalDiskMark).
- **[KFind](https://invent.kde.org/utilities/kfind)** - File search utility.
- **[KCalc](https://invent.kde.org/utilities/kcalc)** - Scientific calculator for KDE.
- **[Qalculate!](https://qalculate.github.io/)** - Multi-purpose calculator with Qt GUI.
- **[SpeedCrunch](https://speedcrunch.org/)** - A fast, high-precision scientific calculator (Qt).
- **[BleachBit](https://www.bleachbit.org/)** - System cleaner (GTK; works fine).
- **[qFlipper](https://github.com/flipperdevices/qFlipper)** - Device management for Flipper Zero (Qt).
- **[GPicView](https://lxde.org/gpicview/)** - Simple GTK image viewer from LXDE; usable as minimal fallback.
- **[Rymd](https://github.com/ssansoni/rymd)** - A pleasant Qt network connectivity monitor.

### CLI & TUI Utilities

For power users who live in the terminal alongside their LXQt desktop.

- **[htop](https://htop.dev/)** - Interactive process viewer and system monitor.
- **[btop](https://github.com/aristocratos/btop)** - A modern, visually appealing system monitor (C++).
- **[ranger](https://github.com/ranger/ranger)** - A VIM-inspired file manager with a curses interface.
- **[yazi](https://github.com/sxyazi/yazi)** - A blazing fast terminal file manager written in Rust, based on async I/O.
- **[lf](https://github.com/gokcehan/lf)** - A terminal file manager inspired by ranger written in Go.
- **[Neovim](https://neovim.io/)** - Vim-fork focused on extensibility and usability.
- **[Helix](https://helix-editor.com/)** - A post-modern modal text editor written in Rust.
- **[tmux](https://github.com/tmux/tmux)** - A terminal multiplexer.
- **[zellij](https://zellij.dev/)** - A terminal workspace with batteries included.
- **[ncmpcpp](https://github.com/ncmpcpp/ncmpcpp)** - A feature-rich ncurses client for MPD (Music Player Daemon).
- **[pulsemixer](https://github.com/GeorgeFilipkin/pulsemixer)** - A CLI and curses mixer for PulseAudio (and PipeWire).
- **[nmtui](https://networkmanager.dev/docs/api/latest/nmtui.html)** - A Text User Interface for controlling NetworkManager.
- **[fastfetch](https://github.com/fastfetch-cli/fastfetch)** - Like neofetch, but much faster because it's written in C.

## Compositing

### X11 Compositors

If your X11 window manager (e.g., Openbox) lacks built-in compositing, add transparency, shadows, and effects with these:

- **[Picom](https://github.com/yshui/picom)** - The de-facto compositor for X11 ricing. Highly configurable (shadows, fading, blur, rounded corners, kawase blur).
- **[xcompmgr](https://gitlab.freedesktop.org/xorg/app/xcompmgr)** - Minimal composite manager; very simple, very lightweight.
- **[compton](https://github.com/chjj/compton)** - Original fork predecessor to Picom. Superseded but still functional.
- **[dcompmgr](https://github.com/lspitzner/dcompmgr)** - A simple, fast compositor with minimal configuration.

### Wayland Compositing Features

Wayland compositors have compositing built in. Here are extensions and tools to enhance or configure visual quality:

- **[wlsunset](https://sr.ht/~kennylevinsen/wlsunset/)** - Adjust screen temperature based on time-of-day (redshift alternative for Wayland wlroots compositors).
- **[gammastep](https://gitlab.com/chinstrap/gammastep)** - A Wayland-compatible fork of redshift that adjusts color temperature automatically.
- **[wlam](https://github.com/majian159/wlam)** - Animated wallpaper manager for wlroots compositors.
- **[KDE Color Corrector](https://invent.kde.org/plasma/kwin/blob/master/src/plugins/kdecorrelation/)** - Night Light feature in KWin for blue light filtering.

**Compositing in specific compositors:**

- **KWin (Wayland)**: Built-in blur, transparency, window effects, and slide animations. Configure via `kwin` settings GUI or `kwinrulesrc`.
- **Hyprland**: Highly customizable compositing — `blur:enabled = true`, `blur:new_optimizations = on`, `animations:enabled = true`, `decoration:drop_shadow = true`, `decoration:rounding = 10`.
- **Wayfire**: Plugin-based compositing effects — `blur`, `csd`, `alpha`, `animation`, `scale`, `switcher`, `cube`, `water`, `fire`. Enable/disable in `wayfire.ini`.
- **Labwc**: Minimal compositing on purpose (no built-in blur). Rely on client-side decorations for visuals.
- **Sway**: Minimal compositing by default. Add blur via `sway-blur` patch (custom build) or use `hyprland` for advanced effects.

## Display Managers

Display managers (login screens) that work well with LXQt:

- **[SDDM](https://github.com/sddm/sddm)** - The recommended display manager for LXQt. Qt-based, themeable, and supports both X11 and Wayland sessions. LXQt provides official SDDM themes.
- **[SDDM Configuration Tool](https://github.com/sddm/sddm-kcm)** - KCM module for configuring SDDM; works on LXQt with `systemsettings`.
- **[LightDM](https://github.com/canonical/lightdm)** - A lightweight, cross-desktop display manager. Works with LXQt via `lightdm-gtk-greeter` or `lightdm-qt-greeter`.
- **[LightDM GTK Greeter](https://github.com/linuxmint/lightdm-settings)** - The standard GTK greeter for LightDM. Lightweight and functional.
- **[LightDM WebKit Greeter](https://github.com/Antergos/web-greeter)** - A more visually customizable greeter with HTML/JS theming.
- **[LXDM](https://sourceforge.net/projects/lxdm/)** - The old LXDE display manager. Extremely lightweight, but no Wayland session support.
- **[CDM](https://github.com/evertiro/cdm)** - A minimal, console-based display manager. No X11/Wayland dependency, purely TTY.
- **[Ly](https://github.com/fairyglade/ly)** - A modern TUI display manager written in Rust with X11 and Wayland session support.
- **[emptty](https://github.com/tvrzna/emptty)** - A simple CLI display manager with X11 and Wayland support.
- **[greetd](https://sr.ht/~kennylevinsen/greetd/)** - A minimal, agnostic display manager daemon. Supports multiple greeters (GTK, Qt, TUI, etc.).

## Screen Lockers

- **[lxqt-sudo's lock](https://github.com/lxqt/lxqt-sudo)** - LXQt relies on its built-in screen locker integration. On X11, `xdg-screensaver` or `xscreensaver-command -lock`.
- **[xscreensaver](https://www.jwz.org/xscreensaver/)** - Classic X11 screen locker with a vast collection of screensavers (can lock via `xscreensaver-command -lock`).
- **[i3lock](https://github.com/i3/i3lock)** - Simple X11 screen locker used by i3. Minimal, no frills.
- **[i3lock-color](https://github.com/Raymo111/i3lock-color)** - A fork of i3lock with more customization (background images, clock, indicators).
- **[xsecurelock](https://github.com/dimkr/xsecurelock)** - An X11 screen locker designed for security and modularity (auth modules).
- **[betterlockscreen](https://github.com/betterlockscreen/betterlockscreen)** - Beautiful lock screen with blur effects (wraps i3lock-color).
- **[swaylock](https://github.com/swaywm/swaylock)** - The standard Wayland screen locker for wlroots compositors.
- **[swaylock-effects](https://github.com/mortie/swaylock-effects)** - A fork of swaylock with blur, brightness, and other effects.
- **[waylock](https://codeberg.org/ifreund/waylock)** - A minimal, secure screen locker for Wayland compositors.
- **[hyprlock](https://github.com/hyprwm/hyprlock)** - Hyprland's eye-candy screen locker with blur, background images, and multi-monitor support.

## Polkit Authentication Agents

PolicyKit agents grant privilege elevation for system tasks. LXQt needs one running for admin operations:

- **[lxqt-policykit](https://github.com/lxqt/lxqt-policykit)** - LXQt's own PolicyKit agent. Lightweight, native Qt, and the recommended choice.
- **[polkit-kde-agent](https://invent.kde.org/plasma/polkit-kde-agent-1)** - KDE's Polkit agent. Feature-rich and integrates well with Qt desktops.
- **[polkit-gnome](https://gitlab.gnome.org/GNOME/polkit-gnome)** - The standard GNOME Polkit agent. Works fine on LXQt.
- **[lxpolkit](https://wiki.lxde.org/en/LXPolkit)** - The old LXDE polkit agent. Minimal GTK-based agent.
- **[mate-polkit](https://github.com/mate-desktop/mate-polkit)** - MATE's polkit agent. Lightweight and functional.
- **[xfce-polkit](https://github.com/nicknisi/xfce-polkit)** - A lightweight polkit agent for Xfce. Works well on LXQt too.

## Clipboard Managers

- **[CopyQ](https://hluk.github.io/CopyQ/)** - Highly feature-rich Qt clipboard manager with search, editing, scripting, and history (X11 & Wayland via wl-clipboard).
- **[cliphist](https://github.com/sentriz/cliphist)** - A clipboard manager for Wayland using wl-clipboard. Simple, text + images.
- **[clipman](https://github.com/bugaevc/wl-clipboard)** - A clipboard manager for wl-clipboard with history (Wayland).
- **[wl-clipboard](https://github.com/bugaevc/wl-clipboard)** - A command-line clipboard utility for Wayland (`wl-copy`, `wl-paste`). Required backend for many tools.
- **[clipmenu](https://github.com/cdown/clipmenu)** - A clipboard manager using dmenu/rofi (X11; works with Xclip).
- **[xclip](https://github.com/astrand/xclip)** - Command-line X11 clipboard utility.
- **[xsel](https://github.com/kfish/xsel)** - Another command-line X11 clipboard tool.
- **[autocutsel](https://www.nongnu.org/autocutsel/)** - Syncs X11 PRIMARY and CLIPBOARD selections.
- **[greenclip](https://github.com/erebe/greenclip)** - A simple clipboard manager for rofi (X11).

## Screenshot & Screen Recording

- **[screengrab](https://github.com/lxqt/screengrab)** - LXQt's own screenshot tool. Works on X11 and Wayland.
- **[Flameshot](https://flameshot.org/)** - Feature-rich Qt screenshot tool with annotation, blur, and upload (X11 & Wayland).
- **[Spectacle](https://invent.kde.org/graphics/spectacle)** - KDE's screenshot utility. Excellent features; native Qt.
- **[Kazam](https://github.com/hzbd/kazam)** - Simple screen recording tool (GTK, but works well).
- **[OBS Studio](https://obsproject.com/)** - Professional streaming and recording software (Qt-based). Full Wayland support via pipewire capture.
- **[wf-recorder](https://github.com/ammen99/wf-recorder)** - Wayland-native screen recording utility for wlroots compositors.
- **[grim](https://github.com/emersion/grim)** - A command-line screenshot tool for Wayland wlroots compositors.
- **[slurp](https://github.com/emersion/slurp)** - A screen area selection tool for Wayland (used with grim).
- **[swappy](https://github.com/jtheoof/swappy)** - A screenshot tool for Wayland (grim frontend) with annotation.
- **[maim](https://github.com/naelstrof/maim)** - A command-line screenshot tool for X11.
- **[xfce4-screenshooter](https://docs.xfce.org/apps/xfce4-screenshooter/start)** - Lightweight screenshot tool (works outside Xfce).
- **[peek](https://github.com/phw/peek)** - Simple animated GIF screen recorder (GTK, but easy to use).

## OSD (On-Screen Display)

Volume, brightness, and media OSD utilities for LXQt:

- **[lxqt-notificationd](https://github.com/lxqt/lxqt-notificationd)** - LXQt's notification daemon doubles as an OSD for volume and brightness changes.
- **[volnoti](https://github.com/darealshinji/volnoti)** - A lightweight volume notification daemon (X11). Shows a volume bar on change.
- **[pasystray](https://github.com/christophgysin/pasystray)** - PulseAudio system tray with volume OSD and per-app volume control (GTK).
- **[swayosd](https://github.com/ErikReider/SwayOSD)** - An OSD for wlroots compositors showing volume, brightness, and caps-lock state.
- **[avizo](https://github.com/PromyLOPh/avizo)** - A simple OSD for PipeWire volume and brightness on Wayland.
- **[wob](https://github.com/francma/wob)** - A lightweight overlay bar for Wayland that displays volume/brightness progress.
- **[brightnessctl](https://github.com/Hummer12007/brightnessctl)** - A command-line brightness control tool; often paired with `wob` or `swayosd` for OSD feedback.
- **[light](https://github.com/haikarainen/light)** - A command-line display brightness controller (X11 and Wayland via `sysfs`/`acpi`).

## Notification Daemons

Replace or complement LXQt's built-in notification system with these:

- **[lxqt-notificationd](https://github.com/lxqt/lxqt-notificationd)** - The default notification daemon shipped with LXQt.
- **[Dunst](https://dunst-project.org/)** - A highly customizable and lightweight notification daemon (X11 & Wayland via layer-shell). Most popular alternative.
- **[Mako](https://github.com/emersion/mako)** - A lightweight notification daemon for Wayland compositors supporting the layer-shell protocol.
- **[Swaync](https://github.com/ErikReider/SwayNotificationCenter)** - A notification daemon for Sway/Wayland with a drop-down notification center.
- **[fnott](https://codeberg.org/dnkl/fnott)** - A lightweight notification daemon for Wayland (from the foot terminal author).
- **[deadd](https://github.com/phuhl/linux_notification_center)** - A notification daemon with a notification center and history UI.
- **[statnot](https://github.com/dmedvinsky/statnot)** - A notification daemon that prints notifications to stdout (scripting-friendly).

## Application Launchers

Alternatives to `lxqt-runner` for a more customized application menu or search interface:

- **[lxqt-runner](https://github.com/lxqt/lxqt-runner)** - The default LXQt runner. Simple and integrated.
- **[Rofi](https://github.com/davatorium/rofi)** - A window switcher, application launcher, and dmenu replacement. Works on X11; Wayland forks available (`rofi-wayland`, `rofi-lbonn-wayland`).
- **[Rofi (Wayland fork)](https://github.com/lbonn/rofi)** - Rofi fork with Wayland support (layer-shell protocol).
- **[Wofi](https://hg.sr.ht/~scoopta/wofi)** - A launcher/menu program for wlroots-based Wayland compositors (rofi-like).
- **[Fuzzel](https://codeberg.org/dnkl/fuzzel)** - A Wayland-native application launcher, similar to rofi's dmenu mode.
- **[Albert](https://albertlauncher.github.io/)** - A fast, extensible keyboard launcher with plugins (works on X11 and Wayland).
- **[Ulauncher](https://ulauncher.io/)** - An application launcher with a modern UI, extensions, and file search.
- **[KRunner](https://invent.kde.org/plasma/krunner)** - KDE's powerful launcher (can be used standalone on LXQt).
- **[dmenu](https://tools.suckless.org/dmenu/)** - The classic suckless dynamic menu (X11).
- **[bemenu](https://github.com/Cloudef/bemenu)** - A dmenu-like menu for Wayland (wlroots).
- **[nwg-launchers](https://github.com/nwg-piotr/nwg-launchers)** - A GTK-based launcher suite for Sway: application grid, task bar, and bar.

## Alternative Panels & Bars

For those who prefer a scriptable or minimalist bar over `lxqt-panel`:

- **[lxqt-panel](https://github.com/lxqt/lxqt-panel)** - The default LXQt panel. Supports X11 and Wayland.
- **[Polybar](https://polybar.github.io/)** - A fast and easy-to-use status bar (X11). Extremely popular in ricing communities.
- **[Waybar](https://github.com/Alexays/Waybar)** - A highly customizable Wayland bar for wlroots-based compositors (supports layer-shell).
- **[Tint2](https://gitlab.com/o9000/tint2)** - A lightweight, simple panel/taskbar (X11). Very low resource usage.
- **[Lemonbar](https://github.com/LemonBoy/bar)** - A lightweight X11 bar; often scripted with shell or a tool like `bspwmbar`.
- **[Eww](https://elkowar.github.io/eww/)** - A widget system for X11 and Wayland using custom XML/YAML/Rust-based widgets.
- **[i3status-rust](https://github.com/greshake/i3status-rust)** - A highly configurable status bar generator (works with i3, sway, and others).
- **[i3blocks](https://github.com/vivien/i3blocks)** - A flexible status bar for i3/Sway using shell scripts.
- **[aggbar](https://github.com/atx/aggbar)** - A minimal, multi-threaded status bar for Wayland (wlroots).
- **[nwg-panel](https://github.com/nwg-piotr/nwg-panel)** - A GTK3 panel for Sway with system tray, taskbar, and clock.

## Dock Panels

macOS-style application docks for Linux. These show running and pinned applications with icons, often with magnification and animation effects.

### X11 Docks

- **[Plank](https://github.com/ricotz/plank)** - The simplest dock on the planet. Lightweight, fast, and minimal. Used by elementary OS. Vala/GTK3.
- **[Plank Reloaded](https://github.com/zquestz/plank-reloaded)** - Actively maintained fork of Plank with modern docklets, GTK theme support, multi-monitor, and floating dock. X11 only. Vala/GTK3.
- **[Cairo-Dock](https://glx-dock.org/)** - Feature-rich dock with OpenGL/Cairo rendering, animations, applets, and themes. Highly customizable. C/GTK3.
- **[DockbarX](https://github.com/M7S/dockbarx)** - Lightweight taskbar/dock with Windows-style grouped window buttons. Works as standalone dock (DockX), XFCE panel applet, or MATE panel applet. Python/GTK3.
- **[Docky](https://launchpad.net/docky)** - GNOME Do's dock interface. Feature-rich with docklets (CPU monitor, weather, etc.). Vala/GTK3.
- **[Latte Dock](https://invent.kde.org/plasma/latte-dock)** - KDE's feature-rich dock with panels, layouts, and KDE Plasma integration. Discontinued but still functional. C++/Qt.
- **[KSmoothDock](https://github.com/dangrin/ksmoothdock)** - Smooth animated dock for KDE with KDE Plasma integration. C++/Qt.
- **[Polydock](https://github.com/folke/polydock)** - Fast, hackable application dock for tiling WMs (bspwm, i3, xmonad). GTK CSS themeable. TypeScript/GJS.
- **[Winbar](https://github.com/jmanc3/winbar)** - Familiar X11 panel/dock to ease new Linux users' transition. C++.
- **[Crystal Dock](https://github.com/dangvd/crystal-dock)** - Cool dock with smooth parabolic zooming, translucent effects, and four visual styles (Glass 3D, Glass 2D, Flat 2D, Metal 2D). Supports KDE, LXQt, Cinnamon, MATE on X11 (v1). C++/Qt6.
- **[nwg-panel](https://github.com/nwg-piotr/nwg-panel)** - GTK3 panel for Sway with taskbar, system tray, and clock. Can function as a dock. Python/GTK3.

### Wayland Docks

- **[Docklike Taskbar](https://gitlab.com/laborius/docklike-taskbar)** - Wayland-native taskbar/dock for wlroots compositors (Sway, Hyprland, Labwc). Supports window grouping. C++/GTK4.
- **[Crystal Dock](https://github.com/dangvd/crystal-dock)** - Cool dock with smooth parabolic zooming, translucent effects, and four visual styles. v2 supports Hyprland, KDE Plasma 6, Labwc, LXQt, Niri, Sway, and Wayfire on Wayland. C++/Qt6.
- **[Rego](https://git.sr.ht/~stacks/rego)** - Simple, minimal dock for Sway. Wayland-native. Rust.
- **[ags dock](https://github.com/Aylur/ags)** - Part of Aylur's GTK Shell (ags). Create dock-like widgets using GTK4 and JavaScript.
- **[eww dock](https://github.com/elkowar/eww)** - Build dock-like widgets using eww's XML/YAML widget system. Works on X11 and Wayland.
- **[nwg-dock-hyprland](https://github.com/nwg-piotr/nwg-dock-hyprland)** - A dock for Hyprland based on nwg-panel's dock component. Python/GTK3.
- **[eqsh](https://github.com/eq-desktop/eqsh)** - Polished all-in-one Hyprland shell with dock, notifications, and system tray. QML.

### Dock Libraries

- **[libwnck](https://wiki.gnome.org/Projects/Libwnck)** - Window Navigation Construction Kit. Library for building taskbars, pagers, and window lists. X11. GTK3 version: `libwnck-3`.
- **[libbamf](https://launchpad.net/bamf)** - BAMF Application Matching Framework. Matches windows to desktop files and groups windows by application. Used by Unity, Plank, DockbarX. GTK3 version: `libbamf3`.
- **[libwnck-3](https://wiki.gnome.org/Projects/Libwnck)** - GTK3 version of libwnck. Required by Plank, Polydock, and most GTK3-based docks.

## Wallpapers & Backgrounds

Tools to set desktop backgrounds, especially if you bypass `pcmanfm-qt` desktop management:

- **[pcmanfm-qt](https://github.com/lxqt/pcmanfm-qt)** - When desktop management is enabled, it handles wallpaper on both X11 and Wayland.
- **[Nitrogen](https://github.com/l3ib/nitrogen)** - A fast and lightweight background browser and setter for X11.
- **[Feh](https://feh.finalrewind.org/)** - An X11 image viewer commonly used to set backgrounds from scripts.
- **[hsetroot](https://github.com/himdel/hsetroot)** - A simple X11 tool to set root window background with gradients and patterns.
- **[xwallpaper](https://github.com/stoeckmann/xwallpaper)** - A lightweight wallpaper setter for X11.
- **[Swaybg](https://github.com/swaywm/swaybg)** - A wallpaper utility for Wayland wlroots compositors.
- **[Hyprpaper](https://github.com/hyprwm/hyprpaper)** - A blazing-fast Wayland wallpaper utility with IPC controls (for Hyprland and other wlroots compositors).
- **[swaybg](https://github.com/swaywm/swaybg)** - Simple, wlroots-native wallpaper setter (fork).
- **[swww](https://github.com/LGFae/swww)** - An animated wallpaper daemon for Wayland with smooth transitions.
- **[mpvpaper](https://github.com/GhostNaN/mpvpaper)** - Use mpv to play videos as animated wallpaper on Wayland (wlroots).
- **[azote](https://github.com/nwg-piotr/azote)** - A wallpaper manager with GUI (GTK) for Sway and other wlroots compositors.

## Color Management & Dynamic Theming

Tools that auto-generate color palettes from wallpapers and apply them across LXQt:

- **[pywal](https://github.com/dylanaraps/pywal)** - Generates a color palette from a wallpaper and applies it system-wide (X11). Supports terminal, GTK, Qt, and more via templates.
- **[wallust](https://codeberg.org/explosion-mental/wallust)** - A modern Rust rewrite of pywal. Generates color schemes, supports pywal templates, and works on both X11 and Wayland.
- **[wpgtk](https://github.com/deviantfero/wpgtk)** - A GTK-based wallpaper color scheme generator with pywal-style templates.
- **[colorz](https://github.com/metakirby5/colorz)** - A simple color palette extractor from images (used with pywal).
- **[chameleon](https://github.com/eragon512/chameleon)** - A wallpaper color scheme generator with KDE Plasma integration (works for Qt apps too).
- **[Oomox](https://github.com/themix-project/oomox)** - A GUI tool for creating GTK and Qt themes from user-defined colors. Can generate Numix, Materia, and Arc-style themes.
- **[KDE Material You](https://github.com/luisbocanegra/kde-material-you)** - Generates Plasma color schemes from wallpapers; also outputs Kvantum themes.
- **[nwg-shell-hooks](https://github.com/nwg-piotr/nwg-shell-hooks)** - Wallpaper-to-color-scheme automation for Sway/Wayland.

## XDG Desktop Portal

Desktop portals enable sandboxed applications (Flatpak, Snap, etc.) to access system resources (file chooser, screen sharing, printing):

- **[xdg-desktop-portal](https://github.com/flatpak/xdg-desktop-portal)** - The main portal daemon. Required for Flatpak app integration.
- **[xdg-desktop-portal-kde](https://invent.kde.org/plasma/xdg-desktop-portal-kde)** - KDE's backend for xdg-desktop-portal. Best choice for LXQt as it uses Qt/KF5.
- **[xdg-desktop-portal-gtk](https://github.com/flatpak/xdg-desktop-portal-gtk)** - GTK backend for xdg-desktop-portal. Works reliably as a fallback.
- **[xdg-desktop-portal-lxqt](https://github.com/lxqt/xdg-desktop-portal-lxqt)** - LXQt's own portal backend (currently in early development). Native LXQt file chooser dialogs.
- **[xdg-desktop-portal-wlr](https://github.com/emersion/xdg-desktop-portal-wlr)** - Portal backend for wlroots-based Wayland compositors. Required for screen capture/pipewire on Sway, Hyprland, Labwc, etc.

## GTK Integration & Theming

Make GTK applications look at home in LXQt:

- **[lxappearance](https://git.lxde.org/gitweb/?p=lxde/lxappearance.git)** - GTK+ theme switcher (not Qt, but essential for GTK app integration on LXQt).
- **[nwg-look](https://github.com/nwg-piotr/nwg-look)** - A GTK3 settings editor for Sway/Wayland. Can set GTK themes, icons, and fonts.
- **[Qt5 GTK2/3 Platform Theme](https://doc.qt.io/qt-5/qtgtkplatformtheme.html)** - Configures Qt apps to use GTK theme/style (`QT_QPA_PLATFORMTHEME=gtk3` or install `qt5-style-plugins`).
- **[Oxygen-gtk](https://invent.kde.org/plasma/oxygen-gtk)** - GTK theme that matches the Oxygen Qt style.
- **[Breeze GTK](https://invent.kde.org/plasma/breeze-gtk)** - GTK theme matching KDE's Breeze. Perfect for LXQt if using Breeze Qt theme.
- **[Adwaita-qt](https://github.com/FedoraQt/adwaita-qt)** - A Qt theme matching GNOME's Adwaita. Makes Qt apps blend in with GTK apps using Adwaita.

## Service Integration

### Audio

- **[PulseAudio](https://www.freedesktop.org/wiki/Software/PulseAudio/)** - The legacy sound server. LXQt volume plugin supports it directly.
- **[PipeWire](https://pipewire.org/)** - The modern audio/video routing service. Replaces PulseAudio. LXQt 2.0+ works well with PipeWire.
- **[pavucontrol](https://freedesktop.org/software/pulseaudio/pavucontrol/)** - PulseAudio/PipeWire volume control GUI (GTK, standard).
- **[pavucontrol-qt](https://github.com/lxqt/pavucontrol-qt)** - Qt port of pavucontrol. Native LXQt look.
- **[QPWGraph](https://github.com/rncbc/qpwgraph)** - PipeWire graph routing GUI. Qt-based, excellent for pro audio.
- **[Helvum](https://gitlab.freedesktop.org/pipewire/helvum)** - GTK-based PipeWire patchbay.

### Network

- **[NetworkManager](https://networkmanager.dev/)** - The standard network management service. Integrated via `nm-tray` or `lxqt-config` network module.
- **[nm-tray](https://github.com/linuxmint/nm-tray)** - A NetworkManager system tray applet (Qt-based), works well as a lightweight alternative to KDE's plasma-nm.
- **[ConnMan](https://01.org/connman)** - A lightweight network manager for embedded/desktop. LXQt has `connman-qt` frontend.
- **[connman-qt](https://github.com/lxqt/connman-qt)** - LXQt's ConnMan UI.
- **[netctl](https://wiki.archlinux.org/title/netctl)** - Command-line network manager used on Arch Linux; scriptable.
- **[wicd](https://wiki.archlinux.org/title/Wicd)** - Legacy lightweight network manager (GTK, but works).

### Bluetooth

- **[BlueDevil](https://invent.kde.org/plasma/bluedevil)** - KDE's Bluetooth stack integration. Works well with LXQt as a system tray applet.
- **[Blueman](https://github.com/blueman-project/blueman)** - GTK-based Bluetooth manager. Feature-rich and reliable.

### Printing

- **[system-config-printer](https://github.com/OpenPrinting/system-config-printer)** - GTK-based printer configuration tool (standard for CUPS management).
- **[print-manager](https://invent.kde.org/utilities/print-manager)** - KDE's print manager with Qt interface. System tray applet and job viewer.

### Power Management

- **[lxqt-powermanagement](https://github.com/lxqt/lxqt-powermanagement)** - LXQt's own power management handler.
- **[xfce4-power-manager](https://docs.xfce.org/xfce/xfce4-power-manager/start)** - Xfce's power manager with battery icon and lid close settings (GTK, but works well).
- **[TLP](https://linrunner.de/tlp/)** - Advanced power management for laptops, no GUI but highly effective.
- **[powertop](https://github.com/fenrus75/powertop)** - Intel's power consumption diagnostic tool.

## How to Customize LXQt Desktop

LXQt is highly modular, meaning it relies on various underlying components and standards (like XDG) to function. Unlike heavier desktop environments (like KDE Plasma or GNOME) that provide integrated settings for everything, LXQt delegates many tasks to specific low-level tools. 

To properly customize LXQt, you need to understand the dependencies and why they are required.

### 1. The Core GUI Toolkit: Qt

LXQt is built on Qt. Therefore, its appearance is dictated by Qt's rendering engine.

- **Dependency needed:** `qt5ct` (Qt5 Configuration Tool) and `qt6ct` (Qt6 Configuration Tool).
- **Why?** LXQt natively provides a basic Appearance Configuration tool, but `qt5ct`/`qt6ct` offer more robust control over fonts, icon themes, and Qt style plugins globally across all Qt apps regardless of DE.
- **Low-level setup:** You MUST export the environment variables for Qt to respect these tools. 
  - Add to `~/.config/lxqt/session.conf` or your `~/.profile`:
    ```bash
    export QT_QPA_PLATFORMTHEME=qt5ct
    # or for Qt6:
    export QT_QPA_PLATFORMTHEME=qt6ct
    ```

### 2. Theming Engine: Kvantum

By default, Qt themes can look outdated (like Windows 95). To get modern, SVG-based, rounded, or translucent themes, you need Kvantum.

- **Dependency needed:** `kvantum` (and `kvantum-qt6`).
- **Why?** Kvantum is an SVG-based theme engine for Qt. It allows theme developers to create complex, pixel-perfect themes (like sweet, dracula, or macOS-like themes).
- **How to apply:** 
  1. Open `qt5ct` / `qt6ct`.
  2. Set the "Style" to `kvantum`.
  3. Open the `Kvantum Manager` app to select your actual theme (e.g., `KvGlass`).

### 3. Window Manager Theming (Openbox / KWin)

LXQt does NOT draw window borders or handle window snapping; it delegates this to the Window Manager.

- **If using Openbox (X11):** 
  - **Dependency:** `obconf-qt`.
  - **Why?** You need Openbox themes (usually downloaded to `~/.themes`) to change the title bar and window borders. Openbox handles the window decorations separately from the Qt widgets inside the window.
- **If using KWin (X11/Wayland):**
  - **Dependency:** `systemsettings` (KDE settings) or edit `kdeglobals`.
  - **Why?** KWin uses Aurorae for window decorations.

### 4. Compositing & Effects (Shadows, Blur, Transparency)

LXQt does not composite the screen. If you see tearing, lack of shadows, or solid black backgrounds behind rounded corners, you lack a compositor.

- **X11 Dependency:** `picom` (or `compton`).
  - **Why?** Picom draws shadows around Openbox windows, provides true transparency to terminals, and allows background blur (especially useful for a translucent LXQt panel).
  - **How:** Add `picom -b` to your LXQt Session Autostart. Configure blur and shadows in `~/.config/picom/picom.conf`.
- **Wayland Dependency:** The compositor handles this natively (e.g., Labwc, Wayfire).

### 5. Icons and Fonts

- **Dependency:** An icon set (e.g., Papirus, Tela) installed in `~/.local/share/icons/` or `/usr/share/icons/`.
- **Why?** LXQt relies heavily on the XDG icon specification. Without a complete icon theme, the panel, PCManFM-Qt, and app launcher will show missing icons.
- **Fonts:** Configure your default fonts and, importantly, anti-aliasing/hinting in the LXQt Appearance module.

### 6. Dynamic Colors and GTK Integration

Since you will likely run GTK apps (like Firefox or GIMP) inside LXQt, you need them to match your Qt theme.

- **Dependency:** `lxappearance` or `nwg-look` (Wayland).
- **Why?** These tools configure `~/.gtkrc-2.0` and `~/.config/gtk-3.0/settings.ini`. Qt and GTK do not share theming natively. You must pick a GTK theme (like Arc or Materia) that closely resembles your Kvantum theme.
- **Color scripts:** Tools like `pywal` can generate colors from your wallpaper, but applying them to LXQt requires generating a custom `.qss` (Qt StyleSheet) file and reloading the LXQt panel.

### 7. The LXQt Panel & QSS

The panel itself (`lxqt-panel`) is themed using standard CSS-like syntax called QSS (Qt Style Sheets).
- **Location:** `~/.config/lxqt/lxqt-panel.qss`
- **Why?** If you want to change the border radius of the start menu, the padding of the taskbar buttons, or the background color of the panel, you do it by editing the active QSS file.

## Low-Level Dependencies & Libraries

Every application recommended in this list ultimately depends on a set of core C/C++ shared libraries. Understanding these helps with dependency troubleshooting, system trimming, and manual installs.

### GTK Stack (libgtk, libglib, libcairo, etc.)

All GTK-based apps (GIMP, Inkscape, pavucontrol, Blueman, Sakura, Terminator, etc.) share this dependency chain:

| Library | Role | Typical consumers |
|---|---|---|
| `libglib-2.0` | Core data types, event loop, threading | Every GTK app |
| `libgobject-2.0` | GObject type/object system | Every GTK app |
| `libgio-2.0` | VFS, D-Bus, file monitoring | Every GTK app |
| `libgtk-3` / `libgtk-4` | Widget toolkit | Every GTK app |
| `libgdk-3` / `libgdk-4` | Windowing abstraction (X11/Wayland) | Every GTK app |
| `libgdk_pixbuf-2.0` | Image loading (PNG, JPEG, etc.) | GIMP, GPicView, lxappearance |
| `libpango-1.0` / `libpangocairo-1.0` | Text layout + Cairo rendering | Every GTK app |
| `libcairo` | 2D vector rendering | Every GTK app, picom |
| `libatk-1.0` / `libatk-bridge` | Accessibility | nwg-panel, nwg-launchers |
| `libharfbuzz` | Text shaping (ICU shaper) | Every GTK app |
| `libfreetype` / `libfontconfig` | Font loading & matching | Every GTK app |
| `libvte` (libvte-2.91) | Terminal emulator widget | Sakura, Terminator |
| `librsvg-2` | SVG rendering | lxappearance, Oomox |
| `libpangoft2` | FreeType backend for Pango | Every GTK app |
| `libpeas-1.0` | Plugin system (GObject-based) | Various GTK apps |
| `libjson-glib-1.0` | JSON parsing | nwg-launchers, azote |
| `libsoup-2.4` / `libsoup-3.0` | glib-based HTTP client | GTK apps needing HTTP |
| `libgudev-1.0` | udev device enumeration | Blueman, system-config-printer |
| `libnotify` | Desktop notification bubbles | notify-send, various GTK apps |

These all sit on top of `libx11`/`libxcb` (X11) or `libwayland-client` (Wayland).

### Qt Stack (libQt5, libQt6, liblxqt, etc.)

LXQt is a Qt-first desktop. All lxqt-* modules and recommended Qt apps (qBittorrent, FeatherPad, Flameshot, Strawberry, etc.) link these:

| Library | Role | Typical consumers |
|---|---|---|
| `libQt5Core` / `libQt6Core` | Core (QObject, containers, threads, JSON, XML) | Every Qt app |
| `libQt5Gui` / `libQt6Gui` | Windowing, images, fonts, text layout | Every Qt app |
| `libQt5Widgets` / `libQt6Widgets` | Widget toolkit | Most Qt apps |
| `libQt5Network` / `libQt6Network` | TCP/HTTP/DNS | qBittorrent, Trojità, qutebrowser |
| `libQt5DBus` / `libQt6DBus` | D-Bus IPC binding | lxqt-panel, nm-tray, connman-qt |
| `libQt5Xml` / `libQt6Xml` | XML parsing | Various Qt apps |
| `libQt5Svg` / `libQt6Svg` | SVG rendering | Kvantum themes, lximage-qt |
| `libQt5Sql` / `libQt6Sql` | SQL database (SQLite, PostgreSQL) | Cantata, Strawberry |
| `libQt5Concurrent` / `libQt6Concurrent` | Parallel map/reduce | digiKam, Krita |
| `libQt5Multimedia` / `libQt6Multimedia` | Audio/video playback | Elisa, qmmp |
| `libQt5WebEngine` / `libQt6WebEngine` | Chromium-based browser engine | qutebrowser, Falkon, Angelfish |
| `libQt5WebEngineWidgets` | WebEngine + Widgets glue | qutebrowser, Falkon |
| `libQt5WaylandClient` / `libQt6WaylandClient` | Wayland platform plugin | All Wayland Qt apps |
| `libQt5XcbQpa` / `libQt6XcbQpa` | X11 platform plugin | All X11 Qt apps |
| `libQt5Sensors` / `libQt6Sensors` | Hardware sensor readings | Various |
| `libQt5Bluetooth` / `libQt6Bluetooth` | Bluetooth stack (Qt) | Various |
| `libQt5Positioning` / `libQt6Positioning` | Geolocation | Various |
| `libQt5Qml` / `libQt6Qml` | QML engine | Some Qt Quick apps |

**LXQt-specific Qt libraries:**

| Library | Role | Consumers |
|---|---|---|
| `liblxqt` | LXQt base (config, logging, window system) | All `lxqt-*` modules |
| `liblxqt-globalkeys` | Global keyboard shortcuts | lxqt-panel, lxqt-runner |
| `libqtermwidget5` | Terminal widget for embedding | QTerminal, QTermWidget |
| `libfm-qt` | Qt binding of libfm (file management) | pcmanfm-qt |
| `libqtxdg` | XDG desktop entry + MIME handling | pcmanfm-qt, lxqt-archiver |
| `libpolkit-qt5` / `libpolkit-qt6` | Polkit Qt binding | lxqt-policykit |
| `libstatgrab` | System statistics | lxqt-panel sensors plugin |
| `libsensors` (lm-sensors) | Hardware sensor access | lxqt-panel sensors plugin |

**KDE Frameworks libraries** — used by KDE-origin apps that run on LXQt (Krita, digiKam, Ark, Okular):

| Library | Role | Consumers |
|---|---|---|
| `libKF5Config` / `libKF6Config` | KConfig (INI/KConfig XT) | Krita, digiKam, Ark, Okular |
| `libKF5I18n` / `libKF6I18n` | i18n/translation framework | KDE apps |
| `libKF5WindowSystem` / `libKF6WindowSystem` | NETWM/EWMH abstraction | KWin panel backend |
| `libKF5Notifications` / `libKF6Notifications` | KNotification daemon | print-manager, Spectacle |
| `libKF5Solid` / `libKF6Solid` | Hardware discovery | Ark, print-manager, KDE apps |
| `libKF5SyntaxHighlighting` | Syntax highlighting engine | FeatherPad (optional), KDE apps |
| `libKDecoration2` | KWin window decoration API | KWin Aurorae themes |

### Windowing & Display System

The lowest graphics/windowing libraries that everything ultimately calls:

| Library | Role |
|---|---|
| `libwayland-client` / `libwayland-server` | Core Wayland protocol (event loop, shm, registry) |
| `libwayland-cursor` / `libwayland-egl` | Wayland cursor images + EGL surface integration |
| `libwlroots` | Compositor toolkit: wlr_output, wlr_input, wlr_scene, wlr_xdg_shell, etc. (used by Labwc, Sway, Wayfire, Hyprland, river, dwl) |
| `libdrm` | Direct Rendering Manager – KMS modesetting, buffer allocation |
| `libgbm` | Generic Buffer Manager – buffer import/export with mesa |
| `libinput` | Input device handling (evdev, libinput events, gestures) |
| `libxkbcommon` | Keyboard layout / XKB state machine |
| `libseat` | Seat management (seatd or logind) |
| `libdisplay-info` | EDID parsing for monitor names, physical size, HDR metadata |
| `libliftoff` | Plane-optimized KMS compositing (atomic page-flip) |
| `libx11` / `libxcb` | X11 protocol C bindings |
| `libxext` / `libxfixes` / `libxdamage` | X11 extensions used by compositors (picom) |
| `libxrender` / `libxcomposite` | X11 rendering + composite redirection |
| `libxrandr` | X11 Resize and Rotate (monitor config) |
| `libxss` / `libXScrnSaver` | X11 screen saver control |
| `libxpresent` | X11 Present extension (tear-free) |
| `libxcursor` / `libxft` | X11 cursor + font rendering |
| `libxinerama` | Multi-monitor (legacy) |

### Graphics / GPU

| Library | Role |
|---|---|
| `libEGL` (libEGL_mesa) | EGL native platform interface (Wayland compositors, GPU rendering) |
| `libGLESv2` / `libGL` | OpenGL ES 2.0 / full OpenGL |
| `libgbm` (already listed) | GBM buffer allocation (EGL native platform for KMS) |
| `libdrm_<driver>` (libdrm_intel, libdrm_nouveau, libdrm_amdgpu, libdrm_radeon) | DRM driver helpers |
| `libva` / `libvdpau` | VA-API / VDPAU hardware video acceleration (H.264/H.265/AV1) |
| `libplacebo` | GPU-accelerated video processing (mpv Vulkan/OpenGL) |
| `libvulkan` (libvulkan.so.1) | Vulkan compute/graphics (Hyprland, modern mpv) |
| `libOpenCL` | OpenCL compute (some filter pipelines) |
| `libcairo` (also GTK dep) | 2D vector rendering (picom compositing, GTK) |
| `libpixman-1` | Pixmap manipulation (software compositing fallback) |
| `libxshmfence` | Shared-memory fences for X11/GL sync |
| `libepoxy` | OpenGL function pointer loading (used by GTK 4 internally) |
| `libshaderc` | Vulkan GLSL/HLSL shader compilation to SPIR-V |
| `libglslang` | GLSL/HLSL frontend for shader compilation |
| `libspirv-tools` | SPIR-V binary processing, optimisation, validation |
| `libblend2d` | JIT-compiled 2D vector rendering engine (CPU, SIMD) |
| `libnanovg` | Small anti-aliased 2D vector drawing on OpenGL (used by GUI widgets) |
| `libskia` | Full 2D graphics library (Chrome, Flutter, Firefox) — software + GPU backends |
| `libgraphene` | Geometric algebra types for graphics (SIMD-optimised vectors, matrices) |
| `libpixman-1` | Software pixel compositing and manipulation |
| `libmtl` | Mesa thread-command submission for multi-threaded GL |
| `libvulkan-intel` / `libvulkan-radeon` / `libvulkan-broadcom` | Vulkan ICD (installable client driver) per GPU vendor |
| `libVkLayer-*` | Vulkan validation layers for debugging custom GUI rendering |

### Image Loading, Encoding & Processing

For apps that display, edit, or convert images:

| Library | Format / Role | Consumers |
|---|---|---|
| `libjpeg-turbo` | JPEG encode/decode (SIMD-accelerated) | GIMP, digiKam, lximage-qt |
| `libpng16` | PNG read/write | Every GUI app with images |
| `libwebp` | WebP encode/decode (lossy + lossless + alpha) | qutebrowser, browsers |
| `libavif` | AVIF image format (HEIF-based, royalty-free) | Modern imaging apps |
| `libheif` | HEIF/HEIC photo container (Apple, camera RAW) | digiKam, gThumb |
| `libtiff-5` / `libtiffxx` | TIFF image read/write | GIMP, digiKam, scanners |
| `libraw` | RAW camera image decoding (CR2, NEF, ARW, DNG, etc.) | digiKam, Darktable, RawTherapee |
| `libjxr` | JPEG XR (HDR photo format, Windows legacy) | Various |
| `libjxl` | JPEG XL (next-gen, lossless recompression of JPEG) | Progressive image viewers |
| `libgexiv2` | EXIF/XMP/IPTC metadata read/write | GIMP, digiKam, lximage-qt |
| `libiptcdata` | IPTC metadata (news photo standard) | Photo management apps |
| `liblcms2` | LittleCMS2 — colour profile management (ICC) | GIMP, digiKam, Oomox |
| `libwmf` | Windows Metafile vector rendering | LibreOffice, Inkscape |
| `libemf` | Enhanced Metafile rendering | LibreOffice |
| `librsvg-2` | SVG rendering (Cairo-based) | lxappearance, Oomox, GTK icon themes |
| `libsixel` | SIXEL graphics encoding (terminal images) | img2sixel, terminal emulators |
| `libquirc` | QR code decoding (camera/photo QR readers) | Various |
| `libzbar` | Barcode/QR reading (supports many symbologies) | Various scanning apps |
| `libfreeimage` | Multi-format image loading (convenience wrapper) | Various apps |
| `libexiv2` | C++ EXIF/IPTC/XMP library (C++ API, used by Qt apps) | digiKam, gThumb |

### Video Playback, Streaming & Camera / Screen Capture

For multimedia players, streaming, screen recorders, and camera apps:

| Library | Role | Consumers |
|---|---|---|
| `libavcodec` / `libavformat` / `libavutil` / `libavfilter` / `libavdevice` / `libswscale` / `libswresample` (FFmpeg) | Complete multimedia framework: codecs, muxers, filters, device capture | VLC, mpv, Kdenlive, OBS, Strawberry |
| `libmpv` | mpv media player client library (scriptable, GPU-accelerated) | Haruna, mpv-qt, baka-mplayer |
| `libvlc` / `libvlccore` | VLC media engine client library | Elisa (Phonon VLC), VLC Qt GUI |
| `libgstreamer-1.0` / `libgstbase` / `gst-plugins-*` | Pipeline-based multimedia framework (GNOME stack) | Totem, Rhythmbox, Cheese, Pitivi |
| `libgstplayer` | High-level GStreamer player API | Simplified video apps |
| `libgstwebrtc` / `libnice` | WebRTC video/audio streaming (ICE/STUN/TURN) | Video conferencing, PipeWire |
| `libvpx` | VP8/VP9 video codec (web video, YouTube) | Browsers, FFmpeg |
| `libx264` / `libx265` | H.264 / H.265 encoding | OBS, Kdenlive, FFmpeg |
| `libdav1d` | AV1 decoding (very fast, from VideoLAN) | FFmpeg, mpv, browsers |
| `libaom` | AV1 encoding/decoding (reference implementation) | FFmpeg |
| `libtheora` / `libogg` | Theora video + Ogg container (legacy, free codec) | Legacy video apps |
| `libmatroska` | Matroska/WebM container parsing | MKV-aware apps |
| `libopenmpt` | Module music (MOD/XM/IT/S3M) playback | Audio players |
| `libopenhevc` | HEVC/H.265 decoder (hardware-accelerated) | Various |
| `libva` / `libvdpau` | VA-API / VDPAU hardware video decode/encode | mpv, VLC, browsers, FFmpeg |
| `libplacebo` | GPU-accelerated video rendering + tonemapping (HDR/SDR) | mpv |
| `libmediainfo` | Media file metadata extraction (codec, bitrate, resolution) | Media info tools |
| `libchromaprint` | Acoustic fingerprinting (audio identification) | Strawberry, MusicBrainz Picard |
| `libprojectM` | MilkDrop-style visualisation (audio-reactive OpenGL) | Audio players |
| `libcamera` | Complex Camera Support Framework (libcamera — modern Linux camera stack) | Camera apps (Cheese, GUVCView) |
| `libv4l2` / `libv4lconvert` | Video4Linux 2 — webcam/device capture | OBS, Cheese, GUVCView, Kamoso |
| `libpipewire-0.3` (also audio) | PipeWire screen/camera capture (wlr-screencopy, portal) | OBS, wf-recorder, Helvum |
| `libwf-recorder` | wlroots screen recording helper | wf-recorder |
| `libgif` / `libgiflib` | GIF encode/decode (including animations) | peek, various image apps |

### Audio Backend

| Library | Used by |
|---|---|
| `libpulse` / `libpulse-simple` / `libpulse-mainloop-glib` | pavucontrol, pasystray, VLC, mpv, Firefox (via PulseAudio) |
| `libpipewire-0.3` / `libspa-0.2` | PipeWire-aware apps, WirePlumber, Helvum, QPWGraph |
| `libalsa` / `libasound2` | ALSA-native apps, volume plugin, some drivers |
| `libsndfile` | Audio file I/O (WAV, FLAC, Ogg) |
| `libavcodec` / `libavformat` / `libavutil` / `libswresample` (ffmpeg) | Media playback in VLC, mpv, Kdenlive, Strawberry |
| `libsoxr` | Sample-rate conversion |
| `libsamplerate` | Sample-rate conversion (legacy) |
| `libmysofa` | HRTF (head-related transfer function) for spatial audio |

### System Services & IPC

| Library | Used by |
|---|---|
| `libdbus-1` | All D-Bus-aware apps (lxqt-*, NetworkManager, PipeWire) |
| `libsystemd` / `libelogind` | Login/seat management, power management, inhibitor locks |
| `libpolkit-gobject-1` | PolicyKit C API (polkit XFCE, lxpolkit) |
| `libpolkit-agent-1` | Polkit agent helpers |
| `libarchive` | Archive reading (tar, zip, 7z, rar) — lxqt-archiver, Ark |
| `libcurl` | HTTP/FTP transfers — CLI tools, some Qt apps via QtNetwork |
| `libxml2` | XML parsing — nearly universal |
| `libjson-c` / `libjansson` / `libyaml` | JSON/YAML parsing — various CLI tools |
| `libnl-3` / `libnl-genl-3` | Netlink sockets (NetworkManager, iwd, wpa_supplicant) |
| `libpcap` | Packet capture (network monitors, Rymd) |
| `libseccomp` | System call filtering (sandboxing) |

### Theming Engines

| Library | Used by |
|---|---|
| `libkvantum` / `libkvantum-qt6` | SVG-based Qt theme engine — all Qt apps when Kvantum is the active style |
| `libgtk-3` / `libgtk-4` (themes) | GTK theme renderer — `gtk3` package includes theme engines |
| `libsass` / `libscss` | SASS/SCSS CSS preprocessor (used by Oomox for theme generation) |

### Rich Text, Fonts, i18n & Input Methods

For apps with complex text editing, multi-language support, charts, or formatted output:

| Library | Role | Consumers |
|---|---|---|
| `libpango-1.0` / `libpangocairo-1.0` / `libpangoft2` | Text layout, bidirectional, Cairo/FreeType backends | Every GTK app, some Qt (via gtk platform theme) |
| `libharfbuzz` | OpenType text shaping, ICU integration | Every GTK/Qt app rendering complex scripts |
| `libraqm` | Complex text layout engine (Arabic, Indic, etc.) | Image editors (GIMP text tool) |
| `libfribidi` | Unicode bidirectional algorithm (bidi reordering) | Text rendering stack |
| `libfreetype` / `libfontconfig` | Font file parsing + system font discovery | Every GUI app |
| `libunistring` | Unicode string operations (case conversion, collation, etc.) | Various text-processing apps |
| `libicuuc` / `libicui18n` / `libicudata` | ICU — full Unicode/CLDR (collation, break iteration, date/number formatting, timezone) | Qt, LibreOffice, Chromium |
| `libmenuwidget` / `libpango-graph` | Pango-based graph/cairo widget | Custom dashboards |
| `libgspell-1` | GTK spellcheck (enchant backend) | Text editors (gedit, mousepad) |
| `libgtksourceview-4` / `libgtksourceview-5` | Rich source code editor widget (line numbers, syntax highlighting, code folding) | Geany, gedit, Mousepad, Builder |
| `libKF5SyntaxHighlighting` / `libKSyntaxHighlighting` | KDE syntax highlighting framework (XML-defined, 200+ languages) | FeatherPad, Kate, KWrite, KDevelop |
| `libpeas-1.0` / `libpeas-gtk` | GObject plugin system for extensible apps | Builder, gedit plugins |
| `libgedit-*` (libgedit-gtksourceview, libgedit-amtk, libgedit-tepl) | Modern GNOME text editor components (split from gtksourceview) | GNOME Text Editor |
| `libtepl-6` | GNOME text editor base library (file loading/saving, search, cursor management) | GNOME Text Editor |
| `libgtkspell` / `libgtkspell3-3` | Legacy GTK spellcheck (obsolete, replaced by gspell) | Older GTK apps |
| `libenchant-2` | Spell-check engine abstraction (aspell, hunspell, nuspell backends) | gspell, Thunderbird, LibreOffice |
| `libebook-1.2` / `libedataserver-1.2` | Evolution Data Server — address book, calendar, contacts backend | Evolution, GNOME calendar |
| `libime` | Fcitx5 input method engine core (Chinese, Japanese, Korean) | Fcitx5 |
| `libfcitx5-qt` / `libfcitx5-gtk` | Fcitx5 input method platform plugins for Qt/GTK | Fcitx5, all Qt/GTK apps |
| `libibus-1.0` | IBus input method framework | IBus, all GTK apps via IM module |
| `libQt5VirtualKeyboard` / `libQt6VirtualKeyboard` | Qt Virtual Keyboard (on-screen, predictive) | Embedded/touch Qt apps |
| `libxkbcommon` (also display) | XKB keyboard layout compilation + state machine | All Wayland compositors, apps |
| `libxcb-xkb` | XKB over X11 | X11 apps |
| `libxcb-keysyms` | X11 keysym lookup | X11 WMs, panels, bars |
| `libm17n` / `libm17n-flt` | Multi-lingual text engine (CJK, complex scripts) | Legacy internationalised apps |
| `libcld2` / `libcld3` | Compact Language Detector (2/3) — language identification | Full-text search, browsers |
| `libonig` / `libonigmo` | Oniguruma regex engine (full Unicode regex, used by TextMate grammars) | Sublime Text, Zed, various editors |

### Cross-Platform & Additional UI Toolkits

Alternative widget or windowing toolkits that run on LXQt (X11 and/or Wayland):

| Library | Type | Best for | Deps size |
|---|---|---|---|
| `libSDL2` / `libSDL2-2.0` | Cross-platform multimedia + windowing (OpenGL/Vulkan) | Games, emulators, media players | ~5 MB |
| `libSDL2_image` / `libSDL2_ttf` / `libSDL2_mixer` / `libSDL2_net` | SDL extensions for image loading, fonts, audio, networking | Game/SDL apps | ~2 MB each |
| `libGLFW` (libglfw) | Lightweight OpenGL/Vulkan windowing and input | OpenGL demos, tools, prototyping (no UI widgets) | ~2 MB |
| `libFLTK` / `libfltk` | Fast Light Toolkit — small, old-school X11/C++ widgets | Minimal GUI tools, embedded, small footprint | ~2 MB |
| `libfox-1.6` | FOX Toolkit — cross-platform C++ widgets | Legacy scientific/engineering GUIs | ~4 MB |
| `libIup` / `libiup` | Portable UI toolkit (C, callbacks, Tecgraf/PUC-Rio) | Scientific GUI wrappers (CD library companion) | ~2 MB |
| `libnuklear` / `libnuklear-gl` | Single-header minimal immediate-mode GUI (no deps) | Overlays, debug UIs, game tools | < 1 MB |
| `libraylib` | Simple OpenGL-based multimedia + GUI (C, beginner-friendly) | Games, prototyping, education | ~3 MB |
| `libgiwx` / `widget` | GTK 3/4 widgets for Rust (via gtk-rs bindings) | Rust GTK apps (the library is indirect) | (Rust deps) |
| `libQt5WebEngine` / `libQt6WebEngine` | Full Chromium rendering inside Qt Widgets | Rich HTML/JS UIs inside Qt apps | ~50 MB |
| `libwebkit2gtk-4.1` / `libwebkitgtk-6.0` | WebKit rendering engine for GTK | Rich HTML/JS UIs inside GTK apps | ~40 MB |
| `libwx_baseu-3.2` / `libwx_gtk3u_core-3.2` | wxWidgets — native-look C++ widgets (wraps GTK or Qt) | Cross-platform desktop apps with native look | ~10 MB |
| `liblgi` / `libim` | IUP + IM + CD toolkit stack (Tecgraf) | Scientific data visualisation, CAD-like tools | ~5 MB |

### Desktop Integration & Portal Widgets

For apps that need system-level features (file dialogs, colour pickers, desktop portals, system trays):

| Library | Role | Consumers |
|---|---|---|
| `libadwaita-1` | GNOME adaptive widgets (GTK 4, header bars, toast overlays, breakpoints) | Modern GNOME apps, GTK 4 apps |
| `libhandy-1` | GNOME adaptive widgets (GTK 3 predecessor to libadwaita) | Legacy GNOME apps (GTK 3) |
| `libdazzle-1.0` | GNOME utility widgets (spinners, docks, panels, search) | Builder, GNOME utility apps |
| `libpanel-1` / `libpanel-6` | GTK 4 panel/dock widget (split views, terminal panels) | Builder, IDEs, developer tools |
| `libwnck-3` | Window Navigation Construction Kit (taskbars, pagers, window lists) | Plank, Polydock, DockbarX, nwg-panel |
| `libbamf3` | BAMF Application Matching Framework (window-to-app matching, grouping) | Plank, DockbarX, Unity launcher |
| `libshumate-1.0` | GTK 4 map widget (OpenStreetMap vector tiles) | GNOME Maps, navigation apps |
| `libchamplain-0.12` | GTK 3 map widget (Clutter-based, OpenStreetMap) | Legacy GNOME Maps |
| `libgtk-4-layer-shell` | GTK 4 integration with Wayland layer-shell protocol | GTK bars, panels, overlays on Wayland |
| `libdbusmenu-glib` / `libdbusmenu-gtk3` | D-Bus status notifier (application indicators, Unity-style) | Legacy app indicators, tray apps |
| `libindicator` / `libindicator3` | Legacy Ubuntu indicator protocol | App indicators (discontinued) |
| `libappindicator` / `libappindicator3` | Application indicator library for system trays | Legacy tray icons, Discord, Slack |
| `libnotify` | Desktop notification bubbles (freedesktop notification spec) | notify-send, various apps |
| `libportal` / `libportal-gtk4` / `libportal-qt6` | Flatpak portal access (file chooser, screenshot, wallpaper, remote desktop, printing, OpenURI) via xdg-desktop-portal | Flatpak apps, xdg-desktop-portal backends |
| `libflatpak` | Flatpak app management (install/remove/update sandboxed apps) | Flatpak CLI, GNOME Software, KDE Discover |
| `libostree` | OSTree atomic update system | System updaters, Flatpak base |
| `libpackagekit-glib2` | PackageKit D-Bus client (install/update/remove packages via PackageKit daemon) | GNOME Software, KDE Discover, pkcon |
| `libzypp` / `libzypp-devel` | ZYpp package management backend (openSUSE) | YaST, Zypper |
| `libalpm` | Arch Linux Package Manager (pacman) library | Pacman, pamac, octopi |
| `libxapp` | Linux Mint XApp library (status icon, preview, sidecar) | Cinnamon/Xfce apps |
| `libgcr-4` / `libgck-2` | GNOME Keyring/Crypto libraries — secret storage, certificate UI | Seahorse, GCR-viewer |
| `libsecret-1` | Freedesktop Secret Service API (password management, keyring) | Gnome Keyring, KeepassXC, Seahorse |
| `libgpgme` | GnuPG Made Easy — crypto operations (encrypt/sign/verify) | GPA, KGpg, Seahorse, git |
| `libpwquality` | Password quality checking and generation | User management, polkit agents |
| `libaccounts-glib` | Online accounts management (sign-on, OAuth) | GNOME Online Accounts |

### Compression, Archiving & Data Serialization

Used by file managers, archivers, package tools, and data-exchange apps:

| Library | Format / Role | Consumers |
|---|---|---|
| `libarchive` (already listed) | Multi-format archive (tar, cpio, zip, 7z, iso, xar, cab, mtree) | lxqt-archiver, Ark, file-roller |
| `libzip` | ZIP archive read/write (simple C API) | Various archivers |
| `liblz4` | Extremely fast compression (streamable) | Systemd, kernel, databases |
| `libzstd` | Zstandard compression (high ratio, fast, dictionary) | FFmpeg, systemd, kernel, compression utils |
| `libbrotli` / `libbrotlidec` / `libbrotlienc` | Brotli compression (HTTP, WOFF2 fonts) | Browsers, web servers, web-font rendering |
| `liblzma` / `liblzmadec` | XZ/LZMA compression (high ratio, slow) | Package managers, archives |
| `libbz2` | bzip2 compression (legacy, good ratio) | Legacy archives, package tools |
| `libz` / `libzlib` | zlib/deflate/gzip compression | Nearly universal (png, http, git, ssh, etc.) |
| `libprotobuf` / `libprotobuf-lite` | Protocol Buffers (Google) — typed, binary serialization | Various networked apps, protobuf services |
| `libprotobuf-c` | Protocol Buffers for C | C-based protobuf consumers |
| `libmsgpackc` / `libmsgpack` | MessagePack — binary JSON (compressed, typed) | Various API clients, messaging |
| `libcbor` | CBOR (RFC 7049) — compact binary representation of JSON-like data | IoT, FIDO/WebAuthn, COSE |
| `libtoml` / `libtoml11` | TOML config file parsing (used by Cargo, many modern tools) | Rust tools, modern apps |
| `libconfuse` | Autoconf-style config file parser (ini-like) | Various C/C++ configs |
| `libinih` | Minimal INI file parser (single header, C) | Lightweight config file reading |
| `libyaml` / `libyaml-cpp` | YAML parsing (Python/Ruby-style config) | Various modern apps |
| `libucl` | Universal Config Library (nginx-like syntax, JSON superset) | Various |  
| `libexpat` / `libexpatw` | XML stream parser (SAX, minimal, used by dbus, SVG) | D-Bus, X11 apps, librsvg |

### Hardware & Peripheral Sensor APIs

For apps that interact with system hardware directly:

| Library | Role | Consumers |
|---|---|---|
| `libpci` | PCI bus enumeration and identification | lspci, hardinfo, pcimem |
| `libusb-1.0` | USB device access (libusb) | lsusb, qFlipper, various USB tools |
| `libhidapi` | HID interface for input devices (gamepads, drawing tablets, UPS) | Steam, game controllers, tablet tools |
| `libgpiod` / `libgpiodcxx` | GPIO control through gpiochip character device | Embedded/IoT apps on Linux |
| `libi2c` | I2C/SMBus device access | Sensor reading, hardware monitors |
| `libwacom` / `libwacom2` | Wacom tablet database + configuration | GNOME Settings Wacom, KDE tablet config |
| `libgudev-1.0` | udev device enumeration and monitoring | Blueman, system-config-printer, device managers |
| `libevdev` | Kernel evdev device wrapper (input event handling for libinput) | libinput, Wayland input backends |
| `libsensors` (lm-sensors) | Hardware sensor reading (CPU temp, fan speed, voltage) | lxqt-panel sensors plugin, psensor |
| `libupower-glib` | UPower power device info (battery, AC adapter status) | lxqt-powermanagement, Xfce power manager |
| `libayatana-appindicator` | Ayatana Indicators (community fork, maintained) | System tray, indicator apps |
| `libqmi` / `libmbim` | Qualcomm MSM Interface / Mobile Broadband Interface Model — WWAN/modem | NetworkManager modems, ModemManager |
| `libpcsclite` | PC/SC Smart Card framework | Smart card readers, crypto tokens |
| `libnfc` | Near Field Communication library | NFC tools, contactless readers |
| `libfreefare` | MIFARE card operations | NFC tag read/write |
| `libbluez` / `libbluetooth` | BlueZ Bluetooth protocol stack | Blueman, BlueDevil, bluetoothctl |
| `libsbc` / `libldac` / `libfdk-aac` | SBC / LDAC / FDK-AAC Bluetooth audio codecs | PulseAudio/PipeWire Bluetooth modules |
| `libwireplumber-0.4` | WirePlumber session manager client library | PipeWire audio routing, Lua scripting |

### Database & Storage Libraries

For apps that store structured data locally:

| Library | Database / Role | Consumers |
|---|---|---|
| `libsqlite3` | SQLite — embedded SQL database (single-file, zero-config) | Qt SQL, Firefox, Chromium, virtually all apps |
| `libmdbx` | libmdbx — fast transactional key-value store (ACID, MMAP) | Various performance-critical apps |
| `liblmdb` / `liblmdb++` | Lightning Memory-Mapped Database (ultra-fast, read-optimised) | OpenLDAP, various |
| `libpq` | PostgreSQL C client library | psql, database GUI tools (PgAdmin) |
| `libmysqlclient` / `libmariadb` | MySQL / MariaDB C client library | mysql CLI, various admin UIs |
| `libsoci_*` / `libsoci-core` | SOCI — C++ database abstraction (supports SQLite, Pg, MySQL) | C++ database apps |
| `libunqlite` | UnQLite — embedded NoSQL (key-value + JSON document store) | Embedded apps, config storage |
| `libgd` / `libgd2` | GD graphics library (dynamic image creation: GIF, JPEG, PNG, WBMP, WEBP) | PHP, web apps, image generation |

### Suggested Early App Install Set

If setting up LXQt from scratch and wanting the best low-library coverage:

**Essential theming & integration:**
```
# Arch
pacman -S qt5ct qt6ct kvantum kvantum-qt5 kvantum-qt6 lxappearance
# Debian/Ubuntu
apt install qt5ct qt6ct kvantum lxappearance
```

**Wayland compatibility layer (XWayland, portals, clipboard):**
```
# Arch
pacman -S xorg-xwayland xdg-desktop-portal xdg-desktop-portal-wlr xdg-desktop-portal-gtk
# Debian/Ubuntu
apt install xwayland xdg-desktop-portal xdg-desktop-portal-wlr xdg-desktop-portal-gtk
```

**Recommended base app suite by toolkit:**
- **Qt apps to install first:** `qterminal`, `pcmanfm-qt`, `featherpad`, `lximage-qt`, `screengrab`, `lxqt-archiver`
- **GTK apps (for tool coverage):** `pavucontrol`, `blueman`, `system-config-printer`, `lxappearance`
- **Clipboard:** `copyq` (Qt) + `wl-clipboard` (Wayland backend)
- **Color generation:** `pywal` or `wallust` + `oomox` (both GTK and Qt theme generation)
- **Key library metapackages (install once):** `qt5-base qt6-base qt5-wayland qt6-wayland gtk3 gtk4 glib2 pango cairo` — these cover 90% of the shared-library needs for any app in this list.

## Building Custom GUI Apps

Knowing the lower-level dependency chain lets you pick the right toolkit for a custom app without pulling in unnecessary weight.

### Toolkit Selection Guide

| Level | Library | Deps pulled | Lines for a window | Best for |
|---|---|---|---|---|
| **Qt (Widgets)** | `libQt5Widgets` / `libQt6Widgets` | ~40-60 MB of libs | ~10 lines | Feature-rich LOB apps, complex widgets |
| **Qt (QML/Quick)** | `libQt5Qml` / `libQt6Quick` | ~50-80 MB | ~8 lines | Animated/smooth UIs, mobile-style |
| **GTK 4** | `libgtk-4` + `libglib-2.0` + `libpango` + `libcairo` | ~15-25 MB | ~12 lines | Lightweight desktop tools, GNOME-style |
| **GTK 3** | `libgtk-3` + same chain | ~10-20 MB | ~12 lines | Legacy compatibility, simpler API |
| **raw XCB** | `libxcb` + `libx11` | ~2 MB | ~40 lines | Minimal X11 utilities, custom WMs |
| **raw Wayland** | `libwayland-client` + `libxkbcommon` | ~3 MB | ~60 lines | Custom compositors, minimal clients |
| **wlroots helpers** | `libwlroots` + `libwayland-server` | ~8 MB | ~30 lines | Compositor components, layer-shell apps |
| **cairo + xcb** | `libcairo` + `libxcb` | ~5 MB | ~35 lines | Custom rendering (graphs, viz, bars) |
| **SDL2** | `libSDL2` | ~5 MB | ~15 lines | Cross-platform games, media players |

### Minimal Build Examples

**Qt6 Widgets (C++)** — a window in ~10 lines:

```cpp
#include <QApplication>
#include <QPushButton>
int main(int argc, char *argv[]) {
    QApplication app(argc, argv);
    QPushButton btn("hello lxqt");
    btn.resize(200, 80);
    btn.show();
    return app.exec();
}
```
```bash
# compile
g++ -std=c++17 $(pkg-config --cflags --libs Qt6Widgets) main.cpp -o qt-hello
```

**GTK 4 (C)** — a window in ~12 lines:

```c
#include <gtk/gtk.h>
int main(int argc, char *argv[]) {
    gtk_init();
    GtkWidget *win = gtk_window_new();
    gtk_window_set_title(GTK_WINDOW(win), "hello lxqt");
    gtk_window_set_default_size(GTK_WINDOW(win), 200, 80);
    g_signal_connect(win, "destroy", G_CALLBACK(gtk_window_destroy), NULL);
    gtk_widget_show(win);
    gtk_main();
    return 0;
}
```
```bash
gcc $(pkg-config --cflags --libs gtk4) main.c -o gtk-hello
```

**Raw XCB (C)** — zero toolkit, pure X11 protocol:

```c
#include <xcb/xcb.h>
int main() {
    xcb_connection_t *c = xcb_connect(NULL, NULL);
    xcb_screen_t *s = xcb_setup_roots_iterator(xcb_get_setup(c)).data;
    xcb_window_t w = xcb_generate_id(c);
    xcb_create_window(c, s->root_depth, w, s->root, 0, 0, 200, 80, 0,
                      XCB_WINDOW_CLASS_INPUT_OUTPUT, s->root_visual, 0, NULL);
    xcb_map_window(c, w);
    xcb_flush(c);
    for (xcb_generic_event_t *e; (e = xcb_wait_for_event(c)); free(e)) {}
    return 0;
}
```
```bash
gcc $(pkg-config --cflags --libs xcb) main.c -o xcb-hello
```

**Raw Wayland client (C)** — minimal wl_shm window:

```c
#include <wayland-client.h>
int main() {
    struct wl_display *d = wl_display_connect(NULL);
    struct wl_registry *r = wl_display_get_registry(d);
    wl_display_roundtrip(d);
    // binds wl_compositor, wl_shm, creates surface + shell_surface
    wl_display_disconnect(d);
    return 0;
}
```
```bash
gcc $(pkg-config --cflags --libs wayland-client) main.c -o wayland-hello
```

**Cairo on XCB (C)** — custom-drawn panel/graph:

```c
#include <cairo/cairo-xcb.h>
#include <xcb/xcb.h>
int main() {
    // creates xcb window, then:
    cairo_surface_t *s = cairo_xcb_surface_create(conn, win, visual, 200, 80);
    cairo_t *cr = cairo_create(s);
    cairo_set_source_rgb(cr, 0.2, 0.4, 0.8);
    cairo_rectangle(cr, 10, 10, 180, 60);
    cairo_fill(cr);
    cairo_destroy(cr);
    cairo_surface_destroy(s);
}
```
```bash
gcc $(pkg-config --cflags --libs cairo xcb) main.c -o cairo-xcb-hello
```

### How to Find Library Flags on Any Distro

Always use `pkg-config` — never hardcode `-I` or `-L` paths:

```bash
# list all known .pc files
pkg-config --list-all | grep -E '^(Qt5|Qt6|gtk|glib|wayland|xcb|cairo)'

# get compiler + linker flags for any library
pkg-config --cflags --libs Qt6Widgets
pkg-config --cflags --libs gtk4
pkg-config --cflags --libs xcb
pkg-config --cflags --libs wayland-client
pkg-config --cflags --libs cairo xcb
```

For CMake-based projects:

```cmake
# CMakeLists.txt
find_package(Qt6 REQUIRED COMPONENTS Widgets)
# or
find_package(PkgConfig)
pkg_check_modules(GTK4 REQUIRED gtk4)
```

### Why This Knowledge Helps

1. **Minimal deps** — Need a simple volume OSD? Use raw Wayland layer-shell (one dep of ~3 MB) instead of pulling in the entire Qt Widgets stack (~60 MB).
2. **Custom panel widgets** — `lxqt-panel`'s CPU/memory graphs use QSS for styling; you could write a dedicated Cairo-based overlay that renders custom graphs with < 2 MB of deps.
3. **Compositor plugins** — Hyprland and Wayfire support plugin systems. A custom blur/effect plugin links only `libwayland-server` + `libwlroots`, not a full toolkit.
4. **Tray/indicator** — A minimal system indicator (battery, network) can be a 50-line XCB window with Cairo drawing — no toolkit required.
5. **Screen locker** — A custom locker for wlroots compositors needs only `libwayland-client` + `ext-session-lock` protocol, keeping the attack surface small.
6. **Resource-constrained systems** — Embed a Qt app on a Raspberry Pi? Drop `Qt5WebEngine` (~50 MB) and use `libsoup` + `webkit2gtk` (~10 MB) or raw `libcurl` + Cairo instead.

## Distributions

Linux distributions that offer LXQt spins or editions out of the box:

- **[Lubuntu](https://lubuntu.me/)** - The official Ubuntu LXQt flavor. Great for beginners and low-spec hardware.
- **[Fedora LXQt Spin](https://spins.fedoraproject.org/lxqt/)** - A clean, up-to-date LXQt experience from Fedora.
- **[Arch Linux](https://archlinux.org/)** - DIY setup; offers the most vanilla LXQt experience via `pacman -S lxqt`.
- **[Manjaro LXQt](https://manjaro.org/)** - A community edition featuring LXQt with Manjaro's hardware detection and tools.
- **[SparkyLinux LXQt](https://sparkylinux.org/)** - A lightweight LXQt edition based on Debian (stable or rolling).
- **[Debian LXQt](https://wiki.debian.org/LXQt)** - Install LXQt on Debian via `tasksel install lxqt-desktop` or the `lxqt` metapackage.
- **[openSUSE LXQt](https://en.opensuse.org/Portal:LXQt)** - openSUSE offers LXQt in its repositories (Tumbleweed and Leap).
- **[Void Linux LXQt](https://voidlinux.org/)** - Void's package manager (`xbps`) includes a complete LXQt package set.
- **[Artix Linux LXQt](https://artixlinux.org/)** - Arch-based without systemd; offers an LXQt edition (OpenRC or runit).
- **[EndeavourOS](https://endeavouros.com/)** - Arch-based; ships with Xfce by default but LXQt is available via the welcome app.
- **[Mageia LXQt](https://www.mageia.org/)** - Offers an LXQt install option in its installer.
- **[Gentoo LXQt](https://wiki.gentoo.org/wiki/LXQt)** - Fully customizable; LXQt available in the main portage tree.
- **[PCLinuxOS LXQt](https://www.pclinuxos.com/)** - Offers an LXQt community edition.
- **[GeckoLinux LXQt](https://geckolinux.github.io/)** - openSUSE-based with a pre-configured LXQt edition.
- **[ROSA Linux LXQt](https://www.rosalinux.ru/)** - A Russian distro offering LXQt as an official desktop option alongside KDE, GNOME, and Xfce.
- **[Alpine Linux](https://www.alpinelinux.org/)** - LXQt is available as a desktop option via the `setup-desktop` script; ideal for minimal and containerized setups.
- **[Calculate Linux LXQt](https://www.calculate-linux.org/)** - A Gentoo-based distro with a dedicated LXQt desktop edition, rolling release.
- **[Slackware](https://www.slackware.com/)** - LXQt packages are available via community SlackBuilds and third-party repositories.
- **[Devuan](https://www.devuan.org/)** - Offers LXQt as a standard desktop choice during installation, without systemd.
- **[ALT Linux](https://en.altlinux.org/)** - Provides LXQt as an available desktop option.
- **[Emmabuntüs](https://emmabuntus.org/)** - A beginner-friendly distribution that includes LXQt as one of its default desktop environment options.
- **[Kali Linux](https://www.kali.org/)** - The popular penetration testing distro offers LXQt as a selectable desktop environment in its installer.
- **[NixOS](https://nixos.org/)** - Provides LXQt as a standard, declaratively configurable desktop environment option.
- **[Garuda Linux](https://garudalinux.org/)** - Has offered an LXQt-Kwin edition focusing on performance and a distinct aesthetic.

## Resources & Tutorials

### Official

- [Official LXQt Website](https://lxqt-project.org/)
- [LXQt GitHub Organization](https://github.com/lxqt)
- [LXQt Wiki](https://github.com/lxqt/lxqt/wiki)
- [LXQt Wayland Wiki](https://github.com/lxqt/lxqt/wiki/Wayland) - Official guide for LXQt on Wayland compositors.
- [LXQt Blog (Planet LXQt)](https://planet.lxqt-project.org/)
- [LXQt Release Notes](https://github.com/lxqt/lxqt/releases)

### Guides & Documentation

- [Arch Linux Wiki - LXQt](https://wiki.archlinux.org/title/LXQt) - Detailed documentation for configuration, troubleshooting, and Wayland setup.
- [Arch Linux Wiki - LXQt (X11)](https://wiki.archlinux.org/title/LXQt#Configuration) - X11-specific configuration guidance.
- [Arch Linux Wiki - Wayland](https://wiki.archlinux.org/title/Wayland) - General Wayland documentation.
- [Arch Linux Wiki - Openbox](https://wiki.archlinux.org/title/Openbox) - Openbox configuration guide.
- [Lubuntu Manual](https://manual.lubuntu.me/) - Official Lubuntu documentation with LXQt details.
- [Lubuntu Release Notes](https://lubuntu.me/blog/) - Release notes and changelogs for the latest LXQt versions.
- [Gentoo Wiki - LXQt](https://wiki.gentoo.org/wiki/LXQt) - Gentoo-specific LXQt install and config guide.
- [Debian Wiki - LXQt](https://wiki.debian.org/LXQt) - Debian-specific LXQt installation.
- [Fedora LXQt Spin](https://fedoraproject.org/spins/lxqt/) - Fedora LXQt Spin documentation.

### Compositor-Specific Guides

- [Labwc Wiki](https://github.com/labwc/labwc/wiki) - Setup and config examples for Labwc + LXQt.
- [Labwc + LXQt Setup](https://github.com/labwc/labwc/wiki/LXQt) - Official Labwc + LXQt integration guide.
- [Hyprland Wiki](https://wiki.hyprland.org/) - Hyprland configuration guide.
- [Hyprland + LXQt](https://wiki.hyprland.org/Useful-Utilities/Desktop-Environment/) - Hyprland's LXQt guide.
- [Sway Wiki](https://github.com/swaywm/sway/wiki) - Sway configuration and usage.
- [Sway + LXQt](https://github.com/swaywm/sway/wiki/Desktop-environments) - Sway + LXQt integration notes.
- [Wayfire Wiki](https://github.com/WayfireWM/wayfire/wiki) - Wayfire configuration.
- [KWin Wiki](https://userbase.kde.org/KWin) - KWin configuration and effects.

### Developer Resources

- [Qt Documentation](https://doc.qt.io/) - Official Qt documentation for developers.
- [LXQt Developer Guide](https://github.com/lxqt/lxqt/wiki/Developers) - Building and contributing to LXQt.
- [LXQt Coding Style](https://github.com/lxqt/lxqt/wiki/CodingStyle) - LXQt coding conventions.
- [Freedesktop.org Specifications](https://www.freedesktop.org/wiki/Specifications/) - Desktop standards (DBus, XDG, etc.) used by LXQt.
- [Wayland Protocols](https://wayland.freedesktop.org/) - Wayland protocol documentation.

### Video Tutorials & Talks

- [LXQt on Wayland - Overview](https://www.youtube.com/results?search_query=lxqt+wayland) - Search for the latest LXQt Wayland demos on YouTube.
- [Lubuntu Reviews & Walkthroughs](https://www.youtube.com/results?search_query=lubuntu+lxqt) - Video walkthroughs of Lubuntu with LXQt.
- [Openbox Ricing Tutorials](https://www.youtube.com/results?search_query=openbox+ricing) - Openbox customization guides (directly applicable to LXQt).
- [Labwc + LXQt Setup](https://www.youtube.com/results?search_query=labwc+lxqt) - Labwc Wayland compositor with LXQt walkthroughs.
- [Qt Theming with Kvantum](https://www.youtube.com/results?search_query=kvantum+theme+setup) - Video guides for Kvantum theming.

## Community

- [Reddit: r/LXQt](https://www.reddit.com/r/LXQt/) - Subreddit for LXQt discussion and support.
- [Reddit: r/unixporn](https://www.reddit.com/r/unixporn/) - Many LXQt rice posts for inspiration.
- [LXQt Mailing List](https://lists.lxqt-project.org/) - Official LXQt development mailing list.
- [LXQt IRC](https://web.libera.chat/#lxqt) - `#lxqt` on Libera.Chat.
- [LXQt Matrix Space](https://matrix.to/#/#lxqt:matrix.org) - LXQt Matrix chat room.
- [LXQt Discord](https://discord.gg/qFh8yJE) - Unofficial LXQt Discord server.
- [LXQt on Reddit: r/linux](https://www.reddit.com/r/linux/) - General Linux discussions where LXQt is frequently mentioned.
- [Planet LXQt](https://planet.lxqt-project.org/) - LXQt blog aggregator (developer blogs).
- [LXQt on Twitter](https://twitter.com/LXQtProject) - Official LXQt Twitter account.

## Troubleshooting & FAQ

### LXQt session won't start (black screen)

**Cause**: The `window_manager` in `~/.config/lxqt/session.conf` points to a missing or broken WM/compositor.

**Fix**: Switch to a different TTY (Ctrl+Alt+F2), log in, and edit `session.conf`:
```bash
sed -i 's/window_manager=.*/window_manager=openbox/' ~/.config/lxqt/session.conf
```
Then try `startx` or restart your display manager.

### Panel doesn't show window buttons on Wayland

**Cause**: The panel needs the compositor's `wlr-foreign-toplevel` protocol to list windows. This is supported by Labwc, Sway, Hyprland, and Wayfire, but not KWin (which uses its own KWindowSystem backend).

**Fix**: 
- If using KWin: Launch the panel with `LXQT_PANEL_WAYLAND_BACKEND=KWindowSystem`.
- If using a wlroots compositor: Ensure `lxqt-panel` is launched without any override (it auto-detects).
- Check with: `lxqt-panel --version` and ensure the Wayland backend is compiled in.

### Qt apps look wrong / theme not applying

**Cause**: Missing `QT_QPA_PLATFORMTHEME` or wrong style set.

**Fix**:
1. Ensure `QT_QPA_PLATFORMTHEME=lxqt` (native) or `=qt5ct`/`=qt6ct` is set in `session.conf` or shell profile.
2. If using Kvantum, set `QT_STYLE_OVERRIDE=kvantum`.
3. Run `qt5ct`/`qt6ct` GUI and confirm the selected theme.
4. Verify the theme engine is installed: `pacman -Qs kvantum` (Arch) or `apt list --installed | grep kvantum` (Debian).

### No system tray icons

**Cause**: Status notifier protocol not supported, or a missing tray plugin.

**Fix**:
- In LXQt panel, ensure the "Status Notifier" plugin is added (not the legacy "System Tray").
- On X11, some apps still use the legacy XEmbed system tray. Add both "Status Notifier" and "System Tray" plugins.
- Ensure a polkit agent is running (see [Polkit Authentication Agents](#polkit-authentication-agents)).

### Copy-paste broken between X11 and Wayland apps

**Cause**: X11 and Wayland use different clipboard systems. Apps forced via `GDK_BACKEND=x11` or `QT_QPA_PLATFORM=xcb` on a Wayland session use X11 clipboard, while native Wayland apps use Wayland clipboard.

**Fix**:
- Keep all apps on the same backend: prefer native Wayland (`QT_QPA_PLATFORM=wayland`, `GDK_BACKEND=wayland`).
- For cross-backend clipboard sync, use `copyq` with both X11 and Wayland support enabled, or manually use `wl-copy`/`wl-paste` and `xclip`/`xsel` to bridge.

### Screen locker won't engage on Wayland

**Cause**: The compositor must support the `ext-session-lock` protocol. KWin supports it natively. Labwc supports it since v0.7. Sway and Hyprland support it via `swaylock`/`hyprlock`.

**Fix**:
- Use the compositor's recommended locker: `swaylock` for Sway, `hyprlock` for Hyprland, `waylock` for wlroots.
- LXQt's built-in lock (`lxqt-sudo --lock`) may not work on Wayland. Bind a compositor-specific lock command instead.

### Firefox/Chromium don't use my GTK theme

**Cause**: Browsers respect the GTK theme but may use the wrong GTK backend or have no theme set.

**Fix**:
- Set `GTK_THEME=Adwaita-dark` or your preferred theme in `session.conf`.
- Ensure GTK themes are installed: `pacman -Qs gtk3` and your theme package.
- For Chromium/Electron apps on Wayland: launch with `--enable-features=UseOzonePlatform --ozone-platform=wayland`.

### LXQt on Wayland: screen sharing doesn't work

**Cause**: Missing `xdg-desktop-portal` backend for the compositor.

**Fix**:
- Install `xdg-desktop-portal-wlr` for wlroots compositors (Labwc, Sway, Hyprland).
- Install `xdg-desktop-portal-kde` for KWin.
- Ensure the portal service is running: `systemctl --user status xdg-desktop-portal`
- PipeWire must be running: `systemctl --user status pipewire`

### GTK apps look huge or tiny on HiDPI

**Cause**: GTK does not auto-scale the same way Qt does.

**Fix**:
- Set `GDK_DPI_SCALE=1` (no scaling) or `GDK_DPI_SCALE=2` (2x scaling) in `session.conf`.
- For per-app overrides: `GDK_DPI_SCALE=1.5 gtk-app-name`.
- Use `gsettings set org.gnome.desktop.interface text-scaling-factor 1.5` for GNOME/GTK3 apps.

### How do I reset LXQt to defaults?

```bash
mv ~/.config/lxqt ~/.config/lxqt.bak
mv ~/.config/openbox ~/.config/openbox.bak  # if using Openbox
```
Log out and back in. LXQt will regenerate default config files. Copy back specific files from the backup to restore settings.

### LXQt 1.x vs LXQt 2.0 — what changed?

| Feature | LXQt 1.x (Qt5) | LXQt 2.0 (Qt6) |
|---------|----------------|----------------|
| Qt version | Qt 5.15 | Qt 6.5+ |
| Wayland support | Experimental | Native (stable) |
| Panel backends | X11 only | X11 + Wayland |
| Config location | `~/.config/lxqt/` | `~/.config/lxqt/` (same) |
| qt5ct/qt6ct | Use `qt5ct` | Use `qt6ct` |
| Compositor | X11 WM required | Works with Wayland compositors |
| Config compatibility | — | **NOT** backwards-compatible with 1.x |

**Migrating from 1.x to 2.0**: Fresh install the LXQt 2.0 packages and reconfigure. Do NOT copy 1.x config files directly — they may cause crashes or undefined behavior.

## Contributing

Contributions are welcome! Please feel free to open a pull request or create an issue to add new awesome LXQt resources. When adding new entries, please ensure:

- The project is actively maintained (or historically significant).
- Links are valid and functional.
- Entries are categorized correctly under X11, Wayland, or both.

## License

[![CC0](https://licensebuttons.net/p/zero/1.0/88x31.png)](https://creativecommons.org/publicdomain/zero/1.0/)
