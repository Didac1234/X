# Projecte 2 - Supabase Migration

Aquest projecte ara està preparat per utilitzar Supabase com a origen de dades persistent.
Si `useSupabase` està activat, la web carregarà les respostes des d'una taula Supabase i desarà noves respostes allà.
Si `useSupabase` està desactivat, el comportament continua usant la base de dades simulada en memòria.

## Passos per configurar Supabase

1. Crea un nou projecte a [Supabase](https://app.supabase.com).
2. A la secció `Table Editor`, crea una taula anomenada `respostes` amb els següents camps:
   - `id` - `bigint` o `bigserial` com a `PRIMARY KEY` amb `auto increment`.
   - `grup` - `text`
   - `puntuacio` - `integer`
   - `comentari` - `text`
   - `data` - `timestamptz`

3. Configura les polítiques de seguretat (RLS) perquè el client pugui llegir i inserir dades públicament. A `SQL Editor` executa:

```sql
-- Activa RLS a la taula
ALTER TABLE public.respostes ENABLE ROW LEVEL SECURITY;

-- Permet seleccions públiques
CREATE POLICY "Allow read" ON public.respostes
  FOR SELECT
  USING (true);

-- Permet insercions públiques
CREATE POLICY "Allow insert" ON public.respostes
  FOR INSERT
  WITH CHECK (true);
```

4. A la pàgina de `Settings > API`, copia el `URL` del projecte i la `anon public key`.
5. A `index.html`, actualitza la configuració de Supabase:

```js
const useSupabase = true;
const SUPABASE_URL = "https://<your-project>.supabase.co";
const SUPABASE_ANON_KEY = "<your-anon-key>";
```

6. Si proves en local amb un fitxer estàtic, obre la web des d'un servidor local perquè Supabase accepti la crida. Per exemple:

```powershell
cd c:\Users\DAW1\Desktop\X
python -m http.server 8000
```

Després obre `http://localhost:8000` al navegador.

7. A Supabase, afegeix `http://localhost:8000` i `http://127.0.0.1:8000` a les ORIGINS autoritzades si és necessari.

## Com funciona la migració

- `index.html` ara canvia entre emmagatzematge local o Supabase segons `useSupabase`.
- Quan Supabase està activat:
  - es llegeixen totes les respostes de la taula `respostes` en iniciar la pàgina.
  - es desaran noves respostes mitjançant `insert` a Supabase.
- Si Supabase falla, el fitxer mostra un missatge d'error i continua amb les dades locals.

## Notes addicionals

- L'ús de la clau `anon` des d'una aplicació estàtica és acceptable per a demos i prototips, però no és la millor opció per a producció a llarg termini.
- Per desplegar en el núvol (Vercel) després, només cal pujar el mateix `index.html` i assegurar-se que les claus del projecte estiguin disponibles com a variables d'entorn o substituïdes en el fitxer.
- Si vols, puc ajudar-te a crear una versió amb `index.html` separant la lògica de Supabase en un petit fitxer `app.js` o afegint `README` de desplegament a Vercel.
