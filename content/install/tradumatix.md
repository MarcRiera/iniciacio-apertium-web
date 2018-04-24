---
title: "Instal·lació d'Apertium a Linux (Tradumàtix)"
weight: 22
disableToc: true
---
1. Obriu el terminal, escriviu l'ordre següent i premeu Intro:
```xml
sudo synaptic-pkexec
```

2. Baixeu-vos la clau d'Apertium i deseu-la en una carpeta: https://apertium.projectjj.com/apt/apertium-packaging.public.gpg

3. A Synaptic, a "Fonts de programari", importeu la clau que us heu baixat i el repositori d'Apertium:
```xml
deb http://apertium.projectjj.com/apt/nightly xenial main
```

4. Actualitzeu la llista de paquets amb el botó superior esquerre de Synaptic.

5. Cerqueu el paquet "apertium-all-dev" i marqueu-lo per instal·lar. Apliqueu els canvis.
