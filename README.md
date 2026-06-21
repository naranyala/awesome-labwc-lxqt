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
  - [Development](#development)
  - [Utilities](#utilities)
  - [CLI & TUI Utilities](#cli--tui-utilities)
  - [Games](#games)
- [CLI & TUI Tools](#cli--tui-tools)
  - [System Monitors](#system-monitors)
  - [File Managers](#file-managers)
  - [Text Editors](#text-editors)
  - [Terminal Multiplexers](#terminal-multiplexers)
  - [Audio (CLI/TUI)](#audio-clitui)
  - [Note-Taking & Productivity (TUI)](#note-taking--productivity-tui)
  - [File Navigation & Searching](#file-navigation--searching)
  - [Git Tools (TUI)](#git-tools-tui)
  - [Network & Download (CLI)](#network--download-cli)
  - [System Info & Utilities](#system-info--utilities)
  - [Shell Prompt Enhancements](#shell-prompt-enhancements)
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
- [Themes & Customization](#themes--customization)
- [Dotfiles & Ricing Setup](#dotfiles--ricing-setup)
  - [LXQt Configuration Files](#lxqt-configuration-files)
  - [Autostart & Session Setup](#autostart--session-setup)
  - [Keybindings & Shortcuts](#keybindings--shortcuts)
  - [Menu & Desktop Entries](#menu--desktop-entries)
  - [LXQt + Openbox Integration](#lxqt--openbox-integration)
  - [LXQt + Labwc Integration (Wayland)](#lxqt--labwc-integration-wayland)
  - [LXQt + Tiling WM Integration](#lxqt--tiling-wm-integration)
  - [Emacs & LXQt Integration](#emacs--lxqt-integration)
  - [qt5ct / qt6ct Setup](#qt5ct--qt6ct-setup)
  - [Font Configuration](#font-configuration)
  - [Cursor Configuration](#cursor-configuration)
  - [Shell Configuration](#shell-configuration)
  - [Xresources / Xdefaults (X11)](#xresources--xdefaults-x11)
  - [Wayland environment.d Configuration](#wayland-environmentd-configuration)
  - [Performance Tuning & Optimization](#performance-tuning--optimization)
  - [Multi-Monitor Setup](#multi-monitor-setup)
  - [Backup & Restore](#backup--restore)
  - [Kvantum Setup & Theming](#kvantum-setup--theming)
  - [Managing Theme Assets](#managing-theme-assets)
  - [Dotfile Management](#dotfile-management)
  - [Community Rices & Dotfile Repos](#community-rices--dotfile-repos)
  - [LXQt-Specific Ricing Tips](#lxqt-specific-ricing-tips)
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

### Development

- **[Qt Creator](https://www.qt.io/product/development-tools)** - Official Qt IDE; the best tool for developing Qt/LXQt applications.
- **[KDevelop](https://www.kdevelop.org/)** - Cross-platform IDE for C/C++/Python and more (Qt/KDE-based).
- **[VSCodium](https://vscodium.com/)** - Free/Libre Open Source Software alternative to VS Code (Electron, but popular).
- **[Geany](https://www.geany.org/)** - Lightweight GTK IDE; fast on LXQt.
- **[Lite XL](https://lite-xl.com/)** - A lightweight, extensible text editor written in Lua.
- **[Kate](https://kate-editor.org/)** - KDE's advanced text editor with multi-cursor, MDI, and IDE features.
- **[ReText](https://github.com/retext-project/retext)** - Simple Markdown editor with live preview (Qt-based).
- **[Gittyup](https://github.com/Murmele/Gittyup)** - Qt-based Git GUI client.
- **[QGit](https://github.com/tibirna/qgit)** - A simple Qt Git GUI viewer/browser.
- **Magit** (Emacs) - The definitive Git porcelain within Emacs. Stage, commit, branch, rebase, diff, and browse history without leaving the editor. Integrates with `forge` for GitHub/GitLab issue and PR management. Considered by many the best Git interface on any platform.

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

### Games

- **[Minetest](https://www.minetest.net/)** - Open-source voxel game engine (Minecraft-like), Qt-based.
- **[0 A.D.](https://play0ad.com/)** - Historical RTS game (uses Qt for some UI).
- **[OpenRA](https://www.openra.net/)** - Classic RTS engine reimplementation (C#/.NET, runs well).
- **[Warzone 2100](https://wz2100.net/)** - 3D RTS with Qt-based UI.
- **[Supertuxkart](https://supertuxkart.net/)** - 3D kart racing game.
- **[FlightGear](https://www.flightgear.org/)** - Flight simulator with Qt-based launcher.
- **[Lutris](https://lutris.net/)** - Open gaming platform (GTK, but essential for gaming on Linux).
- **[Steam](https://store.steampowered.com/)** - Steam client (uses Qt for some UI components).
- **[Heroic Games Launcher](https://heroicgameslauncher.com/)** - Epic Games and GOG launcher (Electron, but works well).

## CLI & TUI Tools

Terminal-based tools that complement an LXQt dotfiles/ricing setup — lightweight, scriptable, and ideal for keyboard-driven workflows.

### System Monitors

- **[btop](https://github.com/aristocratos/btop)** - A modern, colorful resource monitor with CPU, RAM, disk, network, and process management. GPU support via `nvtop`.
- **[htop](https://github.com/htop-dev/htop)** - The classic interactive process viewer. Lightweight and universally available.
- **[glances](https://nicolargo.github.io/glances/)** - A cross-platform monitoring tool with CLI, web, and REST API modes. Plugin system for extensibility.
- **[nvtop](https://github.com/Syllo/nvtop)** - GPU process monitor for NVIDIA, AMD, and Intel GPUs. Like htop for GPUs.
- **[procs](https://github.com/dalance/procs)** - A modern replacement for `ps` with color-coded output, tree view, and watch mode.
- **[nmon](https://nmon.sourceforge.net/)** - Performance monitoring tool for CPU, memory, network, disks, and more. Saves data to CSV for later analysis.
- **[bottom](https://github.com/ClementTsang/bottom)** - A cross-platform graphical process/system monitor with a customizable TUI (similar to btop).

### File Managers

- **[yazi](https://github.com/sxyazi/yazi)** - A blazing-fast terminal file manager written in Rust. Vim-like keybindings, image preview (via `chafa`/`ueberzug`), and async I/O.
- **[nnn](https://github.com/jarun/nnn)** - A tiny, lightning-fast file manager with disk usage analyzer, fuzzy search, and plugin system. Extremely minimal.
- **[lf](https://github.com/gokcehan/lf)** - A terminal file manager written in Go, inspired by ranger. Client-server architecture, image previews, and extensive config.
- **[ranger](https://github.com/ranger/ranger)** - A classic vim-inspired file manager with file previews, multi-pane view, and bulk rename. Highly extensible with Python.
- **[vifm](https://github.com/vifm/vifm)** - A curses-based file manager with vi-like keybindings. Supports two-pane view, regex filtering, and FUSE mounts.
- **[broot](https://github.com/Canop/broot)** - A new way to see and navigate directories. Fuzzy tree view, file preview, and auto-completion.
- **[mc (Midnight Commander)](https://midnight-commander.org/)** - The classic two-pane file manager. Feature-rich, scriptable, and available everywhere.

### Text Editors

- **[Neovim](https://github.com/neovim/neovim)** - A modern fork of Vim. Extensible with Lua, built-in LSP client, tree-sitter, and a thriving plugin ecosystem. Ideal for LXQt config editing.
- **[Helix](https://helix-editor.com/)** - A modal terminal editor with built-in LSP, tree-sitter, and multiple selections. Kakoune-inspired (no config needed for basics).
- **[Kakoune](https://kakoune.org/)** - A modal editor with multiple selections, client-server architecture, and a focus on interactive editing.
- **[micro](https://github.com/zyedidia/micro)** - A modern, intuitive terminal editor. Mouse support, built-in file manager, and familiar keybindings (Ctrl+S, Ctrl+Q).
- **[nano](https://www.nano-editor.org/)** - The simplest terminal editor. Pre-installed on most systems. Great for quick config edits.
- **[Emacs (GUI & terminal)](https://www.gnu.org/software/emacs/)** - The extensible, self-documenting editor. Runs in GUI mode (native with X11/Wayland) or terminal (`-nw`). With its ecosystem (Org, Magit, Dired, Mu4e, Elfeed, EXWM), Emacs can replace a dozen separate applications — a natural fit for a lightweight LXQt + Emacs workflow.
  - **[Doom Emacs](https://github.com/doomemacs/doomemacs)** - A highly acclaimed configuration framework for Emacs tailored for Vim users and those seeking a fast, modern setup.
  - **[Spacemacs](https://www.spacemacs.org/)** - A community-driven Emacs distribution featuring a mnemonic space-bar keybinding setup.
  - **Daemon mode**: `emacs --daemon` + `emacsclient -c` for instant startup. Manage as a systemd user service: `systemctl --user enable --now emacs`.
  - **EXWM**: Emacs X Window Manager ([exwm](https://github.com/emacs-exwm/exwm)) — run EXWM as LXQt's X11 window manager. LXQt provides the panel, tray, and system services; Emacs manages windows entirely with keyboard-driven keybindings.
  - **EAF**: Emacs Application Framework ([eaf](https://github.com/emacs-eaf/emacs-application-framework)) — embed web browsers, PDF viewers, file managers, and terminals as Emacs buffers. Complements LXQt by bringing GUI apps inside the Emacs workflow.
  - **Key packages for dotfiles ricing**:
    - `use-package` / `straight.el` — declarative package management.
    - `org-mode` — note-taking, todo management, literate config (`init.org` → `init.el`).
    - `magit` — the gold-standard Git porcelain.
    - `dired` — file manager with image preview, git integration, and wdired (editable filenames).
    - `mu4e` / `notmuch` — email within Emacs.
    - `elfeed` — RSS/Atom feed reader.
    - `erc` / `rcirc` — IRC client.
    - `emms` / `bongo` — music player.
    - `pdf-tools` — PDF viewer with annotations.
    - `vterm` — terminal emulator within Emacs.
    - `centaur-tabs` / `awesome-tab` — tabbed buffers.
    - `doom-themes` / `ef-themes` — color schemes that can be matched to LXQt/Kvantum themes.
    - `solitaire` / `2048-game` — killing time without leaving Emacs.

### Terminal Multiplexers

- **[tmux](https://github.com/tmux/tmux)** - A terminal multiplexer with session persistence, split panes, customizable keybindings, and scriptable window management. Integral to many dotfiles setups.
- **[Zellij](https://zellij.dev/)** - A terminal multiplexer with a user-friendly layout, built-in plugin system, and clutter-free defaults (no config needed to start).
- **[screen](https://www.gnu.org/software/screen/)** - The classic terminal multiplexer. Pre-installed on nearly every system. Lightweight but less feature-rich.
- **[dtach](https://github.com/crigler/dtach)** - A minimal program that emulates the detach feature of screen/tmux. Attach/detach a single program from a terminal.

### Audio (CLI/TUI)

- **[cmus](https://cmus.github.io/)** - A small, fast, and powerful TUI music player. Vim-style navigation, playlist management, and library browser.
- **[ncmpcpp](https://github.com/ncmpcpp/ncmpcpp)** - A feature-rich TUI client for MPD (Music Player Daemon). Tag editor, visualizer, and lyric display. Works alongside `mpd` + `mpc`.
- **[mpc](https://musicpd.org/clients/mpc/)** - A command-line client for MPD. Ideal for keybinding audio controls (`mpc toggle`, `mpc next`, `mpc volume +5`).
- **[pulsemixer](https://github.com/GeorgeFilipkin/pulsemixer)** - A TUI mixer for PulseAudio/PipeWire. Per-app volume control, sink switching, and profile management.
- **[alsamixer](https://alsa-project.org/)** - The standard ALSA TUI mixer. Works on bare ALSA or as a fallback for PulseAudio/PipeWire.
- **[ffplay](https://ffmpeg.org/ffplay.html)** - A minimal CLI video/audio player from FFmpeg. Great for quick playback without leaving the terminal.

### Note-Taking & Productivity (TUI)

- **[pass](https://www.passwordstore.org/)** - The standard Unix password manager. GPG-encrypted, Git-backed, and scriptable. Complements LXQt with `passmenu` (rofi/dmenu integration).
- **[gopass](https://www.gopass.pw/)** - A modern rewrite of pass with team support, binary storage, auto-sync, and a TUI interface.
- **[taskwarrior](https://taskwarrior.org/)** - A powerful task management CLI. Syncs with `taskd` or `taskserver`. Integrates with `vit` for a TUI frontend.
- **[calcurse](https://calcurse.org/)** - A calendar and scheduling TUI. Supports todo list, appointments, and recurring events. Import/export via iCal.
- **[newsboat](https://newsboat.org/)** - A TUI RSS/Atom feed reader with podcast support, filter, and integration with podcast-dl.
- **[nb](https://github.com/xwmx/nb)** - A note-taking CLI with Git-backed versioning, encryption, and Markdown rendering.
- **[taskell](https://taskell.app/)** - A TUI kanban board for task management. Markdown-based, simple to use.

### File Navigation & Searching

- **[fzf](https://github.com/junegunn/fzf)** - A general-purpose fuzzy finder. Pipe anything into it. Integrates with shell (Ctrl+R, Alt+C), vim/neovim, tmux, and application launchers.
- **[fd](https://github.com/sharkdp/fd)** - A fast and user-friendly alternative to `find`. Colorized output, regex/glob support, parallel traversal.
- **[ripgrep (rg)](https://github.com/BurntSushi/ripgrep)** - A line-oriented search tool that recursively searches directories for regex patterns. Faster than `grep`, respects `.gitignore`.
- **[bat](https://github.com/sharkdp/bat)** - A `cat` clone with syntax highlighting, Git integration, and line numbers. Pairs with `fzf` and `ripgrep` for code inspection.
- **[eza](https://github.com/eza-community/eza)** - A modern replacement for `ls`. Color icons, tree view, Git status, and extended attributes. Fork of `exa`.
- **[zoxide](https://github.com/ajeetdsouza/zoxide)** - A smarter `cd` command that learns your habits. Jump to any directory with `z <fragment>`. Works with all major shells.
- **[duf](https://github.com/muesli/duf)** - A disk usage/ free utility with colored output, JSON export, and device filtering.
- **[ncdu](https://dev.yorhel.nl/ncdu)** - A TUI disk usage analyzer. Fast, minimal, and great for finding large directories.
- **[gdu](https://github.com/dundee/gdu)** - A disk usage analyzer written in Go. Faster than ncdu on SSDs, with parallel traversal and TUI/CLI modes.
- **[dust](https://github.com/bootandy/dust)** - A more intuitive `du`. Shows disk usage in a tree view with the largest directories highlighted.
- **[hyperfine](https://github.com/sharkdp/hyperfine)** - A command-line benchmarking tool. Useful for testing LXQt startup or script performance.
- **[sd](https://github.com/chmln/sd)** - An intuitive find & replace CLI. Simpler and faster than `sed` for most text replacement tasks.
- **[delta](https://github.com/dandavison/delta)** - A syntax-highlighting pager for `git diff`, `blame`, and `grep` output. Works with bat's themes.
- **[doggo](https://github.com/mr-karan/doggo)** - A modern DNS lookup CLI with colorful output and JSON formatting. A friendly alternative to `dig`/`nslookup`.
- **[httpie](https://httpie.io/cli)** - A user-friendly CLI HTTP client with JSON support, syntax highlighting, and session management.

### Git Tools (TUI)

- **[lazygit](https://github.com/jesseduffield/lazygit)** - A TUI Git client with intuitive keybindings. Stage, commit, branch, rebase, and resolve conflicts without leaving the terminal.
- **[gitui](https://github.com/extrawurst/gitui)** - A blazing-fast TUI Git client written in Rust. Vim keys, mouse support, and asynchronous operations.
- **[tig](https://github.com/jonas/tig)** - A text-mode interface for Git. Browse commits, diff, blame, stash, and refs with vim-like navigation.
- **[gh (GitHub CLI)](https://cli.github.com/)** - Manage GitHub repositories, issues, PRs, and releases from the command line.

### Network & Download (CLI)

- **[yt-dlp](https://github.com/yt-dlp/yt-dlp)** - A feature-rich command-line audio/video downloader. Supports YouTube, hundreds of sites, and post-processing (FFmpeg integration).
- **[aria2c](https://aria2.github.io/)** - A lightweight, multi-protocol CLI download utility. Supports HTTP/HTTPS, FTP, SFTP, BitTorrent, and Metalink. Chunked downloads for speed.
- **[nmtui](https://networkmanager.dev/docs/api/latest/nmtui.html)** - A TUI frontend for NetworkManager. Connect to WiFi, edit connections, activate/deactivate without a GUI applet.
- **[nmcli](https://networkmanager.dev/docs/api/latest/nmcli.html)** - NetworkManager's command-line tool. Scriptable WiFi/ethernet/VPN management. Essential for headless LXQt setups.
- **[iwctl](https://iwd.wiki.kernel.org/)** - iNet Wireless Daemon's interactive TUI. Scan, connect, and manage WiFi networks with a clean interface.
- **[termshark](https://github.com/gcla/termshark)** - A TUI frontend for Wireshark (tshark). Capture and analyze network traffic interactively in the terminal.
- **[bandwhich](https://github.com/imsnif/bandwhich)** - A CLI network bandwidth utilization tool. Displays per-process/connection usage in real-time.

### System Info & Utilities

- **[fastfetch](https://github.com/fastfetch-cli/fastfetch)** - A neofetch-like system information tool written in C. Extremely fast, highly customizable, with JSON output and built-in logo support.
- **[neofetch](https://github.com/dylanaraps/neofetch)** - The classic command-line system info tool. Displays logo, OS, kernel, uptime, and hardware details. Used in countless ricing screenshots.
- **[pfetch](https://github.com/dylanaraps/pfetch)** - A minimalist system info tool in a single shell script. Very fast and dependency-free.
- **[macchina](https://github.com/Macchina-CLI/macchina)** - A system information frontend with a focus on performance and customizability. Written in Rust, themeable output.
- **[jq](https://jqlang.github.io/jq/)** - A lightweight and flexible command-line JSON processor. Essential for scripting with APIs and config files.
- **[yq](https://github.com/mikefarah/yq)** - A portable command-line YAML/JSON/XML processor. Useful for manipulating YAML config files programmatically.
- **[lnav](https://lnav.org/)** - A log file navigator with syntax highlighting, timeline view, and SQL-based filtering for log analysis.

### Shell Prompt Enhancements

- **[starship](https://starship.rs/)** - A minimal, fast, and infinitely customizable shell prompt. Works with any shell (bash, zsh, fish, etc.). Preset themes available.
- **[oh-my-posh](https://ohmyposh.dev/)** - A prompt theme engine for any shell. Windows/macOS/Linux support, JSON/YAML themes, and Git status segments.
- **[powerlevel10k](https://github.com/romkatv/powerlevel10k)** - A fast zsh theme with prompt customization wizard, instant prompt, and transient prompt. The most popular Zsh theme.
- **[zinit](https://github.com/zdharma-continuum/zinit)** - A flexible Zsh plugin manager with turbo loading, completions, and snippet support. Keeps Zsh startup fast.
- **[sheldon](https://sheldon.cli.rs/)** - A fast, configurable shell plugin manager. Supports Rust crates, Git repos, and inline plugins.

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

## Themes & Customization

- **[Kvantum](https://github.com/tsujan/Kvantum)** - An SVG-based theme engine for Qt. Essential for deeply customizing the look of LXQt apps. Includes blur, transparency, and animations.
- **[QtCurve](https://github.com/qtcurve/qtcurve)** - A configurable Qt and GTK style engine. Highly tweakable.
- **[Papirus Icon Theme](https://github.com/PapirusDevelopmentTeam/papirus-icon-theme)** - A comprehensive, open-source SVG icon theme. Looks great on LXQt. Includes Papirus-Dark, Papirus-Light variants.
- **[Tela Icon Theme](https://github.com/vinceliuice/Tela-icon-theme)** - A flat, colorful icon theme with circle/circle-black/ubuntu variants.
- **[Qogir Icon Theme](https://github.com/vinceliuice/Qogir-icon-theme)** - A flat, round icon theme with a modern aesthetic.
- **[We10X Icon Theme](https://github.com/Atlas-64bit/We10X-icon-theme)** - Windows 10/11-style icon theme.
- **[Breeze (Qt/GTK)](https://invent.kde.org/plasma/breeze)** - KDE's default theme engine and icon set. Works flawlessly with LXQt.
- **[Breeze Enhanced](https://github.com/tsujan/BreezeEnhanced)** - A patched Breeze theme with transparent and blur effects for Kvantum.
- **[LXQt Themes](https://github.com/lxqt/lxqt-themes)** - The default set of themes bundled with LXQt (Frost, Dark, Ambiance, etc.).
- **[Arc KDE](https://github.com/PapirusDevelopmentTeam/arc-kde)** - Arc theme adapted for KDE/Qt. Includes stylish window decorations.
- **[Materia KDE](https://github.com/PapirusDevelopmentTeam/materia-kde)** - Material Design theme for KDE/Qt.
- **[Adapta KDE](https://github.com/PapirusDevelopmentTeam/adapta-kde)** - Adapta theme adapted for Qt/KDE.
- **[Orchis Theme](https://github.com/vinceliuice/Orchis-theme)** - A Material Design theme for GNOME/GTK, with Qt/Kvantum variant available.
- **[Nordic Theme](https://github.com/EliverLara/Nordic)** - A dark theme using the Nord color palette (GTK with Kvantum variants).
- **[Catppuccin](https://github.com/catppuccin/catppuccin)** - A community-driven pastel theme with four variants (latte, frappe, macchiato, mocha). Has Kvantum ports.
- **[Fluent Theme](https://github.com/vinceliuice/Fluent-kde)** - Fluent Design-style KDE/Qt theme.
- **[WhiteSur Theme](https://github.com/vinceliuice/WhiteSur-kde)** - A macOS-style KDE/Qt theme.
- **[SDDM Themes](https://github.com/lxqt/lxqt-sddm-themes)** - LXQt-themed SDDM login manager themes.
- **[Bibata Cursor](https://github.com/ful1e5/Bibata_Cursor)** - Modern, customizable cursor theme with Material Design influence.
- **[Capitaine Cursors](https://github.com/keeferrourke/capitaine-cursors)** - A macOS-inspired cursor theme.
- **[Fonts](https://www.nerdfonts.com/)** - Nerd Fonts patched for developer icons and powerline symbols. Popular: FiraCode, JetBrains Mono, Hack, Meslo.

## Dotfiles & Ricing Setup

A deep dive into configuring, customizing, and ricing LXQt. This section covers LXQt's configuration files, integration with window managers, autostart, keybindings, and community rice repositories.

### LXQt Configuration Files

LXQt stores all configuration in `~/.config/lxqt/`. Here are the key files:

- **`~/.config/lxqt/lxqt.conf`** - Global LXQt settings: theme, icon theme, font, double-click interval, single-instance apps, and terminal emulator override.
- **`~/.config/lxqt/panel.conf`** - Panel layout: position, size, screen, and plugin list. Each plugin has a numbered section with individual settings.
- **`~/.config/lxqt/session.conf`** - Session management: which window manager to launch, compositor command, auto-start apps, and environment variables.
- **`~/.config/lxqt/globalkeys.state`** - Global keyboard shortcuts. Managed by `lxqt-globalkeys`. Editable via GUI or manually.
- **`~/.config/lxqt/lxqt-runner.conf`** - `lxqt-runner` settings: history size, plugins enabled (apps, desktop files, calculations, terminal commands).
- **`~/.config/lxqt/desktop.conf`** - Desktop/icon settings by `pcmanfm-qt`: icon size, grid, label customization, wallpaper.
- **`~/.config/lxqt/notificationd.conf`** - Notification daemon settings: position, timeout, opacity, font, and per-application overrides.
- **`~/.config/lxqt/powermanagement.conf`** - Power management settings: lid close action, critical battery, idle inhibition.
- **`~/.config/lxqt/lxqt-config.conf`** - LXQt Config Center settings: keyboard layout, mouse speed, monitor configuration.
- **`~/.config/lxqt/lximage-qt.conf`** - Image viewer settings: slideshow interval, background color, fit mode.

### Autostart & Session Setup

LXQt runs a limited set of startup items declared in `session.conf` and the XDG autostart directories. There are multiple ways to launch services on login:

- **`~/.config/lxqt/session.conf`** - The `[Environment]` block exports env vars. The `[QtEnv]` block sets `QT_QPA_PLATFORMTHEME`, `QT_STYLE_OVERRIDE`, etc. Example:

  ```ini
  [General]
  __userfile__=true

  [QtEnv]
  environment=QT_STYLE_OVERRIDE=kvantum
  environment=QT_QPA_PLATFORMTHEME=lxqt

  [Environment]
  environment=GTK_THEME=Adwaita-dark
  environment=EDITOR=nano

  [Session]
  window_manager=openbox
  ```
- **`~/.config/autostart/*.desktop`** - XDG autostart. Place `.desktop` files here. Examples:
  - `picom --config ~/.config/picom.conf`
  - `nm-applet`
  - `lxqt-policykit-agent`
- **`~/.config/lxqt/autostart`** - LXQt legacy autostart (symlinks or `.desktop` files). Overrides XDG autostart for the LXQt session.
- **Custom startup scripts** - For complex setups, call a script from `Exec=` in a `.desktop` file:

  ```bash
  #!/bin/bash
  # ~/.config/autostart/startup.sh
  picom --config ~/.config/picom/picom.conf &
  /usr/lib/polkit-gnome/polkit-gnome-authentication-agent-1 &
  nitrogen --restore &
  ```
- **Conditional autostart per compositor** - Detect the WM and launch accordingly:

  ```bash
  # In session.conf, set window_manager=openbox
  # Then in an autostart .desktop file:
  Exec=bash -c 'if pgrep -x openbox; then picom & fi'
  ```

### Keybindings & Shortcuts

LXQt manages global keyboard shortcuts via `lxqt-globalkeys`. The state file is `~/.config/lxqt/globalkeys.state`.

**GUI configuration**: LXQt Config Center → Shortcut Settings.

**Manual editing** (`globalkeys.state`):

```ini
[QtKeyConf]
shortcut_1=XF86AudioLowerVolume
shortcut_1/Exec=pactl set-sink-volume @DEFAULT_SINK@ -5%
shortcut_1/Comment=Volume Down

shortcut_2=XF86AudioRaiseVolume
shortcut_2/Exec=pactl set-sink-volume @DEFAULT_SINK@ +5%
shortcut_2/Comment=Volume Up

shortcut_3=XF86AudioMute
shortcut_3/Exec=pactl set-sink-mute @DEFAULT_SINK@ toggle
shortcut_3/Comment=Mute

shortcut_4=Ctrl+Alt+T
shortcut_4/Exec=qterminal
shortcut_4/Comment=Launch Terminal

shortcut_5=Alt+F2
shortcut_5/Exec=lxqt-runner
shortcut_5/Comment=Runner

shortcut_6=Print
shortcut_6/Exec=screengrab --current
shortcut_6/Comment=Screenshot current window

shortcut_7=Ctrl+Alt+L
shortcut_7/Exec=lxqt-sudo --lock
shortcut_7/Comment=Lock Screen
```

**WM-specific keybindings** - When using a standalone WM like Openbox or i3, manage window-related shortcuts there (e.g., `rc.xml` for Openbox, `config` for i3). LXQt globalkeys handles desktop/panel shortcuts.

### Menu & Desktop Entries

LXQt builds its application menu from `.desktop` files following the freedesktop.org XDG specification.

- **Menu location**: `~/.config/menus/lxqt-applications.menu` (user override) or `/etc/xdg/menus/lxqt-applications.menu` (system).
- **Custom `.desktop` files**: Place in `~/.local/share/applications/`. Example:

  ```desktop
  [Desktop Entry]
  Name=My Script
  Exec=/home/user/bin/myscript.sh
  Icon=utilities-terminal
  Terminal=true
  Type=Application
  Categories=Utility;
  ```
- **Edit the menu**: Use `lxqt-menu-editor` (GUI) or edit the `.menu` XML file manually to hide entries, reorder categories, or add custom submenus.
- **Favorites in Fancy Menu**: Right-click the Fancy Menu button and choose "Pin to favorites" or edit `~/.config/lxqt/panel.conf` under the Fancy Menu plugin section.

### LXQt + Openbox Integration

Openbox is the default and most mature X11 window manager for LXQt. Here's how to configure them together:

**`~/.config/openbox/rc.xml`** - Key bindings, mouse bindings, desktop behavior, window placement, margins:

```xml
<openbox_config>
  <desktops>
    <number>4</number>
    <names>
      <name>1:Term</name>
      <name>2:Web</name>
      <name>3:Code</name>
      <name>4:Misc</name>
    </names>
  </desktops>
  <resistance>
    <move>8</move>
  </resistance>
  <mouse>
    <dragThreshold>4</dragThreshold>
    <doubleClickTime>300</doubleClickTime>
  </mouse>
  <keyboard>
    <keybind key="W-d">
      <action name="ToggleShowDesktop"/>
    </keybind>
    <keybind key="A-F4">
      <action name="Close"/>
    </keybind>
    <keybind key="A-Space">
      <action name="ShowMenu"><menu>client-menu</menu></action>
    </keybind>
  </keyboard>
</openbox_config>
```

**`~/.config/openbox/menu.xml`** - Custom right-click desktop menu. Can include LXQt components:

```xml
<openbox_menu>
  <menu id="root-menu" label="Openbox 3">
    <item label="Terminal"><action name="Execute"><command>qterminal</command></action></item>
    <item label="File Manager"><action name="Execute"><command>pcmanfm-qt</command></action></item>
    <item label="Runner"><action name="Execute"><command>lxqt-runner</command></action></item>
    <separator/>
    <item label="Configuration"><action name="Execute"><command>lxqt-config</command></action></item>
    <separator/>
    <item label="Lock Screen"><action name="Execute"><command>lxqt-sudo --lock</command></action></item>
    <item label="Log Out"><action name="Execute"><command>lxqt-leave --logout</command></action></item>
  </menu>
</openbox_menu>
```

**`~/.config/openbox/autostart`** - Openbox autostart script runs *before* LXQt session starts. Use for compositor and WM-level tools:

```bash
# ~/.config/openbox/autostart
picom --config ~/.config/picom/picom.conf &
nitrogen --restore &
setxkbmap us,ir -option grp:alt_shift_toggle
xset r rate 250 40
```

**Theme integration** - Openbox themes (`.obt` or extracted in `/usr/share/themes/`) determine window borders and titlebars. Use `obconf-qt` (bundled with LXQt) or `lxqt-config` → "Window Manager" to switch them.

### LXQt + Labwc Integration (Wayland)

Labwc is the recommended lightweight Wayland compositor for LXQt 2.0+. It parses Openbox themes and config files, making migration easy.

**`~/.config/labwc/rc.xml`** - Labwc uses the same XML format as Openbox with Wayland-specific extensions:

```xml
<labwc_config>
  <core>
    <gap>6</gap>
    <decoration>server</decoration>
  </core>
  <placement>
    <policy>center</policy>
  </placement>
  <desktops>
    <number>4</number>
    <names>
      <name>1:Term</name>
      <name>2:Web</name>
      <name>3:Code</name>
      <name>4:Misc</name>
    </names>
  </desktops>
  <keyboard>
    <keybind key="W-Return">
      <action name="Execute"><command>qterminal</command></action>
    </keybind>
    <keybind key="W-d">
      <action name="ToggleShowDesktop"/>
    </keybind>
    <keybind key="A-F4">
      <action name="Close"/>
    </keybind>
  </keyboard>
  <windowRules>
    <windowRule identifier="lxqt-panel">
      <action name="Ignore"/>
    </windowRule>
  </windowRules>
</labwc_config>
```

**`~/.config/labwc/autostart`** - Shell script for Wayland-specific autostarts:

```bash
# ~/.config/labwc/autostart
swaybg -i ~/wallpapers/current.jpg &
waybar &
/usr/libexec/polkit-kde-authentication-agent-1 &
```

**Running LXQt on Labwc**: Set `window_manager=labwc` in `lxqt-session.conf`. LXQt will launch Labwc as its Wayland compositor, and the panel will use the `wlr-foreign-toplevel` backend for task management.

### LXQt + Tiling WM Integration

LXQt pairs well with tiling window managers. The key is letting the WM manage windows while LXQt provides the panel, runner, and system tray.

**LXQt + i3** (`~/.config/i3/config`):

```conf
# i3 config for LXQt integration
exec --no-startup-id lxqt-session
exec --no-startup-id picom

# Use LXQt runner instead of i3's dmenu
bindsym $mod+d exec lxqt-runner

# Volume via LXQt keys
bindsym XF86AudioRaiseVolume exec pactl set-sink-volume @DEFAULT_SINK@ +5%
bindsym XF86AudioLowerVolume exec pactl set-sink-volume @DEFAULT_SINK@ -5%

# Status bar: use i3status or hide i3bar and use lxqt-panel instead
bar {
  status_command i3status
  # Or disable entirely and rely on lxqt-panel:
  # mode invisible
}
```

**LXQt + bspwm** (`~/.config/bspwm/bspwmrc`):

```bash
# bspwmrc with LXQt
lxqt-session &
picom &
pgrep -x sxhkd >/dev/null || sxhkd &
```

**LXQt + Hyprland** (`~/.config/hypr/hyprland.conf`):

```conf
# Hyprland with LXQt
exec-once = lxqt-session

# LXQt panel layer rule
windowrulev2 = float, class:(lxqt-panel)
windowrulev2 = pin, class:(lxqt-panel)
windowrulev2 = move 0 0, class:(lxqt-panel)
windowrulev2 = nofocus, class:(lxqt-panel)
windowrulev2 = noblur, class:(lxqt-panel)
windowrulev2 = noshadow, class:(lxqt-panel)
windowrulev2 = noanim, class:(lxqt-panel)

# LXQt desktop window (pcmanfm-qt desktop)
windowrulev2 = float, class:(pcmanfm-qt), title:(Desktop)
windowrulev2 = pin, class:(pcmanfm-qt), title:(Desktop)
windowrulev2 = noblur, class:(pcmanfm-qt), title:(Desktop)
windowrulev2 = noshadow, class:(pcmanfm-qt), title:(Desktop)
windowrulev2 = nofocus, class:(pcmanfm-qt), title:(Desktop)
windowrulev2 = ignorezerolimits, class:(pcmanfm-qt), title:(Desktop)

# Regular windows
windowrulev2 = float, title:^(LXQt Configuration Center)$
windowrulev2 = float, title:^(About LXQt)$
```

### Emacs & LXQt Integration

Emacs pairs exceptionally well with LXQt — either as a WM replacement (EXWM) or as a power-user toolkit alongside the default setup. Below are key integration points for an Emacs-centric LXQt dotfiles setup:

- **EXWM as LXQt's X11 window manager**: Set `window_manager=exwm` in `~/.config/lxqt/session.conf`. LXQt provides the panel, system tray, notifications, and power management while EXWM manages windows. Create a desktop entry at `~/.local/share/xsessions/exwm.desktop` or use LXQt's session manager to launch EXWM directly.
- **Emacs daemon management**: Add a systemd user service for the Emacs daemon to ensure it starts with LXQt:
  ```ini
  # ~/.config/systemd/user/emacs.service
  [Unit]
  Description=Emacs text editor (daemon)

  [Service]
  Type=simple
  ExecStart=/usr/bin/emacs --daemon
  Restart=on-failure

  [Install]
  WantedBy=default.target
  ```
  Enable with: `systemctl --user enable --now emacs.service`. Then use `emacsclient -c` (GUI) or `emacsclient -nw` (terminal) for instant startup.
- **Keybindings compatibility**: Avoid conflicts between LXQt global shortcuts and Emacs keybindings:
  - Remap LXQt shortcuts that clash with Emacs (e.g., `Alt+W` for copy in Emacs vs LXQt window operations).
  - Set LXQt to use `Super` (Windows key) as its primary modifier, leaving `Alt` and `Ctrl` free for Emacs.
  - In EXWM, use `s-` (Super) prefix for EXWM window management commands to avoid conflicts with Emacs.
- **Theming harmony**: Match Emacs and LXQt themes for a unified look:
  - Kvantum theme + `doom-one` Emacs theme for dark cohesive aesthetics.
  - Catppuccin is available for both [LXQt/Kvantum](https://github.com/catppuccin/kvantum) and [Emacs](https://github.com/catppuccin/emacs).
  - Set Emacs font to match the system font: `(set-frame-font "JetBrains Mono 11")`.
  - Sync cursor color and size between Emacs and LXQt via `(set-cursor-color "#cdd6f4")`.
- **GTK integration in Emacs**: When running Emacs GUI on Wayland, set `GDK_BACKEND=wayland` and `EMACS_GTK_OVERLAY_SCROLLING=1` for native scrollbar behavior.
- **Org-mode as a desktop hub**: Use Org capture to quickly log tasks from LXQt — bind `lxqt-runner` or a global shortcut to an Emacs client org-capture command:
  ```bash
  emacsclient -e '(org-capture)' 2>/dev/null || emacs --daemon && emacsclient -e '(org-capture)'
  ```
- **Emacs as a launcher**: Emacs `M-x` can replace `lxqt-runner`. Add a global shortcut in LXQt to spawn an Emacs client with a Helm/Ivy/Vertico session for app launching, file searching, and calculator.
- **Magit for dotfile management**: Manage Git-based dotfiles ([GNU Stow](#dotfile-management), [Chezmoi](#dotfile-management)) entirely within Emacs via Magit. Bind `C-x g` to open Magit-status in your LXQt dotfiles repository.
- **Emacs on Wayland**: Emacs 29+ supports native Wayland frames via `--with-pgtk`. Set `GDK_BACKEND=wayland` and launch with `emacs -nw` for a terminal experience or `emacs` for GUI. EXWM is X11-only, so pair Emacs GUI + PGTK with Labwc, Sway, or Hyprland on Wayland.

### qt5ct / qt6ct Setup

These tools provide a GUI to configure Qt appearance when desktop-specific settings (like `lxqt-qtplugin`) are not enough.

- **[qt5ct](https://sourceforge.net/projects/qt5ct/)** - Qt5 Settings Controller. Select widget style (Breeze, Kvantum, Fusion), font, icon theme, and color palette.
- **[qt6ct](https://sourceforge.net/projects/qt6ct/)** - Same as qt5ct but for Qt6 applications. Required for LXQt 2.0+ and Qt6 apps.
- **Usage**: Set `QT_QPA_PLATFORMTHEME=qt5ct` (or `qt6ct`) in `~/.config/lxqt/session.conf` or in your shell profile. Open `qt5ct` or `qt6ct` GUI to configure.
- **Override per-application Qt theme**: `QT_STYLE_OVERRIDE=fusion QT_QPA_PLATFORMTHEME=qt5ct qt-app-name`
- **Force dark palette**: In qt5ct/qt6ct, select a dark color scheme, or use `qt5ct-dark`/`qt6ct-dark` style if packaged.

### Kvantum Setup & Theming

Kvantum is an SVG-based theme engine for Qt that is essential for deeply customizing LXQt apps.

- **Configuration Path**: `~/.config/Kvantum/` and `~/.config/Kvantum/kvantum.kvconfig`.
- **Management GUI**: Use `kvantummanager` to install themes, switch themes, and configure transparent backgrounds, blur, and UI animations.
- **Dotfiles structure**: To back up Kvantum themes in a dotfiles repository, include the `~/.config/Kvantum/` directory. Themes are installed as folders within `~/.config/Kvantum/`.
- **Transparent Panels/Menus**: Kvantum allows the LXQt panel and menus to have blur and transparency if the Kvantum theme supports it. Make sure your compositor (e.g., Picom or Labwc) has blur enabled.

### Font Configuration

Consistent font rendering between Qt and GTK apps is a common challenge on LXQt. Here's how to unify it:

- **LXQt font settings**: `lxqt-config` → "Appearance" → "Fonts" to set the default font, monospace font, and DPI globally for Qt apps.
- **Fontconfig** (`~/.config/fontconfig/fonts.conf`): Controls font rendering system-wide for both Qt and GTK applications. Key settings:
  ```xml
  <?xml version="1.0"?>
  <!DOCTYPE fontconfig SYSTEM "fonts.dtd">
  <fontconfig>
    <match target="font">
      <edit name="antialias" mode="assign"><bool>true</bool></edit>
      <edit name="hinting" mode="assign"><bool>true</bool></edit>
      <edit name="hintstyle" mode="assign"><const>hintslight</const></edit>
      <edit name="rgba" mode="assign"><const>rgb</const></edit>
      <edit name="lcdfilter" mode="assign"><const>lcddefault</const></edit>
    </match>
    <!-- Preferred serif, sans-serif, and monospace fonts -->
    <alias>
      <family>serif</family><prefer><family>Noto Serif</family></prefer>
    </alias>
    <alias>
      <family>sans-serif</family><prefer><family>Noto Sans</family></prefer>
    </alias>
    <alias>
      <family>monospace</family><prefer><family>JetBrains Mono</family></prefer>
    </alias>
  </fontconfig>
  ```
- **Qt font DPI override**: Set `QT_FONT_DPI=96` in `session.conf` or shell profile to fix too-large/too-small fonts on HiDPI or mismatched displays.
- **Nerd Fonts**: [Nerd Fonts](https://www.nerdfonts.com/) patches popular programming fonts with glyphs for powerline, devicons, and status bars. Install via your package manager or download from the project site. Apply in terminal emulator settings.
- **Font diagnostic commands**:
  - `fc-list | grep <name>` — list installed fonts matching a pattern.
  - `fc-match <family>` — show which font file will be used for a given family.
  - `fc-cache -fv` — rebuild fontconfig cache after installing new fonts.
- **CJK & emoji fallback**: Ensure fallback fonts are configured for Chinese/Japanese/Korean characters and emoji:
  ```xml
  <alias>
    <family>sans-serif</family>
    <prefer>
      <family>Noto Sans CJK SC</family>
      <family>Noto Color Emoji</family>
    </prefer>
  </alias>
  ```
- **GTK font sync**: Set the same font family and size in `~/.config/gtk-3.0/settings.ini`:
  ```ini
  [Settings]
  gtk-font-name=Noto Sans 10
  gtk-monospace-font-name=JetBrains Mono 10
  ```

### Cursor Configuration

Cursor sizing and theming is a frequent pain point when mixing X11 and Wayland on LXQt:

- **Environment variables** (set in `session.conf`, `~/.profile`, or `~/.config/environment.d/*.conf`):
  - `XCURSOR_THEME=Bibata-Modern-Classic` — set cursor theme.
  - `XCURSOR_SIZE=24` — set cursor size (common values: 24, 32, 48 for HiDPI).
  - `XCURSOR_PATH=/usr/share/icons:~/.local/share/icons:~/.icons` — where to look for cursor themes.
- **LXQt GUI setting**: `lxqt-config` → "Appearance" → "Cursor Theme" — sets the cursor theme for Qt apps.
- **System-wide default** (`~/.icons/default/index.theme`):
  ```ini
  [Icon Theme]
  Inherits=Bibata-Modern-Classic
  ```
- **GTK cursor sync** (`~/.config/gtk-3.0/settings.ini`):
  ```ini
  [Settings]
  gtk-cursor-theme-name=Bibata-Modern-Classic
  gtk-cursor-theme-size=24
  ```
- **Wayland considerations**: On Wayland, cursor size is set per-compositor:
  - Labwc: `<core><cursor><theme>Bibata-Modern-Classic</theme><size>24</size></cursor></core>` in `rc.xml`.
  - Hyprland: `env = XCURSOR_SIZE,24` and `env = XCURSOR_THEME,Bibata-Modern-Classic` in `hyprland.conf`.
  - Sway: `seat * xcursor_theme Bibata-Modern-Classic 24` in `config`.
  - KWin: Configure via System Settings → Cursors.
- **Cursor themes**: See [Themes & Customization](#themes--customization) for popular cursor packs (Bibata, Capitaine).

### Shell Configuration

LXQt-relevant environment variables and aliases to set in your shell profile (`~/.bashrc`, `~/.zshrc`, `~/.config/fish/config.fish`):

```bash
# Default applications for LXQt
export EDITOR=nvim
export BROWSER=falkon
export TERMINAL=qterminal
export FILE_MANAGER=pcmanfm-qt

# Qt theming
export QT_QPA_PLATFORMTHEME=qt5ct     # or "lxqt" for native LXQt theming
export QT_STYLE_OVERRIDE=kvantum      # force Kvantum style
export QT_AUTO_SCREEN_SCALE_FACTOR=1  # HiDPI per-monitor scaling
export QT_FONT_DPI=96                 # force font DPI if needed

# Wayland-specific overrides (set only when on Wayland)
if [ "$XDG_SESSION_TYPE" = "wayland" ]; then
  export QT_QPA_PLATFORM=wayland
  export GDK_BACKEND=wayland
  export SDL_VIDEODRIVER=wayland
  export CLUTTER_BACKEND=wayland
  export _JAVA_AWT_WM_NONREPARENTING=1
fi

# Useful aliases
alias lock='lxqt-leave --lock'
alias logout='lxqt-leave --logout'
alias shutdown='lxqt-leave --shutdown'
alias reboot='lxqt-leave --reboot'
alias suspend='lxqt-leave --suspend'
alias dropdown='qterminal --drop-down'
alias panel-restart='killall lxqt-panel && lxqt-panel &'
alias lxqt-edit='$EDITOR ~/.config/lxqt/'
alias qt-style='QT_STYLE_OVERRIDE=fusion QT_QPA_PLATFORMTHEME=qt5ct'
```

- **Where to set env vars**: `~/.profile` (login shell, all sessions) vs `~/.bashrc`/`~/.zshrc` (interactive shells) vs `lxqt-session.conf[Environment]` (LXQt session only). Prefer `session.conf` for LXQt-specific settings and `~/.profile` for system-wide defaults.
- **Shell aliases for LXQt**: Add common LXQt commands as shell aliases for faster access (as shown above).
- **`command-not-found` hooks**: Install `pkgfile` (Arch) or `command-not-found` (Debian) for intelligent suggestions when a command is missing.

### Xresources / Xdefaults (X11)

On X11 sessions, `~/.Xresources` configures terminal emulators, system colors, and X11 application defaults:

```
! Load with: xrdb -merge ~/.Xresources
! (add to Openbox autostart or LXQt session autostart)

! Xft font rendering
Xft.dpi: 96
Xft.antialias: 1
Xft.hinting: 1
Xft.hintstyle: hintslight
Xft.rgba: rgb
Xft.lcdfilter: lcddefault

! Cursor
Xcursor.theme: Bibata-Modern-Classic
Xcursor.size: 24

! Color scheme (example: Catppuccin Mocha)
*background: #1e1e2e
*foreground: #cdd6f4
! Black
*color0: #45475a
*color8: #585b70
! Red
*color1: #f38ba8
*color9: #f38ba8
! Green
*color2: #a6e3a1
*color10: #a6e3a1
! Yellow
*color3: #f9e2af
*color11: #f9e2af
! Blue
*color4: #89b4fa
*color12: #89b4fa
! Magenta
*color5: #f5c2e7
*color13: #f5c2e7
! Cyan
*color6: #94e2d5
*color14: #94e2d5
! White
*color7: #bac2de
*color15: #a6adc8

! rofi
rofi.font: JetBrains Mono 12
rofi.colorscheme: Catppuccin-Mocha

! URxvt (if used)
URxvt.font: xft:JetBrains Mono:size=11
URxvt.scrollBar: false
```

To load Xresources automatically in LXQt, add this to your Openbox `autostart` or as an LXQt autostart `.desktop` file:

```bash
[ -f ~/.Xresources ] && xrdb -merge ~/.Xresources
```

### Wayland environment.d Configuration

On Wayland, systemd's `environment.d` mechanism is the standard way to set environment variables before the session starts. LXQt 2.0+ benefits from these:

**`~/.config/environment.d/lxqt-wayland.conf`**:

```ini
# Qt Wayland platform
QT_QPA_PLATFORM=wayland
QT_QPA_PLATFORMTHEME=lxqt
QT_STYLE_OVERRIDE=kvantum
QT_AUTO_SCREEN_SCALE_FACTOR=1

# GTK Wayland backend
GDK_BACKEND=wayland

# SDL2 Wayland
SDL_VIDEODRIVER=wayland

# Java non-reparenting (fixes Java apps on Wayland)
_JAVA_AWT_WM_NONREPARENTING=1

# Qt screen locker delay (avoid race condition on lock)
QT_LOCK_SCREEN_DELAY=500

# PipeWire/Wayland
PIPEWIRE_LATENCY=256/48000
```

- **How it works**: `pam_systemd` reads `~/.config/environment.d/*.conf` and `~/.config/environment.d/*.conf` and exports the variables into the user's D-Bus environment before the desktop session starts.
- **Priorities**: Variables set in `environment.d` override those in `~/.profile` but can be overridden by `lxqt-session.conf`.
- **Reloading**: After editing, either reboot or run `systemctl --user import-environment` to apply changes to the current session.

### Performance Tuning & Optimization

LXQt is known for being lightweight, but you can push it further:

- **Disable unnecessary LXQt services**: In `~/.config/lxqt/session.conf`, comment out or remove components you don't need:
  ```ini
  [Environment]
  # environment=...
  ```
  To disable the notification daemon: `killall lxqt-notificationd` and use a lightweight alternative (see [Notification Daemons](#notification-daemons)).
- **Disable desktop icon management**: Open `pcmanfm-qt` → Preferences → uncheck "Manage the desktop". This saves ~20-40MB RAM and reduces CPU usage on both X11 and Wayland.
- **Reduce panel plugins**: Every panel plugin consumes resources. Keep only what you use (clock, taskbar, tray). Remove monitors, sensors, and fancy menu if not needed.
- **Lightweight compositor choice**:
  - X11: Use `xcompmgr` instead of `picom` on very old hardware (no blur but minimal overhead).
  - Wayland: Labwc has no built-in compositing effects — the most lightweight option. Sway with `swayfx` adds overhead.
- **Disable compositing entirely** (X11): Run Openbox without any compositor. No shadows, transparency, or fading — but maximum performance.
- **Reduce startup applications**: Audit `~/.config/autostart/` and `~/.config/lxqt/session.conf` for unnecessary autostarts. Every autostart adds to boot time.
- **Kernel parameters for desktop responsiveness**:
  ```bash
  # Add to /etc/sysctl.d/99-desktop.conf
  vm.swappiness=10          # reduce swapping
  vm.vfs_cache_pressure=50  # keep inode/dentry cache longer
  kernel.nmi_watchdog=0     # disable NMI watchdog on battery
  ```
- **Profile LXQt startup**: Use `systemd-analyze blame` (systemd distros) and `lxqt-session` logging to find bottlenecks:
  ```bash
  systemd-analyze blame | head -20
  ```
- **Reduce animation/effects**: Use a plain Qt style (Fusion) instead of Kvantum. Disable animations in Kvantum and compositor fade effects.

### Multi-Monitor Setup

LXQt's multi-monitor support has some quirks worth documenting:

- **Monitor configuration GUI**: `lxqt-config` → "Monitor Settings" (part of `lxqt-config`). Set resolution, refresh rate, position, and primary display.
- **XRandR (X11)**: Scriptable monitor management:
  ```bash
  xrandr --output HDMI-1 --primary --mode 1920x1080 --rate 144 --right-of eDP-1
  xrandr --output eDP-1 --mode 1920x1080 --rate 60
  ```
- **wlr-randr (Wayland)**: Equivalent for wlroots compositors:
  ```bash
  wlr-randr --output HDMI-A-1 --mode 1920x1080 --pos 1920,0
  wlr-randr --output eDP-1 --mode 1920x1080 --pos 0,0
  ```
- **Hotplug automation**: Use `autorandr` (X11) or `kanshi` (Wayland) to automatically apply monitor profiles when displays are connected/disconnected:
  - `autorandr --save work` — save current layout.
  - `kanshi` — run in background, reads `~/.config/kanshi/config`.
- **Manual panel per monitor**: LXQt panel does not natively support different configs per monitor. Workaround: launch multiple panel instances:
  ```bash
  lxqt-panel --config ~/.config/lxqt/panel-primary.conf &
  lxqt-panel --config ~/.config/lxqt/panel-secondary.conf &
  ```
- **Wallpaper per monitor**:
  - X11: `nitrogen --set-scaled --head=0 ~/wallpapers/left.jpg && nitrogen --set-scaled --head=1 ~/wallpapers/right.jpg`
  - Wayland: `swaybg -o eDP-1 -i ~/wallpapers/main.jpg -o HDMI-A-1 -i ~/wallpapers/second.jpg`
- **Taskbar behavior**: LXQt's task manager shows windows from all monitors by default. To limit per-monitor, use alternative bars (see [Alternative Panels & Bars](#alternative-panels--bars)) or configure individual task manager plugins per panel instance.

### Backup & Restore

Essential LXQt configuration files to back up before experimenting:

```bash
# Quick backup command
tar -czf lxqt-backup-$(date +%Y%m%d).tar.gz \
  ~/.config/lxqt \
  ~/.config/openbox \
  ~/.config/labwc \
  ~/.config/picom \
  ~/.config/picom.conf \
  ~/.config/qt5ct \
  ~/.config/qt6ct \
  ~/.config/Kvantum \
  ~/.config/fontconfig \
  ~/.config/gtk-3.0 \
  ~/.config/gtk-4.0 \
  ~/.Xresources \
  ~/.config/environment.d \
  ~/.config/systemd/user/lxqt* \
  ~/.local/share/lxqt
```

- **What to back up**: The `~/.config/lxqt/` directory is the most critical. Also back up your WM config (`openbox`, `labwc`), compositor config (`picom`), Qt settings (`qt5ct`, `qt6ct`), Kvantum themes, fontconfig, GTK settings, and any custom env files.
- **What can be regenerated**: `~/.cache/lxqt/`, `~/.local/share/lxqt/` (recent files, session cache) — safe to skip.
- **Restore**: Simply extract the backup and restart the LXQt session (log out and back in).
- **Migration between machines**: Dotfile managers ([GNU Stow](#dotfile-management), [Chezmoi](#dotfile-management)) work well for porting LXQt config. Note that LXQt 1.x (Qt5) and LXQt 2.0 (Qt6) config files are NOT interchangeable — migrate by reinstalling and reconfiguring.

### Compositors (X11)

- **[Picom](https://github.com/yshui/picom)** - The de-facto X11 compositor for ricing. Animations, blur, rounded corners, fading. Configuration example:
  ```ini
  # ~/.config/picom/picom.conf
  blur-background = true;
  blur-method = "kawase";
  blur-strength = 7;
  fading = true;
  fade-delta = 4;
  shadow = true;
  shadow-radius = 12;
  corner-radius = 8;
  round-borders = 1;
  ```
- **[xcompmgr](https://gitlab.freedesktop.org/xorg/app/xcompmgr)** - Minimal X compositor. Limited but uses very few resources.

### Managing Theme Assets

When building a dotfiles repository, you'll need to handle visual assets properly alongside your config files:

- **Icons and Cursors**: Store these in `~/.icons/` or `~/.local/share/icons/`. In your dotfiles manager (like Stow), map a directory to populate these folders so your `lxqt-config-appearance` picks them up automatically.
- **GTK Themes**: Store them in `~/.themes/` or `~/.local/share/themes/`.
- **Fonts**: Place custom fonts in `~/.local/share/fonts/`. After syncing your dotfiles on a new machine, remember to run `fc-cache -fv` to refresh the font cache.

### Dotfile Management

- **[GNU Stow](https://www.gnu.org/software/stow/)** - A symlink farm manager; makes dotfiles appear installed in the same place. Common layout:
  ```
  ~/dotfiles/
    lxqt/.config/lxqt/
    openbox/.config/openbox/
    picom/.config/picom/
  ```
  Deploy with: `stow -t ~ lxqt openbox picom`
- **[Chezmoi](https://www.chezmoi.io/)** - Manage dotfiles securely across multiple machines. Supports templates for machine-specific config values.
- **[YADM](https://yadm.io/)** - Yet Another Dotfiles Manager; wraps Git with additional features like bootstrap and alternate files.
- **[Nix](https://nixos.org/)** - Nix package manager can manage entire system and home configurations declaratively.
- **[Home Manager](https://github.com/nix-community/home-manager)** - Manage user environment with Nix; supports LXQt module (`programs.lxqt.enable = true;`).
- **[dotdrop](https://github.com/deadc0de6/dotdrop)** - A dotfile manager with template support, encryption, and per-profile configurations.
- **[vcsh](https://github.com/RichiH/vcsh)** - Manage multiple dotfile repositories with separate Git repositories in a single `$HOME`.

### Community Rices & Dotfile Repos

Real-world LXQt configurations to inspire your own setup:

- **Curated LXQt Dotfiles**:
  - **[gh0stzk/dotfiles](https://github.com/gh0stzk/dotfiles)** - Extensive rice collections, many of which can be adapted to LXQt / Openbox setups.
  - **[owl4ce/dotfiles](https://github.com/owl4ce/dotfiles)** - Famous Openbox dotfiles with beautiful Qt/GTK integration that easily ports to LXQt.
  - **[Murzchnvok/dotfiles](https://github.com/Murzchnvok/dotfiles)** - A great example of a modern, script-driven Openbox and LXQt environment.
  - **[dracula/lxqt](https://github.com/dracula/lxqt)** - The official Dracula theme dotfiles and assets for LXQt.
- **[r/unixporn LXQt tag](https://www.reddit.com/r/unixporn/search/?q=LXQt&restrict_sr=1&sort=top)** - The best source of LXQt rice screenshots and dotfile links.
- **[Lubuntu Rices](https://www.reddit.com/r/Lubuntu/)** - Community rices specific to Lubuntu installations.
- **Discover More**:
  - Browse `github.com/topics/lxqt-dotfiles`
  - UnixPorn Discord `#ricing` channels.

### LXQt-Specific Ricing Tips

- **LXQt config directory**: `~/.config/lxqt/` — back up this entire directory before experimenting.
- **Openbox config**: `~/.config/openbox/` — also used by Labwc on Wayland (themes and `rc.xml`).
- **Qt style override**: Set `QT_STYLE_OVERRIDE=kvantum` or `QT_STYLE_OVERRIDE=breeze` to force a style regardless of the desktop theme.
- **HiDPI scaling**:
  - `QT_AUTO_SCREEN_SCALE_FACTOR=1` — per-screen automatic scaling.
  - `QT_SCALE_FACTOR=1.5` — uniform manual scaling.
  - `GDK_SCALE=2` — GTK scaling to match.
- **Wayland environment variables**:
  - `QT_QPA_PLATFORM=wayland` — force Qt apps to use Wayland (required on native Wayland sessions).
  - `WAYLAND_DISPLAY=wayland-1` — which Wayland socket to use.
- **Disable pcmanfm-qt desktop icons** for a cleaner look: Open `pcmanfm-qt` → Preferences → uncheck "Manage the desktop".
- **Transparent panels**: In Kvantum, create a panel-specific transparent theme. Or set panel opacity via composition (Picom rules for X11, or compositor window rules for Wayland).
- **Picom panel transparency rule for LXQt panel**:
  ```ini
  # In picom.conf
  opacity-rule = [
    "90:class_g = 'lxqt-panel'"
  ];
  ```
- **Blur under LXQt panel** (Picom on X11):
  ```ini
  blur-background-exclude = [
    "class_g = 'lxqt-panel'"
  ];
  blur-background = true;
  ```
- **Screenshots without pcmanfm-qt**: If you disable desktop management, use `nitrogen` (X11) or `swaybg`/`swww`/`hyprpaper` (Wayland) for wallpaper.
- **LXQt leave dialog**: `lxqt-leave` supports `--logout`, `--shutdown`, `--reboot`, `--suspend`, `--hibernate`. Bind these to keyboard shortcuts or WM menus.
- **Multiple LXQt panels**: Run several panels with different configs. Use `lxqt-panel --config ~/.config/lxqt/panel2.conf`.
- **Restart the panel without logout**: `killall lxqt-panel && lxqt-panel &`
- **Tmux-like terminal in LXQt**: Bind a shortcut to `qterminal --drop-down` for a Quake-style drop-down terminal.
- **Per-monitor wallpaper**: Use `nitrogen --set-scaled --random ~/wallpapers/ --head=0 --save` and repeat for each monitor (X11). On Wayland, `swaybg` supports `-o <output>` for per-monitor backgrounds.

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
