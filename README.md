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
