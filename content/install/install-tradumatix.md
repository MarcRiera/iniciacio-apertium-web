---
title: "Instal·lació d'Apertium a Linux (Tradumàtix)"
weight: 20
disableToc: true
---
1. Obriu el terminal, escriviu l'ordre següent i premeu Intro:

> ```sudo synaptic-pkexec```

2. Baixeu-vos la clau d'Apertium i deseu-la en una carpeta: https://apertium.projectjj.com/apt/apertium-packaging.public.gpg

3. A Synaptic, a "Fonts de programari", importeu la clau que us heu baixat i el repositori d'Apertium:

> ```deb http://apertium.projectjj.com/apt/nightly xenial main```

4. Actualitzeu la llista de paquets amb el botó superior esquerre de Synaptic.

5. Cerqueu el paquet "apertium-all-dev" i marqueu-lo per instal·lar. Apliqueu els canvis.

6. Obriu l'explorador de fitxers i creeu una carpeta anomenada "apertium" a /home/samba/homes/<elvostreNIU>.

7. Baixeu-vos Apertium Viewer i deseu-lo a la carpeta "apertium": https://svn.code.sf.net/p/apertium/svn/builds/apertium-viewer/apertium-viewer.jar

8. Obriu el panell de propietats del fitxer "apertium-viewer.jar", i marqueu el fitxer com a executable.
