---
title: "Diccionari monolingüe"
anchor: "Diccionari monolingüe"
weight: 31
---
Dins d'un parell de llengües, hi ha dos diccionaris monolingües (un per a cada llengua). Aquests diccionaris contenen una llista d'entrades lèxiques amb etiquetes que proporcionen informació morfològica. Els diccionaris fan servir el format XML, i s'estructuren en dues columnes: a l'esquerra hi ha la forma superficial de l'entrada (amb flexió i sense etiquetes), i a la dreta hi ha la forma interna (l'arrel amb etiquetes). La forma interna serveix per a agrupar en una mateixa entrada diferents formes superficials, com les conjugacions verbals o les diferents formes dels adjectius.

Exemples d'entrades lèxiques en català ("casa", substantiu femení):

```xml
<l>casa</l><r>casa<s n="n"/><s n="f"/><s n="sg"/></r>
<l>cases</l><r>casa<s n="n"/><s n="f"/><s n="pl"/></r>
```
La primera entrada de l'exemple anterior indica que la forma superficial «casa» equival a la forma interna «casa<n><f><sg>» (nom femení singular). La segona indica que la forma superficial «cases» equival a la forma interna «casa<n><f><pl>» (nom femení plural).

Tot i que aquest exemple correcte i funcional, només per a "casa" calen dues entrades: una per a la forma en singular i una altra per a la forma en plural. Això és poc eficient (amb conjugacions verbals el diccionari es complicaria massa), per la qual cosa habitualment es recorre a l'ús de paradigmes.

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
