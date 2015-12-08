# Rydding av serverrom
Vi har nå ryddet, og alt av utstyr og dingser er atter kategorisert og plassert i bokser i hylla. Nåde den som roter det til! 
Og da mener vi null nåde. Det skal så lite til. Bare det at noen kaster en liiten USB-kabel umotivert inn i hylla er det som skal til for at mayhem blir utløst.
Please da.

# Tilgjengelige skjermer
I ryddingen har vi også endelig fått oversikt over skjermer,
det finnes fire 27" og fem 24" som alle funker og er up for grabs. Send epost til ops@iterate.no om du vil ha.

# Datautstyr up for grabs
I tillegg har vi ryddet i gamle laptoper. Før vi sender dem til gjenvinning vil vi høre om noen er interessert i noen av dem. Diverse Macbooks med diverse mangler, to Sony Vaioer, en Mac Mini, en iMac og en Airport eXtreme. Det er nok fullt mulig å få iallefall to ganske greie laptoper ut av flere. Igjen, send epost til ops@iterate.no om du vil ha. Ellers blir det pælmet om to uker.

# Litt rydding i Kjellerlageret
Kjellerlageret har også fått en gjennomgang, og alt av IT-utstyr som vi inntil videre vil spare på er samlet inne i høyre hjørne. Vi har ikke funnet noen prosjektorer (fra BA21), men to mikrofoner ligger nå sammen med videokameraet i en svart veske inne på serverrommet.

# Docker/Dokku-oppgradering
Ellers har vi oppgradert Docker på app.iterate.no, noe som medførte kort nedetid på tjenestene våre (beklager manglende varsel, Rana!), og gjort litt vedlikehold på drifting av Digital Leksehjelp.

# Prosjektortesting
Prosjektoren i sonen har kjørt fint for oss i fem timer i strekk, så vi gjør ikke noe mer med denne inntil folk melder om mer problemer.

# Amazon S3 rydding
Vi har kvittet oss med Medialounge og Filtermagasin buckets.

# Post Mortem Docker/Dokku-oppgradering
Som vanlig startet vi oppgradering for sent. Dette har vi vært gjennom
før og vi burde lære det snart. Oppgradering burde være første post
for kvelden.

Docker hadde byttet APT repo og navn på pakkene. Oddmund fant en fin
artikkel om dette, og det bø på ca. ingen problemer å endre på dette i
vårt oppsett.

Dokku har byttet fra bygging fra source til deb pakker, og har
tydeligvis et apt repo en eller annen plass. Vi prøde å følge
oppgraderingsinnstruksjonene, og vi fikk oppgradert dokku, men det ble
ikke lagt inn deb pakker. Litt suboptimalt, men vi kjører iallefall
siste versjon!

Så det som gikk galt: pluginarkitekturen til dokku har endret seg.
Våre fine plugins som gir containerne en mappe som lagres persistent
fungerte plutselig ikke lenger. Men med en god del gaffa fikk vi
plastret nok over sårene til at pluginene igjen kjørte.

Vi fikset kun pluginen som gjør en persistent mappe tilgjengelig. Vi
fikset ikke den som oppretter mappen når man laster opp nye apps. Vi
fikset heller ikke pluginen som lager postgresdatabase til nye apps.

Noen™ burde ta en ordentlig ryddesjau og
 - bytte ut persistent-storage pluginen med "docker dokku options" pluginen
 - se om docker dokku options kan opprette mapper on deploy, hvis
ikke, rydde i vår egen create-storage
 - bytte ut eller rydde i postgres pluginen vår
 - ... andre plugins vi har???
 - installere dokku med apt, så slipper vi å bygge fra source

Bleeding edge er gøy.

