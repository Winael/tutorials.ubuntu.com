---
id: tutorial-install-ubuntu-server-fr
summary: Transformez votre PC en un serveur puissant, capable de fournir n'importe quoi, du partage de fichiers et sauvegardes locales jusqu'à des sites Web  complets et même au-delà.
categories: server
language: fr
tags: tutorial,installation,ubuntu,server,Ubuntu 16.04 LTS
difficulty: 2
status: Published
translator: Winael
published: 2017-10-31

---

# Install Ubuntu Server

## Vue d'ensemble
Durée : 0:01

Positive
: Changer la langue : **FR** | [EN](tutorial-install-ubuntu-server)

Ubuntu Server est conçu sur mesure pour les réseaux et les services, et il est tout aussi capable de partager des fichiers sur votre réseau domestique qu'il fonctionne dans un cluster Hadoop.

Contrairement à l'installation d'Ubuntu Desktop, Ubuntu Server n'inclut pas de programme d'installation graphique. Il utilise à la place, un procédé basé sur le menu de la console. Si vous préférez installer la version de bureau, jetez un coup d'oeil à notre tutoriel [Installer Ubuntu desktop](https://tutorials.ubuntu.com/tutorial/tutorial-install-ubuntu-desktop).

Ce guide vous donnera un aperçu de l'installation à partir d'un DVD ou d'une clé USB, convenant à toute personne intéressée par l'exploitation de son propre serveur. Pour un guide plus détaillé sur les capacités d'Ubuntu Server et sa configuration, consultez notre [l'assistance documentaire d'Ubuntu Server](https://help.ubuntu.com/lts/serverguide/installation.html).

