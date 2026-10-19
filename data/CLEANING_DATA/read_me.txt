RENGOERINGSDATA
===============

RENGOERINGSDATA - FORDELING 70 / 15 / 15

Enhed: cases, afventer data
training   : 0 (afventer data) - udvikling og træning
validation : 0 (afventer data) - valg af indstillinger
test       : 0 (afventer data) - afsluttende evaluering
Total      : 0

Der er ingen rengøringsdata endnu. De tre mapper er pladsholdere.

HVOR FINDER JEG DATAENE?

- raw/: plads til den endnu ikke leverede kildefil.
- training/, validation/ og test/: tomme mapper, klar til kommende 70/15/15-opdeling.
Case-id, aktivitetskolonne og tidsstempler skal afklares, før rengøringsdata kan konverteres og opdeles.

Denne read_me.txt er datasættets eneste forklarende tekstfil og dækker også alle undermapper.
Datafilerne kan indlæses direkte; der kræves ikke nogen opsætningsscripts.

PLACERING I GITHUB-PROJEKTET

- Denne mappe skal ligge i projektets data/-mappe.
- Bevar data/.gitattributes; den angiver Git LFS for datafiler.
- Installer Git LFS og kør git lfs install i den lokale repository-klon,
  før filerne tilføjes med git add. Upload via git push, ikke browseren.
- Ingen data er fjernet for at komme under GitHubs filstørrelsesgrænser.
- Rengøringsdata er endnu ikke leveret; mapperne er pladsholdere.
- Aftal adgang og tilladelse med dataejeren, før data lægges på GitHub.
