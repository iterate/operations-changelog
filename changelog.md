Changelog Operations
====================

1. Gamle kontoer fjernet fra LDAP, Google, Atlassian, Github etc.
2. Multi-site backup av PostgreSQL
3. Ryddet i LDAP-grupper
4. Serverrom ryddet for skrot
5. Manuell justering av timer i leancast
6. Oppdatering av firmware alle AP i G9
7. Forsøk på rens av støvsuger
8. Vask og rydd av kjøkken med kaffetrakter/kolber.
9. Startet prosess rundt innkjøpt av mikrofon og lydanlegg til G9


## Gamle kontoer fjernet

Alle gamle kontoer er fjernet med hard hånd. Om noen har fått seg fjernet
ved en feil, er det bare et tegn på at operations ikke liker deg.

## Multi-site backup av PostgreSQL

Det tas nå backup av PostgreSQL til ops.iterate.no (linode) i tilegg til
Amazon Glacier. Dette er for å ha redundans med en mindre kompleks løsning, og
lar oss få opp kjernetjenestene kjappere ved total kollaps.

## Ryddet i LDAP-grupper

LDAP ble ryddet for gammel skrot. For å hjelpe til i arbeidet ble
`phpldapadmin` lagt inn på gatekeeper. Den kan nås på
http://192.168.1.1/phpldapadmin på G9 nettet. Bruk LDAP admin for pålogging.

Grupper som ble fjernet inkluderer mno, em1, leancast-dev, leancast-staging,
leancast-prod, etc etc etc. 

## Serverrom ryddet for skrot

Martin gjorde en heroisk innsats på serverrommet (som straff for å ikke ha med
laptop på opskveld (!)). 

Strømadaptere, skjermadaptere, nettverks- og eurokabler ligger i hver sin
pappeske i hyllen der inne, markert med hva innholdet er.

## Manuell justering av timer i Leancast

Det ble justert timer med har SQL-hånd hvor det var behov.

## Oppdatering av firmware på alle AP i G9

Alle aksesspunkt ble oppgradert til siste firmware, med blant annet fiks for 
"heartblood" og "shellshack" (I kid you not).

## Rens av støvsuger

Den er død. Kan nå kastes. (Full av byggstøv).

## Vask av kjøkken

Kjøkkenet ble vasket, kolbene ble vasket i maskin, benk vasket etc. Såpe og
vann, hand i hand.

## Startet prosess rundt innkjøpt av mikrofon og lydanlegg til G9

Undersøkt receivere til lydanlegg, og sjekket opp forskjellige alternativer
for "konferanse-mikrofon" vi kan bruke til foredrag og lyntaler. Skal snakke
med HiFi-klubben og kanskje andre for å få tilbud og anbefalinger som kan passe
våre lokaler.
