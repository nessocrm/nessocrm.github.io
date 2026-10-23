# Nesso — sito

Sito di Nesso, il motore fra EspoCRM e un sistema esterno. Jekyll, senza Actions. Italiano in `/it/`, inglese in `/en/`.

Il manuale del prodotto sta nel repository [nessocrm/nessocrm](https://github.com/nessocrm/nessocrm), cartella `docs/`. Questo sito non lo ricompila.

## Anteprima locale

```bash
bundle install
bundle exec jekyll serve
```

Apri `http://127.0.0.1:4000/it/`.

## Cosa non è

Non è un connettore con il nome di un gestionale. Non è un secondo CRM. Non raccoglie email: la prova è il repository, con un Espo vuoto.