![screenshot](https://assets.ubuntu.com/v1/fcc62c28-server-welcome.png)

## Pré-requis
Durée : 0:01

Vous devez tenir compte des points suivants avant de commencer l'installation :

* Assurez-vous d'avoir au moins 2 Go d'espace de stockage disponible. 
* Avoir accès à un DVD ou une clé USB contenant la version d'Ubuntu Server que vous désirez installer.
* Si vous devez installer Ubuntu Server en parallèle avec les données que vous souhaitez conserver, assurez-vous d'en avoir une sauvegarde récente.

Voir [Installation/Pré-requis Système](https://help.ubuntu.com/community/Installation/SystemRequirements#Ubuntu_Server_.28CLI.29_Installation) pour plus de détails sur les configurations matérielles requises. Nous avons également [plusieurs tutoriels](/) qui expliquent comment créer un DVD ou une clé USB Ubuntu.


## Démarrage à partir du DVD
Durée : 0:02

Pour déclencher le processus d'installation, procédez comme suit :

1. Placez le DVD Ubuntu dans votre lecteur DVD.
2. Redémarrez votre ordinateur.

Quelques instants plus tard, un grand menu 'Langue' apparaît où la sélection de votre langue vous amènera au menu de démarrage.

![screenshot](https://assets.ubuntu.com/v1/87351452-server-language-select.png)

Si vous n'obtenez pas ce menu, lisez le [guide de démarrage à partir du DVD](https://help.ubuntu.com/community/BootFromCD?_ga=2.102380610.2115462233.1496186978-1155966827.1485186360) pour plus d'informations.

## Démarrage à partir d'une clé USB
Duration: 0:02

Most computers will boot from USB automatically. Simply insert the USB flash drive and either power on your computer or restart it. You should see the same language menu we saw in the previous 'Install from DVD' step, followed by the boot menu.

If your computer doesn't automatically boot from USB, try holding `F12` when your computer first starts. With most machines, this will allow you to select the USB device from a system-specific boot menu.

positive
: F12 is the most common key for bringing up your system's boot menu, but Escape, F10 and F2 are common alternatives. If you're unsure, look for a brief message when your system starts - this will often inform you of which key to press to bring up the boot menu.

## Boot options
Duration: 0:20

The Ubuntu Server boot menu includes handy options for testing your system and for testing the validity of the install media and system disks.

There are two options for installation, and you should select 'Install Ubuntu Server'. 

![screenshot](https://assets.ubuntu.com/v1/c08110df-server-boot-menu.png)

## Network configuration
Duration: 0:03

After selecting installation language, geographical location and keyboard layout, the installer will perform some background configuration and processing. In particular, the installer will attempt to automatically configure your network.

If the installer successfully detects your network configuration, you'll be asked to enter a hostname, which can either be modified or left as the default 'ubuntu'.

![screenshot](https://assets.ubuntu.com/v1/fc14d32b-server-network.png)

positive
: If network autodetection fails, this will mostly likely be because your network isn't using DHCP or the DHCP server isn't accessible. You will see another menu offering you the option to configure the network manually or rerun the autodetection routine. 

## User configuration
Duration: 0:03

After networking, you'll be asked to enter your full name, username and password. As you're configuring a server that's likely to be accessible from the internet (if you choose), make sure your password is strong and difficult to guess.

![screenshot](https://assets.ubuntu.com/v1/cfd45d64-server-password.png)

## Storage configuration
Duration: 0:05

After answering a question about your time zone, you need to configure local storage.

If the storage connected to your server is raw and unformatted, the installer will detect this and present a menu offering four options. The simplest is the second, 'Guided - use entire disk and set up LVM', and we'd recommend selecting this. 

Any of these options will obviously destroy any data currently on your partition(s), but resizing and creating new partitions are options available by selecting 'Manual'.

![screenshot](https://assets.ubuntu.com/v1/bde68a78-server-partition-auto.png)

positive
: If your server storage is already being used, or has been used prior to the installation, you will get a slightly different menu. Once again, the simplest option is to select 'Guided - use the entire disk and set up LVM', but you can also choose the specific partition if that's convenient.

## Package retrieval
Duration: 0:02

After accepting the changes that are going to be made to your storage, the installer will determine the packages to be installed. This will take a few moments.

You will then be asked to enter an HTTP proxy address. This can be ignored if you don't know whether you need one to access the internet from your server. You'll also be asked whether you require automatic updates. Selecting 'Install security updates automatically' is the safest default option. 

![screenshot](https://assets.ubuntu.com/v1/4f89d790-server-updates.png)

## Software selection
Duration: 0:01

The final step before installation starts requires you to select the software you want pre-installed on your server. You can select from a broad set of categories or manually choose the packages yourself. This option is purely for convenience, as you can easily install any additional software you need after installation has completed.

We'd recommend selecting 'standard system utilities' and 'OpenSSH server' as a minimum so that your system is both fully functional and accessible from any SSH client on your local network.

![screenshot](https://assets.ubuntu.com/v1/51cf4395-server-software.png)

## Installation 
Duration: 0:02

Ubuntu Server will now be installed. When complete, one final question asks for permission to install the GRUB boot loader. You should answer 'Yes'.

The installer will finish up by installing the final packages and configuration files. 

![screenshot](https://assets.ubuntu.com/v1/a8d32900-server-grub.png)

## Installation complete
Duration: 0:02

Congratulations! With the installation complete, you can now remove your installation media, restart your machine and begin enjoying Ubuntu Server.

If you're looking for a place to start with your new server, we'd recommend reading the [Server Guide](https://help.ubuntu.com/lts/serverguide/).

Alternatively, alongside its vast array of industry defining applications and services, use your fresh installation to take a look at some of [Canonical's](https://www.canonical.com/) most advanced technologies:

- [MAAS](https://maas.io/) - Metal as a Service, offers complete automation of your physical servers for amazing data centre operational efficiency.

- [Landscape](https://landscape.canonical.com/landscape-features), our cost-effective way to support and monitor large and growing networks of desktops, servers and clouds.

![screenshot](https://assets.ubuntu.com/v1/dbd27849-server-complete.png)

## Finding help
Duration: 0:02

The Ubuntu community, for both desktop and server, is one of the friendliest and most well populated you can find. That means if you get stuck, someone has most likely already been there and solved the same problem.

Try asking for help in one of the following:

* [Ask Ubuntu](https://askubuntu.com/)
* [Ubuntu Forums](https://ubuntuforums.org/)
* [IRC-based support](https://wiki.ubuntu.com/IRC/ChannelList)

Alternatively, if you need commercial support for your server deployments, take a look at [Ubuntu Advantage](https://www.ubuntu.com/support).
