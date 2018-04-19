---
title: "Diccionari bilingüe"
anchor: "Diccionari bilingüe"
weight: 32
---
El diccionaris bilingüe conté una llista d'equivalències entre entrades de les dues llengües que formen el parell. S'estructura en dues columnes: a l'esquerra hi ha la forma interna amb etiquetes de l'entrada de la primera llengua, i a la dreta hi ha la forma interna amb etiquetes equivalent de la segona llengua.

Exemples d'entrades bilingües entre l'anglès i el català:

```xml
<e><p><l>house<s n="n"/><s n="sg"/></l><r>casa<s n="n"/><s n="f"/><s n="sg"/></r></p></e>
<e><p><l>house<s n="n"/><s n="pl"/></l><r>casa<s n="n"/><s n="f"/><s n="pl"/></r></p></e>
```

Tot i que l'exemple és correcte i funcional, definir les equivalències entre entrades lèxiques molt complexes (com els verbs) seria massa feixuc. Per sort, podem simplificar-ho obviant les etiquetes que es repeteixen a tots dos costats: Apertium no transfereix les etiquetes especificades al diccionari i transfereix automàticament d'un costat a l'altre qualsevol etiqueta extra:

```xml
<e><p><l>house<s n="n"/></l><r>casa<s n="n"/><s n="f"/></r></p></e>
``` 

En aquest cas, l'entrada serviria tant per a «house<n><sg>» com per a «house<n><pl>».

De la mateixa manera que amb els diccionaris monolingües, és possible definir paradigmes:

```xml
<pardef n="house-casa__n">
    <e><p><l><s n="n"/></l><r><s n="n"/><s n="f"/></r></p></e>
</pardef>

<e><p><l>house</l><r>casa</r></p><par n="house-casa__n"/></e>
```

Finalment, hi ha l'opció de definir entrades no bidireccionals. En el cas dels diccionaris bilingües, "LR" (left-to-right) indica que una entrada només funcionarà d'esquerra a dreta, i "RL" indica que només funcionarà de dreta a esquerra. Exemple:

```xml
<e r="LR"><p><l>house<s n="n"/></l><r>llar<s n="n"/><s n="f"/></r></p></e>
<e r="RL"><p><l>dream<s n="vblex"/></l><r>somniar<s n="vblex"/></r></p></e>
```

Això és molt útil quan una de les dues llengües té gènere i l'altra no, com passa amb l'anglès i el català. Exemple (l'etiqueta «<GD>» indica que Apertium ha d'escollir entre un dels dos gèneres en funció de la informació que tingui):

```xml
<e r="LR"><p><l>president<s n="n"/></l><r>president<s n="n"/><s n="GD"/></r></p></e>
<e r="RL"><p><l>president<s n="n"/></l><r>president<s n="n"/><s n="m"/></r></p></e>
<e r="RL"><p><l>president<s n="n"/></l><r>president<s n="n"/><s n="f"/></r></p></e>
```

