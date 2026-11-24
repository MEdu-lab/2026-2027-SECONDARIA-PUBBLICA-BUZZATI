# Struttura del repository

Il `README.md` di questo repository **non va modificato a mano**: è il documento di progetto, rigenerato automaticamente dalla GitHub Action a ogni modifica di `config.yml` o `docs/sezioni/`. Qualsiasi cosa scritta lì dentro viene sovrascritta alla build successiva. Questo file serve quindi da indice.

## Il progetto formale

| Percorso | Cosa è |
| --- | --- |
| [`config.yml`](config.yml) | Unica fonte di verità dei dati: titolo, anno scolastico, operatori, date, orari, numero di partecipanti. Le sezioni del progetto leggono da qui |
| [`docs/sezioni/`](docs/sezioni) | Il testo del progetto, in markdown, un file per sezione. L'ordine nel documento segue l'ordine alfabetico dei nomi dei file |
| [`docs/README.md`](docs/README.md) | Documentazione dei campi di `config.yml` |
| [`styles/`](styles) | Template LaTeX e pacchetti usati da Pandoc per impaginare il PDF |
| [`images/`](images) | Immagini incluse nel documento |
| `README.md` | **Generato.** Il documento assemblato, pronto per Pandoc |

Il PDF compilato è pubblicato a ogni push su
<https://medu-lab.github.io/2026-2027-SECONDARIA-PUBBLICA-BUZZATI/latest.pdf>
ed è anche scaricabile come artifact della build.

## Il laboratorio quotidiano

| Percorso | Cosa è |
| --- | --- |
| [`materiali/`](materiali) | Documenti pronti all'uso: locandina per le famiglie, questionario di inizio corso |
| [`resoconti/`](resoconti) | Un resoconto per incontro: cosa si è fatto, cosa ha funzionato, cosa riprendere |
| [`idee/`](idee) | Magazzino di attività, strumenti da costruire e ascolti da proporre |

Queste tre cartelle non entrano nel PDF e non fanno ripartire la compilazione: il workflow le esclude esplicitamente.
