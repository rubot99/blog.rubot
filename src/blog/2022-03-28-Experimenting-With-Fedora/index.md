---
title: "Experimenting with Fedora"
description: "Summary or brief description of the post to be displayed"
date: 2022-03-28
tags: 
    - linux
    - fedora
    - wifi
    - broadcom
---

So I've decided to try and restart my Linux learning. So far I've tried using Debian, Ubuntu, or arch based Linux distros. I've normally gravitated towards Ubuntu based distro that used XFCE. Normally because I've found a lot of help when trying to set up Wi-Fi cards. Recently I saw some YouTube videos reviewing Fedora 35. I've never really used Fedora, so thought I would be give it a try. So this hopefully will be the start of my journey experimenting with Fedora

{% image "./Logo_fedoralogo.png", "Fedora" %}

Let me start by saying I've tried quite distros based on Debian, Ubuntu and arch. I've tried a vanilla arch installation. I enjoyed the learning process, but this means I saw a couple of old / low spec laptops. So I decided to try and install Fedora on one of these laptops. I needed to get Fedora and Wi-Fi running plus it needed to be useable and not too slow. The machine I picked was the HP Stream book (pictured below). The laptop has an Intel Celeron processor, 2 GB RAM and 32 GB MMC drive.

{% image "./hpStream.jpg", "HP Stream 11" %}

I managed to install Fedora without a problem and after the first reboot the laptop seemed quite response. The Wi-Fi adapter wasn't working out of the box since the machine had a Broadcom adapter. After a bit of googling and trying a few things I managed to get the Wi-Fi working. So next steps are to learn how to use Fedora and get used to it as a system. Below are the steps I used to get the Wi-Fi driver working. 

* Update system - sudo dnf update
* Add rpmfusion repositories - sudo dnf install https://download1.rpmfusion.org/free/fedora/rpmfusion-free-release-$(rpm -E %fedora).noarch.rpm https://download1.rpmfusion.org/nonfree/fedora/rpmfusion-nonfree-release-$(rpm -E %fedora).noarch.rpm
* Install drivers - sudo dnf install kmod-wl akmods akmod-wl
* Install kernel-devel - sudo dnf install kernel-devel
* Reboot

The above got my Wi-Fi adapter working. I got the steps from the following [blog post on thetestspeciment.com](https://www.thetestspecimen.com/posts/broadcom-wifi-modules-fedora/)