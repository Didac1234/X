# Sprint 3 - Projecte 2: Enquesta intel·ligent d'aula

## Objectiu
Tancar la versió final del projecte amb pràctiques de manteniment, desplegament i preparació per a persistència de dades.

## Històries d'usuari envoltades
- US-08: Mantenir codi clar i versionat per facilitar manteniment.
- US-09: Desplegar la solució al núvol perquè sigui accessible i compartible.
- US-10: Preparar la migració d'array local a persistència real (Supabase) sense trencar les funcionalitats existents.

## Estat actual
- El projecte ja té un prototip funcional de la versió local amb formulari, filtrat per grup, KPIs i gràfics d'analítica.
- El codi està organitzat dins d'un sol fitxer HTML autoalbergat (`index.html`).
- No s'ha integrat encara una base de dades real ni s'ha desplegat a Vercel/Supabase des de la versió actual.

## Activitats completes de Sprint 3
- Documentació del procés i de l'estat del projecte.
- Identificació clara de les tasques pendents de desplegament i persistència.
- Preparació del projecte per a una futura migració: el prototip local pot evolucionar a Supabase mantenint les mateixes regles de filtrat i càlculs.

## Tasques pendents
- Configurar repositori Git amb commits descriptius i branques per preparar el workflow IA3.
- Deploy a Vercel d'una versió estàtica del projecte perquè sigui verificable públicament.
- Integrar Supabase (o un backend equivalent) per desar respostes de manera persistent i carregar-les en temps real.
- Validar de nou US-04..US-07 sobre dades persistides després de migrar la capa de dades.

## Prova manual suggerida
1. Obre `index.html` en un navegador local.
2. Revisa que el formulari envia dades, que el panell d'analítica respon al filtre de grup i que el llistat mostra respostes filtrades.
3. Comprova que el codi actual està llest per a una migració a backend amb canvis mínims en la lògica de filtrat i càlculs.
4. Documenta els passos de desplegament de Vercel i Supabase en un fitxer separadet (`README.md`) en el següent sprint.

## Conclusions
Aquest Sprint 3 es focalitza en portar el projecte cap a la fase de lliurament real: control de versions, desplegament i migració a persistència.
Per completar-lo plenament, els següents passos són desplegar a Vercel i integrar Supabase, després de validar les funcions existents respecte a dades reals.