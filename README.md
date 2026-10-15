# LESA — sito

Sito statico di LESA (Low-cost Soil Sensor Array), pubblicato con GitHub Pages su `www.ivett.it`.
Nessun build, nessuna dipendenza: `index.html` + `assets/styles.css`.

## Modificare i contenuti

- Testi e sezioni: `index.html`. Ogni sezione è un blocco `<section id="…">`; le linguette a destra (`#tabs`) e il menu mobile (`.topnav`) elencano gli stessi id.
- Stile: `assets/styles.css`. I colori sono in `:root` (`--lime`, `--leaf` sono quelli del logo).
- Foto: `assets/`. Sostituire `angela.jpg`, `sayed.jpg`, `cascina.jpg` con gli originali mantenendo il nome.
- Il modulo "Prenota" apre il programma di posta del visitatore con una mail già compilata per `info@ivett.it`; l'indirizzo è nello `<script>` in fondo a `index.html` e nel footer.
- Il link a Piantami è il bottone "scopri Piantami: clicca qui" (`https://piantami.com`).

## Pubblicare

Ogni push su `main` aggiorna il sito in un paio di minuti.

```
git add -A && git commit -m "Aggiorna testi" && git push
```

## Verifica locale

```
python3 -m http.server 8767 --bind 127.0.0.1     # poi apri http://127.0.0.1:8767
uv run --with playwright python check.py         # controlli automatici + screenshot
```
