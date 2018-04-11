---
title: "Diccionari bilingüe"
anchor: "Diccionari bilingüe"
weight: 32
---
Dins d'un parell de llengües, hi ha dos diccionaris monolingües (un per a cada llengua). Aquests diccionaris contenen una llista d'entrades lèxiques amb etiquetes que proporcionen informació morfològica. Els diccionaris fan servir el format XML, i s'estructuren en dues columnes: la forma superficial de l'entrada (amb flexió i sense etiquetes) i la forma interna (arrel amb etiquetes).

Exemples d'entrades lèxiques en català ("casa", substantiu femení):

```xml
<l>casa</l><r>casa<s n="n"/><s n="f"/><s n="sg"/></r>
<l>cases</l><r>casa<s n="n"/><s n="f"/><s n="pl"/></r>
```

Tot i ser correcte i funcional, només per a "casa" calen dues entrades: una per a la forma en singular i una altra per a la forma en plural. Això és poc eficient (amb conjugacions verbals el diccionari es complicaria massa), per la qual cosa es defineixen els paradigmes.

Un paradigma és una entrada lèxica que serveix de model per a d'altres. "Taula", per exemple, fa el plural de la mateixa manera que "casa" (canvia -a per -es). Per tant, amb el paradigma "casa" podem obtenir la flexió de qualsevol substantiu femení similar. Exemple de paradigma i entrades lèxiques que s'hi basen:

```xml
<pardef n="cas/a__n">
    <e><p><l>a</l><r>a<s n="n"/><s n="f"/><s n="sg"/></r></p></e>
    <e><p><l>es</l><r>a<s n="n"/><s n="f"/><s n="pl"/></r></p></e>
</pardef>

<e lm="casa"><i>cas</i><par n="cas/a__n"/></e>
<e lm="taula"><i>taul</i><par n="cas/a__n"/></e>
```

Els paradigmes permeten estalviar temps i espai, i milloren substancialment l'organització interna dels diccionaris.
