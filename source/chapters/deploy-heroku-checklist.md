---
title: Checklist deploy su Heroku
---

# Setup generale

* Stiamo usando lo stack Cedar?
* La region è impostata su `eu`?
* Stiamo usando background jobs?
  * Abbiamo attivato un worker nel `Procfile`?
* Sono state impostate tutte le variabili `ENV` necessarie?
  * `SECRET_KEY_BASE`
  * API keys varie (controlla il tuo file `.env` locale)

## Invio emails

* Abbiamo attivato l'[addon di Mandrill](https://addons.heroku.com/mandrill)?
* Sono state impostate le `ENV` per `SMTP_*`?

## Cron jobs

* Abbiamo impostato [Heroku Scheduler](https://addons.heroku.com/scheduler)?

# Ambienti di produzione

* Abbiamo già impostato il dominio da puntare?
* Stiamo trackando gli errori con Errbit?
* I backup con [PG Backups](https://addons.heroku.com/pgbackups) sono stati impostati?
* Abbiamo aggiunto il rake task che controlla il limite di rows sul db heroku?

## SEO
* Abbiamo inserito `meta noindex` nell'head della pagina?
* Abbiamo aggiunto `robots.txt`?
* Abbiamo generato la sitemap?
