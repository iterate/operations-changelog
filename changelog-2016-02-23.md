# Rapport OPS-kveld 2016-02-23

## Fjerne Quitters

Renset opp i brukere.

## Backup av app

Vi har byttet backup av viktige ting på App-serveren fra Amazon Glacier til Rsync.net via
duplicity.

## Provisjonering av Postgresql på App

Vi har lagd en plugin til Dokku som oppretter Postgresql-databaser til
nyopprettede apps på App-serveren. (https://github.com/iterate/dokku-db-plugin)
