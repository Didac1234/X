# Sprint 1 - Projecte 2: Enquesta intel·ligent d'aula

## Objectiu
Implementar les funcionalitats bàsiques de la versió local (US-01, US-02 i US-03) perquè l'alumnat pugui enviar valoracions i el docent pugui associar-les a un grup.

## Històries d'usuari implementades
- US-01: Formulari amb validació, enviament i confirmació visual.
- US-02: Comentari opcional desat i mostrat al llistat de respostes.
- US-03: Selecció de grup (DAW1A / DAW1B / ASIX1) i associació de la resposta al grup seleccionat.

## Canvis aplicats
- Afegida confirmació visual de "Resposta guardada correctament." en verd.
- Afegida validació de puntuació entre 1 i 5 amb missatge d'error en cas de valor invàlid.
- Conservada la funcionalitat de comentari opcional i mostra en el llistat final.
- S'assegura que la resposta s'associï al grup escollit des del formulari.

## Com provar-ho
1. Obre `m1665-p2-enquesta-local.html` en un navegador.
2. Selecciona un grup, introdueix una puntuació de 1 a 5 i escriu un comentari opcional.
3. Premi "Guardar resposta".
4. Comprova que apareix el missatge de confirmació i que la nova resposta es mostra al llistat.
5. Introdueix una puntuació fora de rang (per exemple 0 o 6) i comprova que apareix l'error.

## Notes
Aquesta versió ja inclou funcionalitats més enllà del Sprint 1, però el que s'ha reforçat ara és la confirmació visual d'enviament i la validació específica del formulari.