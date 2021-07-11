## Guide d'installation complet pour Arch Linux avec en WM [AwesomeWM 4.3](https://awesomewm.org/)
### A l'origine de ces projets PapyElGringo, Chris Titus Tech, MAtmoul et bien d'autres.

Note: Ce guide fait office de pense-bête pour les débutants afin d'installer ou réinstaller Arch.

Le but de la manoeuvre est d'installer Arch via archfi, et ensuite avoir un simili environement de bureau avec [AwesomeWM](https://awesomewm.org/) avec la [norme graphique material](https://material.io) dans une volonté d'allier le confort de travail à l'esthétique.

[![](./theme/PapyElGringo-theme/demo.gif?raw=true)](https://www.reddit.com/r/unixporn/comments/anp51q/awesome_material_awesome_workflow/)
*[Cliquer pour voir en bonne qualité](https://www.reddit.com/r/unixporn/comments/anp51q/awesome_material_awesome_workflow/)*

| Tiled         | Panel         | Exit screen   |
|:-------------:|:-------------:|:-------------:|
|![](https://i.imgur.com/fELCtep.png)|![](https://i.imgur.com/7IthpQS.png)|![](https://i.imgur.com/rcKOLYQ.png)|


## I) Installation avec le script archfi

### 1) Lancement du script Archfi

| Lancer la clé | Lancer Arch   | tty1   |
|:-------------:|:-------------:|:-------------:|
|![](https://i.vgy.me/trAsRK.png)|![](https://i.vgy.me/xb5izX.png)|![](https://i.vgy.me/QlzrmF.png)|


##### Après le boot sur la clé avec Arch en EFI

```
curl -LO archfi.sf.net/archfi
sh archfi
```

### 2) Choix de la langue et du clavier

| Menu de  base | Langue        | Retour au menu       | Clavier       |
|:-------------:|:-------------:|:--------------------:|:-------------:|
|![](https://i.vgy.me/akWuSX.png)|![](https://i.vgy.me/w4d9Gv.png)|![](https://i.vgy.me/ds0d9H.png)|![](https://i.vgy.me/Ce7DUL.png)

### 3) Gestion des partitions disque

#### a) Partitionner le disque

| Menu de  base | Choisir SDA        | Confirmer       | Retour au menu      |
|:-------------:|:------------------:|:---------------:|:-------------------:|
|![](https://i.vgy.me/BBGsjK.png)|![](https://i.vgy.me/JvFjr9.png)|![](https://i.vgy.me/QezmTx.png)|![](https://i.vgy.me/n1ZjjC.png)

#### b) Selectionner les partitions d'installation

| Menu de  base | Boot          | Swap       |
|:-------------:|:-------------:|:----------:|
|![](https://i.vgy.me/uVBBxV.png)|![](https://i.vgy.me/ifB8mK.png)|![](https://i.vgy.me/XvZphn.png)|![](https://i.vgy.me/tuUDGk.png)

| Root      | Home      | Confirmer |
|:---------:|:---------:|:---------:|
|![](https://i.vgy.me/tuUDGk.png)|![](https://i.vgy.me/CfYEaQ.png)|![](https://i.vgy.me/NKcAlN.png)

#### c) Formater et monter les partitions

| Menu de  base | Confirmer          | Boot = FAT32 (EFI) |
|:-------------:|:------------------:|:------------------:|
|![](https://i.vgy.me/yDyLa4.png)|![](https://i.vgy.me/wG3dqX.png)|![](https://i.vgy.me/5OU7JT.png)

| Swap = Swap   | Root = btrfs       | Monter les partitions |
|:-------------:|:------------------:|:---------------------:|
|![](https://i.vgy.me/42ZHTY.png)|![](https://i.vgy.me/QL6QZW.png)|![](https://i.vgy.me/zDe03H.png)

### 4) Installer Archlinux pacstrap

| Menu de  base | Noyau =  linux-lts | Firmwares       | Système de fichiers |
|:-------------:|:------------------:|:---------------:|:-------------------:|
|![](https://i.vgy.me/93K8at.png)|![](https://i.vgy.me/ottSLt.png)|![](https://i.vgy.me/LS755B.png)|![](https://i.vgy.me/JcPGpu.png)

### 5) Configurer Archlinux

#### a) Définir le nom de l'ordinateur

| Configurer    | Menu de  base      | Choisir le nom du pc |
|:-------------:|:------------------:|:--------------------:|
|![](https://i.vgy.me/jrwPWO.png)|![](https://i.vgy.me/2XWJaU.png)|![](https://i.vgy.me/xW6nqN.png)

#### b) Disposition clavier

| Menu de  base | Choix clavier      |
|:-------------:|:------------------:|
|![](https://i.vgy.me/TJGTHd.png)|![](https://i.vgy.me/d4n2NA.png)

#### c) Définir locale

| Menu de  base | Choix localité     |
|:-------------:|:------------------:|
|![](https://i.vgy.me/FvdefQ.png)|![](https://i.vgy.me/jLXOLk.png)

#### d) Définir l'horloge

| Menu de  base | Région             | Ville      | Horloge matériel |
|:-------------:|:------------------:|:----------:|:-------------------:|
|![](https://i.vgy.me/EwXKmo.png)|![](https://i.vgy.me/JqCdEK.png)|![](https://i.vgy.me/BEU4wx.png)|![](https://i.vgy.me/wdv55g.pngg)

#### e) Définir le mot de passe root

| Menu de  base | Choix du pwd     |
|:-------------:|:------------------:|
|![](https://i.vgy.me/tZP29t.png)|![](https://i.vgy.me/NY1hoU.png)

#### f) Générer fstab

| Menu de  base | fstab -U     |
|:-------------:|:------------------:|
|![](https://i.vgy.me/2Y5Vnq.png)|![](https://i.vgy.me/uctxpr.png)

#### g) Bootloader

#### h) Extras

#### i) archdi

#### Arch-Based

```
yay -S awesome rofi picom i3lock-fancy xclip ttf-roboto gnome-polkit materia-gtk-theme lxappearance flameshot pnmixer network-manager-applet xfce4-power-manager -y
wget -qO- https://git.io/papirus-icon-theme-install | sh
```

#### Program list

- [AwesomeWM](https://awesomewm.org/) as the window manager - universal package install: awesome
- [Roboto](https://fonts.google.com/specimen/Roboto) as the **font** - Debian: fonts-roboto Arch: ttf-roboto
- [Rofi](https://github.com/DaveDavenport/rofi) for the app launcher - universal install: rofi
- [picom](https://github.com/yshui/picom) for the compositor (blur and animations) universal install: picom - Debian users need PPA (`sudo add-apt-repository ppa:regolith-linux/unstable`)
- [i3lock](https://github.com/meskarune/i3lock-fancy) the lockscreen application universal install: i3lock-fancy
- [xclip](https://github.com/astrand/xclip) for copying screenshots to clipboard package: xclip
- [gnome-polkit] recommend using the gnome-polkit as it integrates nicely for elevating programs that need root access
- [Materia](https://github.com/nana-4/materia-theme) as GTK theme - Arch Install: materia-theme debian: materia-gtk-theme
- [Papirus Dark](https://github.com/PapirusDevelopmentTeam/papirus-icon-theme) as icon theme Universal Install: wget -qO- https://git.io/papirus-icon-theme-install | sh
- [lxappearance](https://sourceforge.net/projects/lxde/files/LXAppearance/) to set up the gtk and icon theme
- (Laptop) [xbacklight](https://www.x.org/archive/X11R7.5/doc/man/man1/xbacklight.1.html) for adjusting brightness on laptops (disabled by default)
- [flameshot](https://flameshot.js.org/#/) my personal screenshot utility of choice, can be replaced by whichever you want, just remember to edit the apps.lua file
- [pnmixer](https://github.com/nicklan/pnmixer) Audio Tray icon that is in debian repositories and is easily installed on arch through AUR.
- [network-manager-applet](https://gitlab.gnome.org/GNOME/network-manager-applet) nm-applet is a Network Manager Tray display from GNOME.
- [xfce4-power-manager](https://docs.xfce.org/xfce/xfce4-power-manager/start) XFCE4's power manager is excellent and a great way of dealing with sleep, monitor timeout, and other power management features.

### 2) Clone the configuration

```
git clone https://github.com/ChrisTitusTech/material-awesome.git ~/.config/awesome
```

### 3) Set the themes

Start `lxappearance` to active the **icon** theme and **GTK** theme
Note: for cursor theme, edit `~/.icons/default/index.theme` and `~/.config/gtk3-0/settings.ini`, for the change to also show up in applications run as root, copy the 2 files over to their respective place in `/root`.

### 4) Same theme for Qt/KDE applications and GTK applications, and fix missing indicators

First install `qt5-style-plugins` (debian) | `qt5-styleplugins` (arch) and add this to the bottom of your `/etc/environment`

```bash
XDG_CURRENT_DESKTOP=Unity
QT_QPA_PLATFORMTHEME=gtk2
```

The first variable fixes most indicators (especially electron based ones!), the second tells Qt and KDE applications to use your gtk2 theme set through lxappearance.

### 5) Read the documentation

The documentation live within the source code.

The project is split in functional directories and in each of them there is a readme where you can get additional information about the them.

* [Configuration](./configuration) is about all the **settings** available
* [Layout](./layout) hold the **disposition** of all the widgets
* [Module](./module) contain all the **features** available
* [Theme](./theme) hold all the **aesthetic** aspects
* [Widget](./widget) contain all the **widgets** available
