BPI2014
=======

BPI2014 - FORDELING 70 / 15 / 15

Enhed: cases
training   : 32631 (70.00 %) - udvikling og træning
validation : 6992 (15.00 %) - valg af indstillinger
test       : 6993 (15.00 %) - afsluttende evaluering
Total      : 46616

Hele cases er fordelt; ingen case overlapper inden for samme log.

Nye cases fra samme proces er ikke det samme som holdout af helt nye processer.

HVOR FINDER JEG DATAENE?

- training/log.xes: træningsdata (cirka 70 % af hele cases).
- validation/log.xes: valideringsdata (cirka 15 %).
- test/log.xes: testdata (cirka 15 %).
- training/samples/log.xes, validation/samples/log.xes og test/samples/log.xes: op til 1.000 cases fra netop det split.
- raw/: den komplette originale kildefil før opdeling.

Samples er delmængder af de fulde splits og må ikke tilføjes som ekstra cases.
raw indeholder også validation- og testcases og bruges derfor ikke som træningssplit.
Hele cases holdes samlet. Samme aktivitetssekvens kan godt forekomme i flere splits, når den stammer fra forskellige cases.
XES-loggenes oprindelige eventrækkefølge og attributter er bevaret.
- metadata/statistics.json: antal cases, events, aktiviteter og størrelsen på hvert split/sample.
- metadata/splits/*.csv: case-id, split og samplemedlemskab for hver case.

- processed/log.xes: hele CSV-kilden konverteret til XES, før opdeling.
Konvertering: Incident ID = case-id, IncidentActivity_Type = aktivitet, DateStamp = tidsstempel.
Datoer læses dag-måned-år; events sorteres efter tidspunkt med oprindelig rækkefølge ved ens tid. Ingen tidszone er tilføjet.

KILDER OG DOKUMENTATION
- metadata/sources.json: udgiverens filnavne, downloadadresser, størrelser og checksums for de oprindelige downloads.
- metadata/source_pages/: gemte originale websider med datasætbeskrivelse og licensoplysninger.
Kildemanifestet beskriver de oprindelige downloads.

van Dongen, Boudewijn (2014): BPI Challenge 2014: Activity log for incidents. Version 1. 4TU.ResearchData. dataset. https://doi.org/10.4121/uuid:86977bac-f874-49cf-8337-80f26bf5d2ef
