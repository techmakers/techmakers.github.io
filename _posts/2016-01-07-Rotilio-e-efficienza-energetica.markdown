---
layout: post
title:  "Rotilio e l'efficienza energetica"
subtitle: "come controllare il proprio impianto di riscaldamento con Rotilio"
date:   2016-01-07 09:20:29 +0100
categories: Rotilio
---



Vogliamo inaugurare il nostro blog con un articolo riguardante il Decreto Legislativo per il riempimento della [direttiva europea](http://www.formazione.enea.it/documents/direttiva_2012_27_UE.pdf) 2012/27/UE sull'efficienza energetica varato dal Consiglio dei Ministri il 30 Giugno 2014.

La normativa prevede che tutti i condomini con riscaldamento centralizzato si muniscano di valvole termostatiche per ogni termosifone presente nell'appartamento di modo che il monitoraggio dei consumi e la contabilizzazione del calore avvenga correttamente. 


Noi di Techmakers che crediamo nell'efficienza energetica e nella facile gestione della casa attraverso l'internet of things, abbiamo pertanto realizzato il nostro primo prodotto IoT, [Rotilio](http://techmakers.io/rotilio.html) piattaforma hardware e software open source che con l'ausilio di diversi sensori e la presenza del [Photon](https://www.particle.io) permette l'automatizzazione di alcuni aspetti della vita domestica e non solo.

Rotilio è dotato di un sensore per la misurazione della temperatura e permette l'accensione e lo spegnimento dell'impianto di riscaldamento in base alla temperatura ambientale, inoltre è possibile misurare l'effettivo tempo di accensione dell'impianto di modo che si rispettino le ore di utilizzo previste dalla [normativa](http://www.intrage.it/Casa/riscaldamento_periodi_e_orari_di_accensione#).
Per essere sicuri di non superare la soglia indicata, è possibile predisporre la nostra piattaforma al fine di inviare una notifica del superamento del limite di attività consentito.


Abbiamo realizzato Rotilio in modo che sia uno strumento di facile utilizzo che comprende: firmware, applicazioni web e mobile, cloud di comunicazione, dashboard di controllo e amministrazione e che permetta in questo specifico caso la gestione dell'impianto di riscaldamento da remoto. L'utilizzo intuitivo e l'istallazione veloce permettono la lettura dei dati in tempo reale, la visualizzazione dello storico di dati ed eventi attraverso la app e una gestione efficiente della temperatura e del consumo di calore, oltre ad una possibilità di risparmio sui costi annuali del riscaldamento. 

Un controllo efficace ed efficente del riscaldamento, e quindi delle  [emissioni di PM10](http://www.meccanismo.it/termotecnica/emissioni-inquinanti-impianti-di-riscaldamento-domestico-pellet-legna-cippato/) (Materia Particolata) nell'aria, permette inoltre un risparmio per quanto riguarda il costo medio annuale che può variare dal 10% al 60%, con la sola variazione di un grado della temperatura ad esempio da 21°C a 20°C (limite dei 20°C imposto per legge [DPR 412/93](http://efficienzaenergetica.acs.enea.it/doc/dpr412-93.pdf)), il risparmio annuo conisterebbe nel 7%. 

Questi dati hanno rafforzato le nostre convinzioni sulla necessità di creare una piattaforma flessibile che ci permettesse l'interazione con con le "cose" che caratterizzano la nostra vita quotidiana.

Rotilio è dotato del sensore di temperatura DS18B20 della Maxim Integrated che lavora in connessione 1-Wire e che può segnalare allarmi per temperature fuori range con consumi estremamente bassi.

La connessione su 1-Wire permette sia di sfruttare un unico pin della MCU per più sensori, sia di posizionare il sensore ad una certa distanza con solo due fili di collegamento.

Attraverso il rele in dotatzione è possibile interagire con le "cose" accendendo e spegnendo la calderina o nel caso in cui i termosifoni siano elettrici si può controllare ogni singolo elemento.

La [App](http://rotilio.cc/#/home) mobile e WEB dedicata che abbiamo costruito per Rotilio permette la visualizzazione di tutti i parametri di funzionamento e una facile gestione in base alle esigenze di ogni utente.

Il tutto grazie al metodo di configurazione automatica dell'interfaccia in base alle impostazioni ricevute dal dispositivo che si sta interrogando.

Da non dimenticare la perfetta integrazione con il Cloud di [Particle.io](https://www.particle.io), che permette quindi di raggiungere tutti i dispositivi Rotilio con semplici chiamate https come ad esempio:

```
http://api.particle.io/v1/devices/0123456789abcdef01234567/temperature
```







