---
title: How to Install Nessus on Ubuntu 20.04
description: >-
  Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor
  incididunt ut labore et dolore magna aliqua.
date: '2020-12-07T17:30:53.930Z'
modified: '2020-12-07T17:30:53.930Z'
tags:
  - Nessus
  - Ubuntu 20.04
categories: []
layout: post
---
Installation Instructions for Ubuntu 20.04

Head on over to [Download Nessus | Tenable®](https://www.tenable.com/downloads/nessus?loginAttempted=true)
Click to Download Nessus-8.12.1-ubuntu1110_amd64.deb
![nessus-download](https://i.imgur.com/GkOESuM.png)Open a terminal and navigate to where the .deb file was downloaded to.
Run the command:

```shell
sudo dpkg -i Nessus-8.12.1-ubuntu1110_amd64.deb
```

![dpkg-nessus-install](https://i.imgur.com/q2Jxb2q.png)
If you have ufw (uncomplicated firewall) running enter:

```shell
sudo ufw allow 8834
```

Next we will enable and start the nessus daemon

```shell
#Use these two commands to enable then start Nessus
sudo systemctl enable nessusd
sudo systemctl start nessusd
```

In your web browser navigate to https://vulnscan:8834/

Choose Advanced -> Accept the Risk and Continue

Choose Nessus Essentials

Enter your First / Last Name, and email to receive and activation code

Copy and Paste the Code from your email into the Activation code spot and choose continue

Next Create a user account and then continue

Nessus will begin to Download and install necessary files

For extra information check: 

   <https://docs.tenable.com/nessus/Content/GettingStarted.htm>