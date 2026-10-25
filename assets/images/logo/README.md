# Marchio

I file usati dal sito sono tre, copiati dal repository del prodotto:

- `logo-light.svg` — lockup su fondo chiaro
- `logo-dark.svg` — lockup su fondo scuro
- `favicon.svg` — il segno, anche in `/favicon.svg`

Il layout punta solo al vettore. Non c'è un bitmap del template precedente.

## Palette del sito

I quattro colori del simbolo restano invariati: grigio `#8B939C`, ambra `#E4A133`, blu `#5589CA`, verde `#58C97A`.

I ruoli cromatici sono definiti in `assets/css/brand-theme.css` e collegati alle utility Tailwind in `_layouts/default.html`. Usare `bg-canvas`, `bg-surface`, `text-ink`, `text-muted`, `text-link`, `text-accent` e `border-line` per gli elementi che seguono il tema. Evitare valori esadecimali nelle classi delle pagine.

| Ruolo | Chiaro | Scuro |
|---|---|---|
| Sfondo | `#F4F5F7` | `#262626` |
| Superficie | `#FFFFFF` | `#303337` |
| Testo principale | `#262626` | `#F4F5F7` |
| Testo secondario | `#525B66` | `#B9C2CC` |
| Link | `#2B5E9C` | `#8FB9EB` |
| Accento testuale | `#91590C` | `#E4A133` |
| Stato positivo | `#236F3D` | `#58C97A` |

Le varianti più scure nel tema chiaro rendono leggibili gli accenti su bianco. I pulsanti principali usano l’ambra originale (`bg-accent-fill`) con testo antracite (`text-on-accent`); quelli blu usano la coppia `bg-action text-on-action`, che varia insieme al tema.

Una fascia sempre scura deve usare `bg-brand-night brand-inverse`: la classe imposta anche i colori di testi, link e bordi al suo interno. Non applicare `brand-inverse` a superfici che devono seguire il tema.

Le regole dei componenti condivisi sono nello stesso foglio cromatico. Dimensioni, griglie, animazioni e breakpoint restano nei fogli esistenti. Le classi `dark:hidden` e `dark:block` continuano a selezionare il logo appropriato.
