gummibaerchen
=============

Hier werden Daten über die statistische Verteilung der Farben in Gummibärchentüten gesammelt. Konkret werden Daten von den **HARIBO Fruchgummi - Goldbären 300g* gesammelt. Mithilfe dieser Daten lassen sich dann ausführliche Statistiken erstellen und es können genauere Aussagen getroffen werden.


### Repository Struktur
Die Repository Struktur ist in zwei große Bereiche aufgeteilt. Der Bereich `data` und `source`.

#### data
Hier werden alle Statistiken in .json Dateien gesammelt. Sie müssen in einer speziellen Struktur festgehalten werden, die hier später erläutert wird.

Das Format der einzelnen .json Dateien ist folgendermaßen aufgebaut:
```plain
{
    "lnr": "L493-104 12",
    "uid": "04109 00_49 19",
    "mhd": "04/2013",
    "counting": "13.01.2013",
    "bears": {
        "orange": 25,
        "pineapple": 24,
        "raspberry": 16,
        "strawberry": 23,
        "apple": 20,
        "lemon": 23
    }
}
```
Als Beispiel habe ich nun mal die erste Statistik genommen. Wir haben insgesamt 5 Paare die mit unterschiedlichen Daten befüllt werden. Am einfachsten ist das Eingeben einer Statistik, indem man die sample.json herunterlädt, die Daten eingibt, die Kommentare entfernt und dann speichert und einreicht.

##### Der Dateiname
Der Dateiname besteht aus der *L-Nummer* (lnr), wobei allerdings die Leerstelle aus technischen Gründen, durch einen Unterstrich ersetzt werden muss. Was genau die L-Nummer ist, ist weiter unten ausführlich erklärt.

##### lnr
Im lnr Feld wird die sogenannte L-Nummer aufgeschrieben. Die L-Nummer ist die fett und größer gedruckte Nummer über dem Mindeshaltbarkeitsdatum. Bitte darauf achten, dass die Nummer komplett mit Leerzeichen eingegeben wird.

##### uid
Die uid ist die einzigeartige ID, mit der sich jede Tüte identifizieren lässt. Sie setzt sich aus mehreren Bestandteilen zusammen: Zuerst kommt die Nummer die in der 1. Zeile des Aufdrucks steht mit Leerstellen. Danach folgt ein Unterstrich (_) und die zweite 4-stellige Nummer vor dem Mindesthaltbarkeitsdatum. 

In der folgenden Grafik ist das ganze nochmals verdeutlicht:

*Grafik folgt demnächst.*
##### mhd
Im Feld mhd wird das aufgedruckte Mindesthaltbarkeitsdatum, im aufgedruckten Format (MM/YYYY), angegeben.

##### counting
Hier wird das Datum eingefügt, an dem die Zählung durchgeführt wurde. Das Format muss DD.MM.YYYY lauten.

##### bears
Nun sind wir beim Hauptteil der Statistik angelangt, bei den verschiedenen "Bären". Wir haben bewusst die Geschmacksrichtungen als Kennzeichnung genommen um Umlaute und ähnliche Kennzeichen zu vermeiden.

Hier gilt folgende Zuordnung:
<table>
  <tr>
    <th>Farben</th>
    <td>orange</td>
    <td>weiß</td>
    <td>dunkelrot</td>
    <td>hellrot</td>
    <td>grün</td>
    <td>gelb</td>
  </tr>
  <tr>
    <th></th>
    <td>Orange</td>
    <td>Ananas</td>
    <td>Himbeere</td>
    <td>Erdbeere</td>
    <td>Apfel</td>
    <td>Zitrone</td>
  </tr>
  <tr>
    <th>Geschmacksrichtung (Englisch)</th>
    <td>Orange</td>
    <td>Pineapple</td>
    <td>Raspberry</td>
    <td>Strawberry</td>
    <td>Apple</td>
    <td>Lemon</td>
  </tr>
</table>

Hinter die jeweilige Geschmacksrichtung wird die Anzahl der Gummibärchen geschrieben. Bitte darauf achten das die Zahl *nicht* in Anführungszeichen eingeschlossen ist.


---

#### source
Hier finden sich in Unterverzeichnissen die verschiedenen Anwendungen oder Bibliotheken (Libaries). Das können Anwendungen sein die, die Daten auswerten, weiterverarbeiten oder das Erstellen einfacher gestalten.
Auch diese müssen spezielle Regeln einhalten die hier später dokumentiert werden.


### Mitmachen
Mitmachen ist nicht nur erlaubt, sondern sogar erwünscht. Egal ob als Programmierer oder als Statistiker der einfach manchmal,
ein Tüte zählt bevor er sie genießt. Wir freuen uns über Helfer, die die Statistik vergrößern.

Am einfachsten ist das Mitmachen, indem man das Repository forked, dann die Statistik einfügt und einen Pull Request an mich schickt.
Wem das zu kompliziert ist, kann mir auch eine E-Mail senden: *reflic{:at:}notesafe{:dot:}de*

### Lizenz
Die Statistiken und auch jeglicher Code ist frei verfügbar und kann für jegliche Zwecke verwendet werden.
**Ein Link auf dieses Repository ist bei Verwendung der Daten oder des Codes jedoch notwendig.**