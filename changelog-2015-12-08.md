# Minne på Anne Frank
I forbindelse med strømbruddet for en stund siden ble det oppdaget at en eller
flere av RAM-brikkene i Anne Frank fusket. I kveld har vi testet litt
kombinasjon av brikker og bestilt nye.

# Oppgradring av App-server
Kloke av skade startet vi oppgradering av app-server tidlig denne gangen.
Oppgradering av Ubuntu fra 14.04.3 til 15.10. Dette som forventet ikke helt
glatt og vi endte opp med en ny innstallasjon i stedet.

Med blanke dataark flyttet vi Postres fra / til /srv.

# Fornyelse av app-deployment
I forbindelse med oppgraderingen av Anne Frank ble vi tvunget til å vurderere
oppgradering/utfasing av Dokku som deployment-plattform. Konklusjonen ble å
oppgradere Dokku til 0.4.5, og å vurdere å bytte til Deis på sikt. Pushing til
app.iterate.no funker som før, men om man vil SSH-e inn må man kontakte Ops.

Vi har gått fra AUFS til OverlayFS som storage backend til Docker.

# Sky-boks til Røde Kors
Vi satt i gang arbeidet med å opprette en server til Røde Kors-prosjektet hos
Linode.

# Brukere
I tillegg til kraftig opprydding i brukere har vi onboardet vår nyeste operatør
Sindre Johansen!
