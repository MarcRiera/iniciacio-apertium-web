---
title: "Com funciona?"
weight: 12
disableToc: true
---

Apertium és una plataforma de traducció automàtica formada per mòduls connectats en cadena. Aquests mòduls no estan dissenyats per a una combinació de llengües en concret; les dades lingüístiques dels parells estan programades a part, de manera que és possible crear parells nous sense haver de modificar els mòduls en si.

![Apertium pipeline](/images/Apertium_system_architecture.png)

Els mòduls es comuniquen mitjançant una cadena de text que al principi conté text original. Cada mòdul l'altera fent la tasca concreta per al qual ha estat programat fins que després de l'últim mòdul el text es troba en la llengua d'arribada. Exemple de traducció de la frase «The blue house» de l'anglès al català («La casa blava»):

```
1. The blue house
2. ^The/the<det><def><sp>$ ^blue/blue<adj><sint>/blue<n><sg>$ ^house/house<n><sg>/house<vblex><inf>/house<vblex><pres>/house<vblex><imp>$ 
3. ^The/The<det><def><sp>$ ^blue/blue<adj><sint>$ ^house/house<n><sg>$ 
4. ^The<det><def><sp>$ ^blue<adj><sint>$ ^house<n><sg>$ 
5. ^The<det><def><sp>/El<det><def><GD><ND>$ ^blue<adj><sint>/blau<adj>$ ^house<n><sg>/casa<n><f><sg>/cambra<n><f><sg>/càmera<n><f><sg>$ 
6. ^Det_nom_adj<SN><DET><f><sg>{^el<det><def><3><4>$ ^casa<n><3><4>$ ^blau<adj><3><4>$}$ 
7. ^El<det><def><f><sg>$ ^casa<n><f><sg>$ ^blau<adj><f><sg>$ 
8. ~La casa blava 
9. La casa blava 
```
