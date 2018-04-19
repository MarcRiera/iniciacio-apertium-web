---
title: "Quins mòduls hi ha?"
weight: 13
disableToc: true
---

Apertium es basa en una cadena de mòduls que alteren un text de manera lineal. Els principals són els diccionaris. Cada parell està format per tres diccionaris de dos tipus:

* Diccionari monolingüe: n'hi ha dos, un per a cada llengua del parell. Conté entrades lèxiques (paraules o multiparaules) i la seva informació morfològica (conjugacions, declinacions, etc.).
* Diccionari bilingüe: n'hi ha un i conté una llista d'entrades lèxiques en les dues llengües del parell. Estableix com es relacionen les entrades de les dues llengües entre si.

A més, hi ha dos altres mòduls imprescindibles:

* Desambiguador: en cas d'ambigüitat durant l'anàlisi de la llengua d'origen, tria la millor opció a partir d'un model estadístic.
* Regles de transfèrencia: aplica canvis a les entrades lèxiques (canvis d'ordre, de gènere, declinacions, etc.).

Hi ha molts altres mòduls que amplien les possibilitats d'Apertium.
