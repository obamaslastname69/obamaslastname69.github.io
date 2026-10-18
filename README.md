# obamaslastname69.github.io

Dieses Repo hat nur einen Zweck: die Datei `.well-known/assetlinks.json`
an der **Wurzel der Domain** ausliefern.

Android prüft dort, ob die installierte App wirklich zu dieser Webseite
gehört. Liegt die Datei nicht an der Wurzel, zeigt die App oben eine
Browser-Adressleiste statt wie eine echte App auszusehen.

Unter `/Planer/` darf sie dafür nicht liegen — Android schaut immer nur
an der Wurzel nach.

Die `.nojekyll` muss bleiben: ohne sie überspringt GitHub Pages alle
Ordner, die mit einem Punkt beginnen, und `.well-known` käme nie an.

Der Fingerabdruck in der assetlinks.json gehört zum Signierschlüssel der
APK (`signing.keystore`). Wird die App je mit einem anderen Schlüssel
signiert, muss er hier mitgeändert werden.

## Planer.apk

Liegt hier, damit sie sich am Handy ueber eine kurze Adresse laden
laesst. Die Datei ist nur die Huelle um die Webseite - keine Daten und
keine Schluessel darin. Der Signierschluessel (signing.keystore) gehoert
NICHT hierher und darf nie ins Netz.

(Die frueher hier abgelegte Planer.apk war die TWA-Fassung. Sie braucht
Chrome als Motor und ist deshalb entfernt worden. Die gueltige App liegt
unter /Planer/app.apk und bringt ihren Motor selbst mit.)
