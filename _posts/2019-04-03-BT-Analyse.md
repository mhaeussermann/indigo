---
title:  "Ein Stimmungsbild aus 28 Jahren Bundestag"
layout: post-graph
date:   2019-04-03 19:00:00 +0100
author: mhaeussermann
lang: de
ref: bt-überblick
tag: 
- Bundestag
- Diagramm
- Zwischenrufe
- Explorative Datenanalyse
blog: true
star: false
description: "Ein Stimmungsbild aus 28 Jahren Bundestag: Zwischenrufe, Beifall und Heiterkeit"
category: blog
---
Nachdem ich für den [Bau meines Zwischenrufe-Twitterbots]({% post_url 2019-03-24-BT-Botbau %}) einen Prozess konzeptioniert hatte, der aus PDFs von Plenarprotokolle extrahiert und abspeichert, ist mir aufgefallen, dass meine Recherche etwas oberflächlich war.

Was ich damit meine, ist nicht, dass die Protokolle keine gute Quelle gewesen wären, nein, was ich meine ist, dass ich übersehen hatte, dass der Bundestag im Bereich der Open Data recht gut aufgestellt ist. Ich hatte schlicht und einfach die Unterseite [Open Data](https://www.bundestag.de/services/opendata) des Bundestages übersehen. Es ist eine Quelle, die mir mein Vorgehen wohl deutlich erleichtert hätte, enthält sie doch "alle Drucksachen und Plenarprotokolle ab der 1. Wahlperiode sowie die Biografie-Daten der Abgeordneten seit 1949 als XML-Dateien".

Diese XML-Dateien sind sehr praktisch, gerade auch weil sie komplex ausgezeichnet sind und deshalb sehr präzise ausgewertet werden können. Es gibt sogar eine [vierzehnseitige Strukturdokumentation](https://www.bundestag.de/resource/blob/577234/f9159cee3e045cbc37dcd6de6322fcdd/dbtplenarprotokoll_kommentiert-data.pdf), dass alle Elemente erklärt, weswegen ich an dieser Stelle darauf verzichten kann. Puh! Von Interesse ist für mich natürlich insbesondere der Tag "kommentar", der nicht nur Zwischenrufe, sondern auch Beifall und Momente der Heiterkeit markiert – genauer: "Kommentare mit der Reaktion der Zuhörer".

Das Problem an dieser Auszeichnungsmethode ist – und dies ist ein oft genannter Grund gegen XML - ihre Aufwendigkeit. Das bedeutet: lediglich die Bundestagsprotokolle der aktuellen, 19. Wahlperiode nutzen die Möglichkeiten der XML-Struktur wirklich aus, um komplex Daten zu strukturieren. Alle Protokolle vorheriger Wahlperioden sind in einer Minimalform ausgezeichnet, folglich: Metadaten ja, Textstruktur nein.

Um also ein kurzes Stimmungsbild der 12. bis zur 18. Wahlperiode zu erhalten, kann nicht auf das XML-Markup zurückgegriffen werden. Einzig Metadaten über Wahlperiode, Sitzungsnummer und Datum können vereinfacht ausgelesen werden und die beiden ersteren sind bereits im Dateiname jedes Protokolls enthalten. Zudem bedeuten XML-Protokolle nicht, dass wir keine Probleme mit Silbentrennungen bekommen, denn diese sind auch hier enthalten.

Es scheint so, als seien die XML-Dateien - zumindest jene vor der aktuellen Wahlperiode - grundsätzlich auch nur konvertierte PDFs. Damit ist die Bereinigung zwar etwas leichter, ein vollständig sauberer Datensatz würde jedoch trotzdem einen nicht unerheblichen Aufwand erfordern, problematisch sind hauptsächlich Zwischenrufe, die über zwei Protokollseiten verlaufen.

Für die folgenden Überblicke über den Datensatz braucht es diesen Aufwand jedoch nicht, da lediglich Frequenzen gezählt und geplottet werden. Es geht mir um drei wesentliche Formen von "Kommentaren": Zwischenrufe, Beifall und Bekundungen von Heiterkeit. Mir geht es um einen groben Überblick über die Verteilung über fast dreißig Jahre, ich gehe daher explorativ vor. _Oh yeah_, eine Sache noch: Ich bin kein Statistiker, also kann es durchaus sein, dass ich in meinen Berechnungen Fehler gemacht habe.

## Wie oft wurde gelacht?
Durchschnittlich wurde zwischen 1990 und 2018 pro Sitzung 10.50 Mal gelacht, auch im Vergleich zwischen den verschiedenen Bundestagsperioden scheint der Wert zunächst stabil: Die 15. Wahlperiode stellt mit 8.59 Lachern pro Sitzung den niedrigsten Wert, den Höchstwert bilden 12.37 Lacher pro Sitzung während der 18. Wahlperiode.

Ein Scatterplot der Verteilungen offenbart jedoch, dass es große Abweichungen zwischen den Sitzungen gibt. Neben 78 Sitzung sehr ernsten Sitzungen ohne Heiterkeitsvermerken fallen insbesondere die Sitzungen 17/250, 18/11, 12/115, 12/6 und 13/31 auf, die 50 oder mehr Vermerke der Heiterkeit beinhalten. Die beiden ersten bilden mit 58 (17/250) respektive 57 (18/11) die Spitze. Die Standardabweichung über den gesamten analysierten Zeitraum beträgt entsprechend 8.86.

<div>
    <a href="https://plot.ly/~mhaeussermann/3/?share_key=4rcRWpyXaNGAlLHwduiKw4" target="_blank" title="Plot Heiterkeit" style="display: block; text-align: center;"><img src="https://plot.ly/~mhaeussermann/3.png?share_key=4rcRWpyXaNGAlLHwduiKw4" alt="Plot Heiterkeit" style="max-width: 100%;width: 600px;"  width="600" onerror="this.onerror=null;this.src='https://plot.ly/404.png';" /></a>
    <script data-plotly="mhaeussermann:3" sharekey-plotly="4rcRWpyXaNGAlLHwduiKw4&link=false" src="https://plot.ly/embed.js" async></script>
</div>

Bei der Betrachtung des Diagramms scheint es, als würde die Verteilung insbesondere in der 12. bis 14. Wahlperiode stark schwanken, was jedoch nicht notwendigerweise auf reale Inkonsistenzen in der Belustigung des Parlaments hindeuten muss, sondern auch auf unregelmäßige Sitzungslänge zurückzuführbar sein kann, eine Tatsache, die uns auch noch im folgenden begegnen wird. Dennoch zeigt der Plot, dass auch Krisensituation wie die Finanzkrise ab 2008 nicht zwangsläufig zu einer Trübung der Stimmung im Bundestag führen.

## Wie oft wurde zwischengerufen?
Der Deutsche Bundestag ist eine Mischung zwischen "Arbeitsparlament" und "Redeparlament". Ersterer Aspekt findet sich hauptsächlich in der Arbeit der verschiedenen Ausschüsse wieder, in denen alle Fraktion proportional vertreten sind. Die Plenarsitzungen und -debatten sind Teil des zweiten Aspekts, des Redeparlaments.

In der Politikwissenschaft ist die Ansicht weithin akzeptiert, dass der erste Aspekt, der meist abseits öffentlicher Beobachtung stattfindet, den Vorrang besitzt, wie etwa Manfred G. Schmidt argumentiert:

>Vom Vorrang des Arbeitsparlaments zeugt auch die Arbeitszeiteinteilung der Abgeordneten auf Kommiteearbeit und Debattentätigkeit. Den Großteil des Zeitbudgets im Parlament konsumiert die Teilnahme an Bundestagsausschusssitzungen. Der Vorrang des Arbeitsparlaments lässt sich zudem daran ablesen, dass das Plenum des Bundestags meist nur als Notar oder als Verkünder von Beschlüssen wirkt, die in den Parlamentsausschüssen und in informellen Abstimmungen zwischen Regierung, Fraktionen und Parteiführungen vorberaten oder schon entschieden wurden.[^fn1]

Gleichzeitig lässt sich der Deutsche Bundestag als Vertreter eines "kooperativen Parlamentarismus" beschreiben, in dem Regierung und Opposition zusammenarbeiten (müssen). Dies zeigt sich etwa in der konstitutionell notwendigen 2/3-Mehrheit für Verfassungsänderungen und im Aufbau der Ausschüsse.[^fn2] Während der 18. Wahlperiode war der erste Aspekt in gewisser Weise ausgehebelt, da die Regierungskoalition von Union und SPD 504 von 631 auf sich vereinigte und damit eine 2/3-Mehrheit für Beschlüsse besaß.

Was diese Prinzipien – die Mischung von Arbeits- und Redeparlament und der kooperative Parlamentarismus jedoch bedeuten, ist, dass es in Plenarsitzungen des Bundestages deutlich ruhiger zugeht als etwa im britischen oder US-amerikanischen Parlamentssystem, das weitaus kompetitiver angelegt ist. Dies ist ein Feature und kein Bug, stellt es doch eine Lehre aus dem Untergang der Weimarer Republik dar.

Warum diese lange Einleitung? Nun, angesichts dieser Überlegungen wäre anzunehmen, dass Zwischenrufe im Deutschen Bundestag eine relative Seltenheit darstellen. Die Daten zeigen etwas anderes: Zwischenrufe sind keine Seltenheit, sondern die Regel. Über den gesamten beobachteten Zeitraum lässt sich ein Wert von 240.32 Zwischenrufen pro Sitzung beschreiben. Die Standardabweichung beträgt 165.09. Die höchste durchschnittliche Anzahl an Zwischenrufen findet sich in der 17. Wahlperiode (328.45 Zwischenrufe), während die Sitzungen des 12. und 13. Bundestags durchschnittlich am wenigsten unterbrochen wurden (175.47 und 184.05  Zwischenrufe).

<div>
    <a href="https://plot.ly/~mhaeussermann/2/?share_key=gaXtaY6eYgvuFmP13q5aWg" target="_blank" title="Plot Zwischenrufe" style="display: block; text-align: center;"><img src="https://plot.ly/~mhaeussermann/2.png?share_key=gaXtaY6eYgvuFmP13q5aWg" alt="Plot Zwischenrufe" style="max-width: 100%;width: 600px;"  width="600" onerror="this.onerror=null;this.src='https://plot.ly/404.png';" /></a>
    <script data-plotly="mhaeussermann:2" sharekey-plotly="gaXtaY6eYgvuFmP13q5aWg&link=false" src="https://plot.ly/embed.js" async></script>
</div>

Im Plotdarstellung lassen sich insbesondere zwei Gruppen ausmachen: während in der ersten deutliche Abweichungen nach oben erkennen lassen, gemeint sind die 14., 15. und 17. Wahlperiode, sind die Datenpunkte der zweiten Gruppe gleichmäßiger verteilt und bleiben größtenteils um oder unter 500 Zwischenrufen (12. 13., 18. Wahlperiode). Zudem gibt es einen extremen Outlier innerhalb der 17. Wahlperiode: Sitzung 250 mit 1343 notierte Zwischenrufe. Um diese Sitzung wird es im letzten Abschnitt dieses Texts gehen.

Wie sich herausstellt, handelt es sich bei zweiterer Gruppe um die Kabinette Kohl IV und V sowie um das Kabinett Merkel III, also um Wahlperioden, in denen zugleich eine vergleichsweise starke Regierungskoalition (Kohl IV: 60%; Kohl V: 51%; Merkel III: 80%) bei gleichzeitig vergleichsweise lang andauernder Regierungszeit eines/r einzigen KanzlerIn gegeben sind. Auch die 16. Wahlperiode ist arm an großen Ausschlägen in der Anzahl der Zwischenrufe, aber hier ist immerhin eines der beiden Kriterien gegeben, nämlich die Dominanz der Regierungskoalition. Ganze 73% der Sitze im Bundestag wurden während des Kabinetts Merkel I von Repräsentanten der Großen Koalition besetzt.

## Wie oft wurde applaudiert?
Verglichen mit der geplotteten Verteilung der Zwischenrufe wirkt der Graph zur Verteilung von Applaus deutlich innerhalb der Wahlperioden konsistenter, erkennbar ist ein Anstieg des Applauses in frühen und späten Sitzungen einer Wahlperiode. Von den 20 Sitzungen mit den meisten markierten Applausmomenten befinden sich 7 innerhalb der ersten 50 Sitzungen und 7 innerhalb der letzten 50 Sitzungen der jeweiligen Wahlperiode.

<div>
    <a href="https://plot.ly/~mhaeussermann/4.embed" target="_blank" title="Plot Beifall" style="display: block; text-align: center;"><img src="https://plot.ly/~mhaeussermann/4.png?share_key=gaXtaY6eYgvuFmP13q5aWg" alt="Plot Beifall" style="max-width: 100%;width: 600px;"  width="600" onerror="this.onerror=null;this.src='https://plot.ly/404.png';" /></a>
    <script data-plotly="mhaeussermann:4" sharekey-plotly="gaXtaY6eYgvuFmP13q5aWg&link=false" src="https://plot.ly/embed.js" async></script>
</div>

Die Wahlperiode mit dem durchschnittlich höchsten Applauswert ist die 18. mit 378.72 mal Applaus pro Sitzung, der niedrigste Wert ist in der 12. Wahlperiode zu finden: 219 mal Applaus pro Sitzung. Der Durchschnitt über alle Wahlperioden gerechnet beträgt 325.58, wobei dieser Wert jedoch maßgeblich durch die 16. bis 18. Wahlperiode beeinflusst wird. Die Standardabweichung beträgt 224.46 und fällt damit erstaunlicherweise höher aus als im Fall der Zwischenrufe. Die insgesamte Zunahme an Applaushäufigkeit über den Verlauf der beobachteten Wahlperioden lässt sich auch an der Plotchart erkennen. Auch hier ist wiederum ein extremer Ausbrecher nach oben zu erkennen, erneut ist es Sitzung 17/250.

## Eine ungewöhnliche Sitzung
Sitzung 17/250 ist so etwas wie der weiße Wa(h)l unter den Bundestagssitzungen, zumindest innerhalb des untersuchten Zeitraums. Allein das Inhaltsverzeichnis aller Tagesordnungspunkte und Zusatztagesordnungspunkte sowie Anlagen umfasst 33 Seiten, insgesamt breitet sich das Protokoll auf 620 Seiten aus. Ein Roman von einer Sitzung, der um 9:02 Uhr morgens am 27. Juni 2013 beginnt und um 0:51 Uhr am 28. Juni 2013 geschlossen wird. Die Sitzungszeit beträgt fast 16 Stunden. Zum Vergleich: Vierzehnstündige Sitzungen kommen vor, wenn auch selten, wie etwa 17/211 oder 18/11, aber, so weit ich das ersehen kann, ist dies die längste Sitzung, zumindest zwischen 1990 und 2018.[^fn3] Bundestagspräsident Dr. Norbert Lammert beginnt die Sitzung bereits mit einem leicht ironischen Unterton.

<div style="text-align:center"><img alt="17. Wahlperiode, S. 31877" src ="{{site.url}}{{site.baseurl}}/assets/images/bt/bt_1.png" /></div>
Beginn der Sitzung 17/250
{: style="color:gray; font-size: 80%; text-align: center;"}

Beim ersten Überfliegen der Tagesordnung und des Protokolls sind mir keine besonderen Gründe aufgefallen, warum diese Sitzung so absonderlich lang ausfiel. Weder wurde ein Thema besonders lang und kontrovers besprochen, noch handelte es sich um eine Krisensitzung wie etwa die 248. Sitzung, die angesichts des Hochwassers 2013 einberufen wurde.

Zugegeben, einige Themen wurden ausführlicher besprochen als andere, etwa die Debatte zu einer Beschlussempfehlung einer Pflegereform der SPD, die 1 Stunde 45 Minuten in Anspruch nimmt, die Beratung mehrerer Vorlagen zum Verbraucherschutz mit 1 Stunde 47 Minuten oder auch die Regierungserklärung zum G8-Gipfel und Europäischem Rat mit 2 Stunden 17 Minuten, die gleichzeitig auch eine Debatte zum möglichen Eintritt Serbiens in die EU beinhaltet.

<div style="text-align:center"><script id="tv2478144" src="https://webtv.bundestag.de/player/macros/bttv/hls/player.js?content=2478144&phi=default"></script></div>
Vollständige Videoaufzeichnung der Sitzung 17/250
{: style="color:gray; font-size: 80%; text-align: center;"}

Aber insgesamt scheint für die Länge der Sitzung zunächst die Menge der abzuarbeitenden Tagesordnungspunkte entscheidend gewesen zu sein. Es gab einfach viel zu besprechen und Reden zu halten. Um die Frage zu beantworten, ob und was diese Bundestagssitzung besonders gemacht hat beziehungsweise wie es zu der thematischen Überladung kam, muss man qualitativ vorgehen, nicht quantitativ. Falls ich Zeit dazu finde, lese ich mich vielleicht mal durch die 620 Protokollseiten.

---
[^fn1]: Schmidt, Manfred G.: _Das politische System Deutschlands_, 2. überarbeitete, aktualisierte und erweiterte Ausgabe, München 2011, S. 152.
[^fn2]: Ebd., S. 155f.
[^fn3]: Eine Suche nach der längsten Bundestagssitzung erbringt gehäuft Ergebnisse, die Sitzung 17/237 als "längste Bundestagssitzung" bezeichnen. Dies stimmt nur zum Teil: Zwar wurde die Sitzung erst gegen 2 Uhr beendet, wegen einer Unterbrechung liegt jedoch die Gesamtsitzungszeit lediglich bei 14 Stunden 33 Minuten und damit deutlich unter den 16 Stunden der Sitzung 17/250.
