# Eibit — homepage

Homepage statica (un'unica pagina, inglese, copy in stile IBM Style Guide,
voce "we/you" verso il cliente) per Eibit, società di consulenza
tecnologica indipendente: AI, distributed ledger, cybersecurity, cloud
architecture, integrazione di sistemi, sistemi legacy.

## Struttura

| File            | Descrizione                                            |
| --------------- | ------------------------------------------------------ |
| `index.html`    | La pagina (struttura semantica + contenuti)            |
| `styles.css`    | Stile; palette e font come variabili `:root`           |
| `fonts.css`     | Dichiarazioni `@font-face` per i font locali           |
| `fonts/`        | Font woff2 (Inter 400/500, Spectral 400/500/600; subset latin e latin-ext) |
| `og-image.png`  | Anteprima 1200×630 per la condivisione (LinkedIn, …)   |
| `robots.txt`    | Permessi per i crawler + riferimento al sitemap        |
| `sitemap.xml`   | Sitemap (un'unica URL: `https://www.eibit.it/`)        |

Nessun build, nessun backend, nessun JavaScript, nessuna dipendenza
esterna: i font (Inter + Spectral) sono serviti localmente da
`fonts.css`/`fonts/`, con fallback di sistema.

Dominio canonico: `https://www.eibit.it` (canonical, og:*, sitemap, robots).
Se si sceglie l'apice senza www, aggiornare questi 4 punti.

`og-image.png` è un asset statico: per rigenerarlo o cambiarne il design
basta sovrascriverlo (stesse dimensioni 1200×630, o 2400×1260 per nitidezza).

## Dati della società

Eibit S.r.l. — `info@eibit.it` — Turin, Italy —
[LinkedIn](https://www.linkedin.com/company/eibit).
Nessun altro dato da esporre (no P.IVA, no indirizzo completo).

## Personalizzazione

- **Colori**: variabili `--bg`, `--ink`, `--muted`, `--hairline`, `--accent`
  in cima a `styles.css`.
- **Font**: variabili `--serif` e `--sans` in `styles.css` + le
  dichiarazioni `@font-face` in `fonts.css` (file woff2 in `fonts/`).
  Per cambiare font: sostituire i file e aggiornare `font-family`/
  pesi in `fonts.css`.

## Deploy

Pubblica tutti i file (tranne `README.md` e `.gitignore`) su qualsiasi
hosting statico (Netlify, GitHub Pages, nginx, …) e configura il redirect
301 `eibit.it → www.eibit.it`.
