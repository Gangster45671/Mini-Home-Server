# Mini Home Server
The *Mini Home Server* is designed to be an all-purpose home server. With a hard-drive and a Orange Pi it can do a variety of tasks such as;
* File Serving / NAS
* Web Serving / Website
* Media Center / MediaBox
* ...

 Inspired by the [NODE Mini Server](https://www.youtube.com/watch?v=2NAGp-nRsX4)
 and the [NODE Pi Plug](https://www.youtube.com/watch?v=a1p-kd6U_Qo).
 
Being so versatile, what you do with it is up to you! Please share your creations `@Luigi_Pizzolito`(Twitter) if you do attempt at making one!

---

## Table Of Contents
- [Mini Home Server](#mini-home-server)
    - [Table Of Contents](#table-of-contents)
    - [Progress / Plan / Engineer's Log](#progress--plan--engineers-log)
    - [Hardware](#hardware)
        - [Electronics](#electronics)
            - [Components](#components)
                - [Orange Pi Lite](#orange-pi-lite)
                - [Hard Drive](#hard-drive)
                - [Power Supply](#power-supply)
            - [BOM (Bill Of Materials)](#bom-bill-of-materials)
            - [Wiring](#wiring)
        - [Enclosure](#enclosure)
            - [Design](#design)
            - [Assembly](#assembly)
    - [Software](#software)
        - [Remote Login / VNC / SSH (Headless Operation)](#remote-login--vnc--ssh-headless-operation)
        - [Web Server](#web-server)
            - [Apache, Nginx, MySQL, PHP](#apache-nginx-mysql-php)
            - [Cronjobs](#cronjobs)
        - [File Server (NAS)](#file-server-nas)
            - [Samba](#samba)
            - [FTP / SFTP / SCP / RSync / SSHFS](#ftp--sftp--scp--rsync--sshfs)
            - [Backup Server](#backup-server)
        - [Media Center](#media-center)
            - [Downloads Center](#downloads-center)
            - [Media Streamer](#media-streamer)
        - [IOT Server](#iot-server)
            - [Node.js](#nodejs)
            - [Bots](#bots)
                - [Twitter](#twitter)
                - [Discord](#discord)
            - [IOT Device Database](#iot-device-database)
        - [Gaming Console](#gaming-console)
                    - [MarkDown CheatSheet](#markdown-cheatsheet)

---

## Progress / Plan / Engineer's Log
- [ ] Planning
    - [X] Plan Software
    - [ ] Plan Hardware
- [ ] Aquire Resources
- [ ] Setup Software
    - [ ] Remote Access
        - [ ] CLI
        - [ ] GUI
        - [ ] Startup
    - [ ] File Server
        - [ ] Samba
        - [ ] SFTP / SSH(RSync)
        - [ ] Backups
        - [ ] *Startup / Cronjobs*
    - [ ] Web Server
        - [ ] LAMP Stack
        - [ ] Startup Cronjobs
    - [ ] Media Center
        - [ ] Downloads
        - [ ] Stream
        - [ ] *Startup / Cronjobs*
    - [ ] IOT Server
        - [ ] Node.js
        - [ ] Bots
        - [ ] IOT Database
        - [ ] *Startup / Cronjobs*
    - [ ] Gaming Console
- [ ] Build Hardware
    - [ ] Electronics
    - [ ] 3D Printing
- [ ] Document Project
    - [ ] ReadMe.md / GitHub
        - [ ] Text
        - [ ] Media
        - [ ] Links
    - [ ] Instructables
        - [ ] Text (Extract from ReadMe.md)
        - [ ] Media
    - [ ] Video Guide
        - [ ] Footage
        - [ ] Editing

---

## Hardware
The hardware for this projects consists of an Orange Pi Lite, a 3.5" hard-drive and a 5V power supply, snuggly fit into a 3D printed enclosure.
### Electronics
 #### Components
  ##### Orange Pi Lite
  The [Orange Pi Lite](http://www.orangepi.org/orangepilite/) is a powerfull yet cheap SBC(Single Board Computer) that will server as the brains of our *Mini Home Server*. It's specs are listed below:
  Feature | Specification
  --- | ---
  Price | $12
  Dimensions | 69mm x 48mm
  Weight | 36g
  Power | Barrel jack (5V 2A)
  CPU | H3 (Cortex-A7) Quad-Core 1.2GHz
  GPU | Mali400MP2 600MHz (OpenGL)
  RAM | 512MB DDR3
  WiFi | Built-In External Antenna
  SD Card | 32GB Maximum
  USB | 2x Vertical USB Hosts, 1x µUSB OTG
  Video | HDMI
  Audio | HDMI Out & Microphone
  GPIO | 40 Pin (Raspberry Pi Compatible)
  Extras | IR Reciever, CSI (Camera In), Power Button, Status Led, Power Led
  Operating Systems | Android 4.4, Ubuntu, Debian, Raspbian
  ##### Hard Drive
  The hard-drive is any 3.5" SATA hard-drive, I will be using a 3TB one.
  ##### Power Supply
 #### BOM (Bill Of Materials)
 Component | Price | Link
 --- | --- | ---
 Orange Pi Lite | CN¥94 | [TaoBao](https://item.taobao.com/item.htm?spm=a1z10.1-c.w4004-9552179465.10.6dab6cf1k6rwVL&id=531431687002)
 3.5" 3TB Hard Drive | CN¥330 | [TaoBao](https://item.taobao.com/item.htm?spm=2013.1.20141001.2.58541465k2YEez&id=562186167791&scm=1007.12144.81309.42296_42296&pvid=e5f8ccf4-7c13-43a8-918f-147740b71562&utparam=%7B%22x_object_type%22%3A%22item%22%2C%22x_hestia_source%22%3A%2242296%22%2C%22x_object_id%22%3A562186167791%7D&utparam=%7B%22x_object_type%22%3A%22item%22%2C%22x_hestia_source%22%3A%2242296%22%2C%22x_object_id%22%3A562186167791%7D)
 SATA to USB Adapter | CN¥9.90 | [TaoBao](https://item.taobao.com/item.htm?spm=a1z0d.6639537.1997196601.14.15e87484e8sE1w&id=36788516377)
 Power Supply | CN¥ | [TaoBao]()
 Total | CN¥ | 

---

 #### Wiring

### Enclosure
 #### Design
 #### Assembly

---

## Software
The Orange Pi Lite will be running Raspbian.
 - [RaspberryPi Linux Docs](https://www.raspberrypi.org/documentation/linux/)
 ### Remote Login / VNC / SSH (Headless Operation)
 - [RaspberryPi Remote AccessDocs](https://www.raspberrypi.org/documentation/remote-access/)
---
 ### Web Server
  #### Apache, Nginx, MySQL, PHP
-  [Video Tutorial by __TinkerNut__](https://www.youtube.com/watch?v=WgcNBjIJNYs)
-  On RaspberryPi Remote Access Docs.
  #### Cronjobs
  - [Raspberry Pi Cronjobs Docs](https://www.raspberrypi.org/documentation/linux/usage/cron.md)
---
 ### File Server (NAS)
   #### Samba
 [Video Tutorial by __Ksk Royal__](https://www.youtube.com/watch?v=EH6P6v3lxsE)
  #### FTP / SFTP / SCP / RSync / SSHFS
 - On RaspberryPi Remote Access Docs.
  #### Backup Server
  - Rsync from other computers
  - Local Backup on [RaspberryPi Backup Docs](https://www.raspberrypi.org/documentation/linux/filesystem/backup.md)
---
 ### Media Center
  #### Downloads Center
  - Sonarr
  - Radarr
  - SABnzbd
  - Jackett
  #### Media Streamer
  - Kodi
  - Using a Node.js server
---
 ### IOT Server
  #### Node.js
-   [Video Tutorial by __BureauForFreshness__](https://www.youtube.com/watch?v=J6g53Hm0rq4)
  #### Bots
   ##### Twitter
   ##### Discord
  #### IOT Device Database
  - Using LAMP Stack
---
 ### Gaming Console
 - [RetroArch](http://www.retroarch.com/)
 - [Lutris](https://lutris.net/)


---
###### [MarkDown CheatSheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)