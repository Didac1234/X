# Sprint 2 - Projecte 2: Enquesta intel·ligent d'aula

## Objectiu
Implementar el panell d'analítica complet amb filtre per grup, KPIs en temps real, gràfiques de distribució i comparativa de mitjanes.

## Històries d'usuari implementades
- US-04: Visualització de KPIs (respostes totals, mitjana i percentatge positives) actualitzats en funció del filtre seleccionat.
- US-05: Visualització de distribució de puntuacions en gràfiques de barres i gràfics de quesito per al conjunt filtrat.
- US-06: Comparativa de mitjanes entre grups amb un gràfic de barres per mostrar la diferència entre DAW1A, DAW1B i ASIX1.
- US-07: Filtre del panell amb l'opció "Tots els grups" i selecció de grups individuals.

## Canvis destacats
- Afegit el KPI de respostes totals, mitjana i percentatge de valoracions 4-5 per al grup filtrat.
- S'han creat gràfics de distribució amb barres per cada valoració 1-5.
- S'han creat gràfics de quesito per la distribució de puntuacions i el percentatge de respostes positives.
- S'ha afegit comparativa de mitjanes per grup amb un gràfic de barres horitzontals.
- El llistat de respostes es filtra pel grup seleccionat i es mostra ordenat per data més recent.

## Prova manual
1. Obre `index.html` en un navegador.
2. Selecciona un grup del filtre del panell (`Tots els grups`, `DAW1A`, `DAW1B` o `ASIX1`).
3. Comprova que els KPIs i els gràfics es recalculen immediatament.
4. Revisa que el gràfic de distribució mostra les quantitats per cada puntuació 1-5.
5. Revisa que el gràfic de quesito mostra la proporció de puntuacions positives (4-5) en relació a la resta.
6. Observa que el gràfic de comparativa de mitjanes està disponible per als tres grups.
7. Comprova que el llistat de respostes mostra només les respostes del grup filtrat.

## Observacions
Aquesta versió ja compleix Sprint 2 amb panell d'analítica i segmentació per grup. El proper sprint pot centrar-se en control de versions, desplegament al núvol i persistència real de dades.