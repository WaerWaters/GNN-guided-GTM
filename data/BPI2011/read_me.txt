BPI2011
=======

BPI2011 - FORDELING 70 / 15 / 15

Enhed: cases
training   : 800 (69.99 %) - udvikling og træning
validation : 171 (14.96 %) - valg af indstillinger
test       : 172 (15.05 %) - afsluttende evaluering
Total      : 1143

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

KILDER OG DOKUMENTATION
- metadata/sources.json: udgiverens filnavne, downloadadresser, størrelser og checksums for de oprindelige downloads.
- metadata/source_pages/: gemte originale websider med datasætbeskrivelse og licensoplysninger.
Kildemanifestet beskriver de oprindelige downloads.

van Dongen, Boudewijn (2011): Real-life event logs - Hospital log. Version 1. 4TU.ResearchData. dataset. https://doi.org/10.4121/uuid:d9769f3d-0ab0-4fb8-803b-0d1120ffcf54

