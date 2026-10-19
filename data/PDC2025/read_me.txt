PDC2025
=======

PDC2025 - FORDELING 70 / 15 / 15

Enhed: modelkonfigurationer
training   : 67 (69.79 %) - udvikling og træning
validation : 14 (14.58 %) - valg af indstillinger
test       : 15 (15.62 %) - afsluttende evaluering
Total      : 96

Modelkonfigurationer holdes samlet: tre discoverylogs, testlog, base-log, facitlog og reference-Petri-net.
discovery/*00.xes: støjfri; *10.xes: støj; *11.xes: støj og præklassifikationer.
evaluation/ground_truth indeholder facit til sammenligning af test- og base-traces.
96 konfigurationer deler én basismodel; de er ikke 96 uafhængige procesfamilier.

HVOR FINDER JEG DATAENE?

- training/, validation/ og test/: hver indeholder mapper med modelkonfigurationer pdc2025_ABCDEF.
Inde i hver modelmappe:
  discovery/*00.xes: støjfri discoverylog med 1.000 traces.
  discovery/*10.xes: støjende discoverylog med 1.000 traces.
  discovery/*11.xes: støjende discoverylog med præklassificerede traces.
  reference/*.pnml: kendt genererende Petri-net.
  evaluation/test/*.xes: officiel testlog.
  evaluation/base/*.xes: officiel sammenligningslog.
  evaluation/ground_truth/*.xes: facit til sammenligning af test- og base-traces.

Det ydre training/validation/test bestemmer VORES split. Den indre evaluation/test er en rolle i PDC-protokollen.
Facit og reference-Petri-net må ikke utilsigtet blive input til discovery/GNN.
- raw/: udgiverens originale ZIP-arkiver; de omfatter alle splits.
- metadata/model_splits.json: konfigurationernes splitmedlemskab.
- metadata/inventory.json: hver fils placering og rolle.
UDGIVERENS ORIGINALE README (samlet her, så der kun er én tekstfil):

This folder contains the data set as was used for the Process Discovery Contest of 2025 (PDC 2025).
The data set contains 288 training logs, 96 corresponding test logs and base logs, 96 corresponding
ground truth logs, and 96 models. The logs are all stored using the IEEE XES file format (see either
 https://www.xes-standard.org/ or https://ieeexplore.ieee.org/document/7740858), while the models are
workflow nets (a subclass of Petri nets) stored in the PNML fileformat (see 
https://www.iso.org/obp/ui/#iso:std:iso-iec:15909:-2:ed-1:v1:en).

The data set is generated from a single base model that allows for the following characteristics A-H 
to be configured:

A: Dependent tasks, also known as long-term dependencies. Possible values are 0 for No and 1 for Yes. 
If Yes then all transitions that bypass the dependent tasks are disabled.

B: Loops. Possible values are 0 for No, 1 for Simple, and 2 for Complex. If No, then all transitions 
that start a loop are disabled. If Simple, then all transitions that are a shortcut between the loop 
and the main flow are disabled.

C: OR constructs. Possible values are 0 for No and 1 for Yes. If No, then all transitions that only 
take some inputs for an OR-join and all transitions that generate only some outputs for an OR-split
are disabled.

D: Routing constructs, also known as invisible tasks. Possible values are 0 for No and 1 for Yes. If 
Yes, then some transitions are made invisible.

E: Optional tasks. Possible values are 0 for No and 1 for Yes. If Yes, then some invisible transitions 
are added to allow skipping of some (visible) transitions.

F: Duplicate tasks, also known as recurrent activities. Possible values are 0 for No and 1 for Yes. 
If Yes, then some transitions are relabeled to existing labels.

G: Noise. Possible values are:
   0: no noise,
   1: in every trace with probability 20% either one random event
      is removed (40%), moved (20%), or copied (40%),

H: Pre-classified traces. Possible values are 0 for No and 1 for Yes. If Yes, then 20 positive traces are already classified as positive (“pdc:isPos” attribute has value true), and (if possible) 20 negative traces are also classified as negative (“pdc:isPos” attribute has value false). If Yes, G has to be 1 (there needs to be noise to classify traces as negative). 

The models and logs were generated in the following way from the base model. For all 96 possible 
values for A-F, the corresponding model pdc2025_ABCDEF.pnml is generated from the base model. From
every model pdc2025_ABCDEF.pnml, six logs are generated:
 (1) a noise-free training log pdc2025_ABCDEF00.xes containing 1000 traces,
 (2) a noisy training log pdc2025_ABCDEF10.xes containing 1000 traces,
 (3) a noisy and pre-classified training log pdc2025_ABCDEF11.xes containing 1000 traces,
 (4) a test log pdc2025_ABCDEF.xes containing 1000 traces,
 (5) a base log pdc2025_ABCDEF.xes containing 1000 traces, and
 (6) a ground truth log pdc2025_ABCDEF.xes that results from classifying the test log 
pdc2025_ABCDEF.xes and the base log pdc2025_ABCDEF.xes using the model pdc2025_ABCDEF.pnml. In each 
ground truth log, the additional boolean “pdc:isPos” attribute denotes whether the corresponding 
trace of the test log fits the model better than the corresponding trace from the base log. Of the 
1000 traces in the test log, 500 fit the corresponding trace in the base log better. 


KILDER OG DOKUMENTATION
metadata/sources.json: udgiverens filnavne, downloadadresser, størrelser og checksums for de oprindelige downloads.
metadata/source_pages/: gemte originale websider med datasætbeskrivelse og licensoplysninger.
Kildemanifestet beskriver de oprindelige downloads; PDC-udgiverens readme.txt er nu indarbejdet i denne read_me.txt.

Eric Verbeek (2025): Process Discovery Contest 2025. Version 1. 4TU.ResearchData. dataset. https://doi.org/10.4121/7212a73a-1eac-4a08-8c01-973dca020822.v1


Denne read_me.txt er datasættets eneste forklarende tekstfil og dækker også alle undermapper.
Datafilerne kan indlæses direkte; der kræves ikke nogen opsætningsscripts.

