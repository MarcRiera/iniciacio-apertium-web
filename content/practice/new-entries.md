---
title: "Entrades noves als diccionaris"
anchor: "Entrades noves als diccionaris"
weight: 41
---
En aquesta pràctica aprendreu a expandir els diccionaris d'Apertium perquè reconegui més paraules. A partir d'un parell de prova entre l'anglès i el català creareu un traductor automàtic bàsic.

## Abans de començar

1. Instal·leu els paquets de desenvolupament d'Apertium i Apertium Viewer.

2. Baixeu-vos el [parell de prova](/files/apertium-prova.zip) i extraieu-lo en una carpeta.

3. Obriu un terminal a les dues carpetes monolingües (apertium-eng i apertium-cat) i executeu:
```xml
./autogen.sh
```

4. Obriu un terminal a la carpeta bilingüe (apertium-eng-cat) i executeu:
```xml
./autogen.sh --with-lang1=../apertium-eng --with-lang2=../apertium-cat
make langs
```

5. Executeu l'Apertium Viewer. Des del menú File>Load a language pair, aneu a la carpeta on teniu el parell de prova i seleccioneu els fitxers "eng-cat.mode" i "cat-eng.mode", que trobareu a "apertium-eng-cat/modes".

Ara ja està instal·lat el parell de prova a l'Apertium Viewer. Després de qualsevol modificació que feu als diccionaris, si voleu veure el resultat, executeu abans la segona ordre del pas 4.


## Diccionari monolingüe

Afegiu les entrades següents al diccionari anglès:

```xml
chair
window
door
kitchen
room
computer
TV
book
mouse
keyboard
blue
red
green
big
small
beautiful
```

Ara feu el mateix però en català:

```xml
cadira
finestra
porta
cuina
habitació
ordinador
televisor
llibre
ratolí
teclat
blau
vermell
verd
gran
petit
bonic
```

## Diccionari bilingüe

A partir de les entrades que heu afegit anteriorment, creeu la llista d'equivalències al diccionari bilingüe del parell. Fet això, Apertium hauria de reconèixer les paraules i ja hauríeu aconseguit crear el vostre primer parell!

