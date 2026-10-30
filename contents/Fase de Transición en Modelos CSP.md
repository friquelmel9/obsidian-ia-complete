---
tags:
  - cs/optimization
aliases:
---
# Fase de Transición en Modelos CSP

La fase de trancisión es un concepto que se explica en [[INF295 - Inteligencia Artificial|INF295]] para explicar la siguiente pregunta

¿Si se aumenta el número de restricciones en un [[Constraint Satisfaction Problem|CSP]], el problema se volvera más rapido de resolver?

La respuesta es no necesariamente. Se responde mediante la **Fase de Transición**

![[Fase de Transición.png]]

Se separa en tres secciones
1. Un [[Constraint Satisfaction Problem|CSP]] con pocas restricciones es facil de resolver, dado que no hay una cantidad importante de restricciones, lo que genera un montón de soluciones validas
2. Un [[Constraint Satisfaction Problem|CSP]] con muchas restricciones, la cantidad de soluciones validas es muy poca, haciendo que el problema sea más facil de resolver.
3. La **Fase de Transición** están los problemas más dificles de resolver, dado que el [[Constraint Satisfaction Problem#Search Space|CSP > Search Space]] es muy grande, y no se puede apoyar en las restricciones para disminuit su filtrado.