---
title:  "Ein Stimmungsbild aus 28 Jahren Bundestag"
layout: post-graph
date:   2019-03-29 19:00:00 +0100
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
description: "Ein Stimmungsbild aus 28 Jahren Bundestag: Über Zwischenrufe, Beifall und Heiterkeit"
category: blog
---
Nachdem ich für den [Bau meines Zwischenrufe-Twitterbots]({% post_url 2019-03-24-BT-Botbau %}) einen Prozess konzeptioniert hatte, der aus PDFs von Plenarprotokolle extrahiert und abspeichert, ist mir aufgefallen, dass meine Recherche etwas oberflächlich war.

Was ich damit meine, ist nicht, dass die Protokolle keine gute Quelle gewesen wären, nein, was ich meine ist, dass ich übersehen hatte, dass der Bundestag im Bereich der Open Data recht gut aufgestellt ist. Ich hatte schlicht und einfach die Unterseite [Open Data](https://www.bundestag.de/services/opendata) des Bundestages übersehen. Es ist eine Quelle, die mir mein Vorgehen wohl deutlich erleichtert hätte, enthält sie doch "alle Drucksachen und Plenarprotokolle ab der 1. Wahlperiode sowie die Biografie-Daten der Abgeordneten seit 1949 als XML-Dateien".

Diese XML-Dateien sind sehr praktisch, gerade auch weil sie komplex ausgezeichnet sind und deshalb sehr präzise ausgewertet werden können. Es gibt sogar eine [vierzehnseitige Strukturdokumentation](https://www.bundestag.de/resource/blob/577234/f9159cee3e045cbc37dcd6de6322fcdd/dbtplenarprotokoll_kommentiert-data.pdf), dass alle Elemente erklärt, weswegen ich an dieser Stelle darauf verzichten kann. Puh! Von Interesse ist für mich natürlich insbesondere der Tag "kommentar", der nicht nur Zwischenrufe, sondern auch Beifall und Momente der Heiterkeit markiert – genauer: "Kommentare mit der Reaktion der Zuhörer".

Das Problem an dieser Auszeichnungsmethode ist – und dies ist ein oft genannter Grund gegen XML - ihre Aufwendigkeit. Das bedeutet: lediglich die Bundestagsprotokolle der aktuellen, 19. Wahlperiode nutzen die Möglichkeiten der XML-Struktur wirklich aus, um komplex Daten zu strukturieren. Alle Protokolle vorheriger Wahlperioden sind in einer Minimalform ausgezeichnet, folglich: Metadaten ja, Textstruktur nein.

Um also ein kurzes Stimmungsbild der 12. bis zur 18. Wahlperiode zu erhalten, kann nicht auf das XML-Markup zurückgegriffen werden. Einzig Metadaten über Wahlperiode, Sitzungsnummer und Datum können vereinfacht ausgelesen werden und die beiden ersteren sind bereits im Dateiname jedes Protokolls enthalten. Zudem bedeuten XML-Protokolle nicht, dass wir keine Probleme mit Silbentrennungen bekommen, denn diese sind auch hier enthalten.

Es scheint so, als seien die XML-Dateien - zumindest jene vor der aktuellen Wahlperiode - grundsätzlich auch nur konvertierte PDFs. Damit ist die Bereinigung zwar etwas leichter, ein vollständig sauberer Datensatz würde jedoch trotzdem einen nicht unerheblichen Aufwand erfordern, problematisch sind hauptsächlich Zwischenrufe, die über zwei Protokollseiten verlaufen.

Für die folgenden Überblicke über den Datensatz braucht es diesen Aufwand jedoch nicht, da lediglich Frequenzen gezählt und geplottet werden. Es geht mir um drei wesentliche Formen von "Kommentaren": Zwischenrufe, Beifall und Bekundungen von Heiterkeit. Mir geht es um einen groben Überblick über die Verteilung über fast dreissig Jahre, ich gehe daher explorativ vor. _Oh yeah_, eine Sache noch: Ich bin Statistiker, also kann es durchaus sein, dass ich in meinen Berechnungen Fehler gemacht habe.

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

Gleichzeitig lässt sich der Deutsche Bundestag als Vertreter eines "kooperativen Parlamentarismus" beschreiben, in dem Regierung und Opposition zusammenarbeiten (müssen). Dies zeigt sich etwa in der konstitutionell notwendigen 2/3-Mehrheit für Verfassungsänderungen und im Aufbau der Ausschüsse.[^fn2] Während der 18. Wahlperiode war der erste Aspekt in gewisser Weise ausgehebelt, da die Regierungskoalition von Union und SPD 504 von 631 auf sich vereinigte und damit eine 2/3-Mehrheit für Beschlüsse besass.

Was diese Prinzipien – die Mischung von Arbeits- und Redeparlament und der kooperative Parlamentarismus jedoch bedeuten, ist, dass es in Plenarsitzungen des Bundestages deutlich ruhiger zugeht als etwa im britischen oder US-amerikanischen Parlamentssystem, das weitaus kompetitiver angelegt ist. Dies ist ein Feature und kein Bug, stellt es doch eine Lehre aus dem Untergang der Weimarer Republik dar.

Warum diese lange Einleitung? Nun, angesichts dieser Überlegungen wäre anzunehmen, dass Zwischenrufe im Deutschen Bundestag eine relative Seltenheit darstellen. Die Daten zeigen etwas anderes: Zwischenrufe sind keine Seltenheit, sondern die Regel. Über den gesamten beobachteten Zeitraum lässt sich ein Wert von 240.32 Zwischenrufen pro Sitzung beschreiben. Die Standardabweichung beträgt 165.09. Die höchste durchschnittliche Anzahl an Zwischenrufen findet sich in der 17. Wahlperiode (328.45 Zwischenrufe), während die Sitzungen des 12. und 13. Bundestags durchschnittlich am wenigsten unterbrochen wurden (175.47 und 184.05  Zwischenrufe).

<div>
    <a href="https://plot.ly/~mhaeussermann/2/?share_key=gaXtaY6eYgvuFmP13q5aWg" target="_blank" title="Plot Zwischenrufe" style="display: block; text-align: center;"><img src="https://plot.ly/~mhaeussermann/2.png?share_key=gaXtaY6eYgvuFmP13q5aWg" alt="Plot Zwischenrufe" style="max-width: 100%;width: 600px;"  width="600" onerror="this.onerror=null;this.src='https://plot.ly/404.png';" /></a>
    <script data-plotly="mhaeussermann:2" sharekey-plotly="gaXtaY6eYgvuFmP13q5aWg&link=false" src="https://plot.ly/embed.js" async></script>
</div>

Im Plotdarstellung lassen sich insbesondere zwei Gruppen ausmachen: während in der ersten deutliche Abweichungen nach oben erkennen lassen, gemeint sind die 14., 15. und 17. Wahlperiode, sind die Datenpunkte der zweiten Gruppe gleichmäßiger verteilt und bleiben größtenteils um oder unter 500 Zwischenrufen (12. 13., 18. Wahlperiode). Zudem gibt es einen extremen Outlier innerhalb der 17. Wahlperiode: Sitzung 250 mit 1343 notierte Zwischenrufe. Um diese Sitzung wird es im letzten Abschnitt dieses Texts gehen.

Wie sich herausstellt, handelt es sich bei zweiterer Gruppe um die Kabinette Kohl IV und V sowie um das Kabinett Merkel III, also um Wahlperioden, in denen zugleich eine vergleichsweise starke Regierungskoalition (Kohl IV: 60%; Kohl V: 51%; Merkel III: 80% [!sic]) bei gleichzeitig vergleichsweise lang andauernder Regierungszeit eines/r einzigen KanzlerIn gegeben sind. Zwar ist auch 16. Wahlperiode.

## Wie oft wurde applaudiert?

<div>
    <a href="https://plot.ly/~mhaeussermann/4.embed" target="_blank" title="Plot Beifall" style="display: block; text-align: center;"><img src="https://plot.ly/~mhaeussermann/4.png?share_key=gaXtaY6eYgvuFmP13q5aWg" alt="Plot Beifall" style="max-width: 100%;width: 600px;"  width="600" onerror="this.onerror=null;this.src='https://plot.ly/404.png';" /></a>
    <script data-plotly="mhaeussermann:4" sharekey-plotly="gaXtaY6eYgvuFmP13q5aWg&link=false" src="https://plot.ly/embed.js" async></script>
</div>

## Der Outlier aller Outlier

<script id="tv2478144" src="https://webtv.bundestag.de/player/macros/bttv/hls/player.js?content=2478144&phi=default"></script>

---
[^fn1]: Schmidt, Manfred G.: _Das politische System Deutschlands_, 2. überarbeitete, aktualisierte und erweiterte Ausgabe, München 2011, S. 152.
[^fn2]: Ebd., S. 155f.
