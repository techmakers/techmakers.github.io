---
layout: post
title:  "Guida base Rotilio"
subtitle: "Guida base per l'utilizzo della nostra piattaforma IoT"
date:   2016-01-15 09:20:29 +0100
categories: Rotilio
---
Techmakers
				
![techmakers](../img/post/techmakersLogo110 copia.png) 


Prima di addentrarsi nella parte pratica è necessario dotarsi della strumentazione necessaria all'utilizzo della piattaforma.

Setup di base

Smartphone iOS o Android con installata App Particle.io

- [Android](https://play.google.com/store/apps/details?id=io.particle.android.app)

- [iOS](https://itunes.apple.com/it/app/particle-build-photon-electron/id991459054?l=en&mt=8)

Un computer Mac, Linux o Windows

Installare [NODEjs](https://nodejs.org)

Installare [NODE-RED](http://nodered.org/)

Installare i componenti Particle per l'interazione con NODE-RED attraverso il comando da terminale:

Mac e Linux

```
sudo npm install -g node-red-contrib-particle
```
Windows

```
npm install -g node-red-contrib-particle
```
Un altro passaggio che noi giudichiamo fondamentale prima di passare alla parte pratica consiste nel clonare la nostra repository di GitHub [ https://github.com/techmakers/rotilio.cc]( https://github.com/techmakers/rotilio.cc) in modo da usufruire dei futuri aggiornamenti dell'interfaccia senza intaccare le modifiche che fate alla vostra versione di App.

Nel caso non foste ancora inscritti a GitHub potete farlo al seguente link [https://github.com/](https://github.com/) oppure potete usufruire della versione aggiornata e funzionante dell'interfaccia [https://rotilio.cc](https://rotilio.cc).

Pratica

1 Accendere Rotilio

Come procedere all'accensione di Rotilio:

- Aprire l'applicazione Particle sul proprio smartphone e registrasi

![home](../img/post/home.jpg) ![signin](../img/post/signin.jpg)

- dopo la registrazione sarà visibile la dashboard vuota da cui è possibile aggiungere un nuovo dispositivo

![dashboard](../img/post/dashboard.jpg) ![addevice](../img/post/addevice.jpg)

- Scegliendo la voce Photon si procede con la registrazione, Rotilio ora deve essere alimentato e connesso seguendo le indicazioni fornite dall'Applicazione

![config](../img/post/config.jpg) ![connect](../img/post/connect.jpg)

- Successivamente bisogna collegare lo smartphone al Rotilio attraverso dei semplici passaggi

![wifi](../img/post/wifi.jpg) ![wifiP](../img/post/wifiP.jpg)

2 Configurazione Wifi

- Il secondo passo consiste nella configurazione del Wifi, inserendo la password della nostra rete 

![configwifi](../img/post/configwifi.jpg) ![configwifi2](../img/post/configwifi2.jpg)

- dopo questa operazione l'applicazione procederà con il set up e fornirà il nome del device, cliccando sul tasto fine si ritornerà alla dashboard iniziale con inserito il nostro nuovo device.

![setup](../img/post/setup.jpg) ![dashboard2](../img/post/dashboard2.jpg)

3 Registrazione su rotilio.cc

Con questo passaggio conclusivo sarà possibile visualizzare i dati e l'iterazione di Rotilio attraverso i sensori e gli attuattori su di esso montati.

- Per poter visualizzare il nostro Rotilio e tutti i dati è necessario procedere con la registrazione sulla nostra web app [rotilio.cc](http://rotilio.cc) con gli stessi dati utilizzati per la registrazione sull'applicazione Particle

![rotiliocc](../img/post/rotiliocc.jpg) ![device](../img/post/device.jpg)

- cliccando sull'icona freccia si accederà alla schermata variabili, 

![variables](../img/post/variables.jpg)

- cliccando sull'icona telefono sranno invece visibili gli eventi

![event](../img/post/event.jpg) ![event2](../img/post/event2.jpg)


