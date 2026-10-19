BPI2015
=======

BPI2015 - FORDELING 70 / 15 / 15

Enhed: cases
training   : 3953 (69.98 %) - udvikling og træning
validation : 844 (14.94 %) - valg af indstillinger
test       : 852 (15.08 %) - afsluttende evaluering
Total      : 5649

Hele cases er fordelt; ingen case overlapper inden for samme log.

Nye cases fra samme proces er ikke det samme som holdout af helt nye processer.
bpi2015_municipality_1: training=839, validation=179, test=181
bpi2015_municipality_2: training=582, validation=124, test=126
bpi2015_municipality_3: training=986, validation=211, test=212
bpi2015_municipality_4: training=737, validation=157, test=159
bpi2015_municipality_5: training=809, validation=173, test=174

HVOR FINDER JEG DATAENE?

- training/kommune_1/log.xes ... kommune_5/log.xes: træningscases pr. kommune.
- validation/kommune_1/log.xes ... kommune_5/log.xes: valideringscases pr. kommune.
- test/kommune_1/log.xes ... kommune_5/log.xes: testcases pr. kommune.
Under hver kommune og hvert split findes samples/log.xes med op til 1.000 cases.
- raw/kommune_1/ ... kommune_5/: komplette originale eventlogs.

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

van Dongen, Boudewijn (2015): BPI Challenge 2015 Municipality 1. Version 1. 4TU.ResearchData. dataset. https://doi.org/10.4121/uuid:a0addfda-2044-4541-a450-fdcc9fe16d17

van Dongen, Boudewijn (2015): BPI Challenge 2015 Municipality 2. Version 1. 4TU.ResearchData. dataset. https://doi.org/10.4121/uuid:63a8435a-077d-4ece-97cd-2c76d394d99c

van Dongen, Boudewijn (2015): BPI Challenge 2015 Municipality 3. Version 1. 4TU.ResearchData. dataset. https://doi.org/10.4121/uuid:ed445cdd-27d5-4d77-a1f7-59fe7360cfbe

van Dongen, Boudewijn (2015): BPI Challenge 2015 Municipality 4. Version 1. 4TU.ResearchData. dataset. https://doi.org/10.4121/uuid:679b11cf-47cd-459e-a6de-9ca614e25985

van Dongen, Boudewijn (2015): BPI Challenge 2015 Municipality 5. Version 1. 4TU.ResearchData. dataset. https://doi.org/10.4121/uuid:b32c6fe5-f212-4286-9774-58dd53511cf8


