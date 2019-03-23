---
title: "Geisteswissenschaften auf Twitter: #twitterphilologie"
layout: post
date: 2018-12-05 18:00
tag:
- Digital Humanities
- Twitter
- Soziale Netzwerkanalyse
lang: de
ref: twitterphilologie
star: false
category: blog
author: mhaeussermann
description: Literaturwissenschaftliche Kommunikation und Communities auf Twitter
---

In den letzten Monaten scheint Twitter als Kommunikationsmittel zunehmend auch in der deutschen Wissenschaftslandschaft Fuß zu fassen. Die Beobachtung, Twitter sei heute auch "ein Ort für Bildungsreisende", die [Jörg Scheller](https://twitter.com/joergscheller1) und [Wolfgang Ullrich](https://twitter.com/ideenfreiheit) Anfang des Jahres in der Zeit beschrieben haben ([Link](https://www.zeit.de/2018/22/twitter-tweets-intellektuelle-philosophie-diskurs-debatte/komplettansicht)), deckt sich mit meinen eigenen Erfahrungen.

In letzter Zeit bemerke und folge ich auf Twitter verstärkt GeisteswissenschaftlerInnen, darunter vornehmlich Literatur- und KulturwissenschaftlerInnen, die sich in Kurzform mit ihrem Fachgebiet und -gegenstand, Feuilletondebatten oder aktuellen Ereignissen auseinandersetzen. Immer wieder kommt es zu Diskussionen, die sich teilweise in weitläufige und trotzdem kurzweilige Threads ausbreiten.

Eines macht sich dabei schnell bemerkbar: Der Austausch innerhalb der geisteswissenschaftlichen Community auf Twitter ist deutlich zwangloser als in akademischen Veranstaltungen und ist oft von einem ironischen Ton begleitet. Der/die AkademikerIn will zumeist Meinungen vertreten oder unterhalten und nicht dozieren.
Es ist eine sehr erfreuliche Entwicklung, wie ich finde, wird doch Wissenschaftskommunikation bisher in vielen geisteswissenschaftlichen Fakultäten wenig thematisiert, Twitter wird im Betrieb noch vielfach kritisch beäugt:

<blockquote class="twitter-tweet" data-lang="en"><p lang="de" dir="ltr">Reaktionen auf <a href="https://twitter.com/hashtag/TwitterPhilologie?src=hash&amp;ref_src=twsrc%5Etfw">#TwitterPhilologie</a> Große Irritation und Anlass für lange enthusiastische kulturkritische Diagnosen... die meist in ein Loblied auf die Haptik des Buches münden.</p>&mdash; JohannesFranzen (@Johannes42) <a href="https://twitter.com/Johannes42/status/1001150069570265089?ref_src=twsrc%5Etfw">May 28, 2018</a></blockquote>
<script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

Jedoch ist es nicht nur eine verstärkte Kommunikation nach außen, die durch Twitter ermöglicht werden kann. [Stephan Poromba](https://twitter.com/stporombka) hat in einem [Interview mit dem Deutschlandfunk](https://www.deutschlandfunkkultur.de/twitternde-akademiker-der-blick-in-die-feeds-der-philologen.976.de.html?dram:article_id=421961) schön beschrieben, wie die Kommunikation und Interaktion über soziale Medien die geistes- bzw. literaturwissenschaftliche Arbeit bereichern kann:
> „Klar, ich kann wenig schreiben, wichtig ist aber: ich vernetzte mich. Ich kann bestimmen, wen ich noch lese, ich kann mir eine ganze Leseliste zusammenstellen und diese Leseliste wird dauernd aktualisiert. Ich kann richtige Werkstätten mir aufbauen, wo ich dauernd mit dem versorgt werde, was ich brauche – und ich tauche in den Feeds von anderen auf, wenn sie mich lesen wollen, also das heißt: nicht nur die beliefern mich, sondern auch ich beliefer‘ sie. Und jetzt kommt aber noch was drittes hinzu: wir können miteinander in Kontakt treten. Wir können unmittelbar darauf reagieren, was wir da gerade sehen, was reinkommt.“ 

Je nachdem, wie man Twitter nutzt, ist es durchaus geeignet, Denkprozesse zu unterstützen und Gedanken voranzutreiben, denn Denken passiert nicht allein im eigenen Kopf, sondern maßgeblich im Austausch mit anderen. Ich habe selbst häufig die Erfahrung gemacht, dass ich durch meine Timeline auf Ideen und Beiträge stoße, die mich nachhaltig beeindrucken und faszinieren.

Unter Hashtags wie #TwitterPhilologie, #DarumGW oder #RelevanteLiteraturwissenschaft bilden sich Diskussionsräume, in denen die Geisteswissenschaften beziehungsweise insbesondere die Literaturwissenschaften und ihre Stellung in der modernen Gesellschaft wie im digitalen Kontext verhandelt werden. Es stellt sich jedoch die Frage, ob mit der Nutzung von Twitter zwangsläufig eine Öffnung der Geisteswissenschaften einhergeht. Gerade @mianjanssens Blogbeitrag über [Ein- und Ausschlussverfahren geisteswissenschaftlicher Communities](https://buechnerwald.wordpress.com/2018/11/16/elitaere-gruppenbildung-in-den-online-geisteswissenschaften/) hat diesbezüglich Zweifel angemeldet.

## #Twitterphilologie
Um das _community building_ insbesondere der LiteraturwissenschaftlerInnen auf Twitter besser zu verstehen, greife ich im Folgenden auf eine mittlerweile weitverbreitete Methode zur Analyse für Soziale Netzwerke zurück, die Soziale Netzwerkanalyse (SNA). Hierbei werden die Akteure des Netzwerks als Knoten dargestellt und ihre Interaktionen durch Kanten.

Twecoll wird genutzt um Tweets, ihre Urheber und deren Followings und alle Followings der Follower zu extrahieren und nach Freundschaftsbeziehungen zu suchen. Das jeweilige Ergebnis wird daraufhin in Gephi visualisiert. Hilfreich für die Datensammlung und -visualisierung mit [Twecoll](https://github.com/jdevoo/twecoll) und [Gephi](https://gephi.org/) waren die Blogbeiträge [How to collect any Twitter follower network with the Python script twecoll](https://medium.com/@Luca/how-to-collect-any-twitter-follower-network-with-the-python-script-twecoll-c482eeb61f77) und [Guide: Analyzing Twitter Networks with Gephi 0.9.1](https://medium.com/@Luca/guide-analyzing-twitter-networks-with-gephi-0-9-1-2e0220d9097d) von Luca Hammer. 

Ich möchte jedoch zunächst bekräftigen, was er in seinem Artikel zum Ausdruck bringt: "Network visualization is messy". Es gibt nicht _die_ Visualisierung von Netzwerken, es ist ein Prozess, in dem man ausprobieren muss, welche Einstellungen passen könnten. Zudem bin ich kein Experte in der Theorie und Praxis sozialer Netzwerke, ich bitte also darum, meine Interpretationen mit einem _grain of salt_ zu nehmen.

![Abb. 1]({{site.url}}{{site.baseurl}}/assets/images/twitterphilologie/hashtagtwitterphilologie(alt).png)
Abb. 1: #twitterphilologie (Stand: 16. November).
{: style="color:gray; font-size: 80%; text-align: center;"}

Da sich die Diskussion insbesondere in und um #Twitterphilologie orientierte, erschien eben dieser Hashtag als logischer Startpunkt. Bereits am 16. November nutzte ich dafür twecoll, war aber nicht unbedingt komplett überzeugt vom Ergebnis. Wie sich herausstellt, ist die Twitter-API limitiert, sodass Tweets, die einen längeren Zeitraum zurückliegen, bei einer Abfrage der neusten Tweets miteinbezogen werden. Obwohl also maximal 100 Tweets erfragt werden können, wurden nur 42 Tweets zwischen 7. und 15. November für den Graphen genutzt. Eine weitere Extraktion am 28. November beruht auf einer ähnlich geringen Anzahl von Tweets (Zeitraum zwischen 17. und 27. November). Dabei ergibt sich jedoch ein komplett anderes Bild, was damit erklärt werden kann, dass auch Retweets von der API als Tweets erachtet werden. Folge: Eine größere Menge an Accounts also Knoten, auch außerhalb des erwarteten Spektrums.

![Abb. 2]({{site.url}}{{site.baseurl}}/assets/images/twitterphilologie/hashtagtwitterphilologie(neu).png)
Abb. 2: #twitterphilologie (Stand: 28. November).
{: style="color:gray; font-size: 80%; text-align: center;"}

Beide Abbildungen wurden mit ForceAtlas 2 (Maßstab: 50, Stärkere Anziehungskraft) erstellt, zudem wurde über den in Gephi integrierten Modularitätsalgorithmus verschiedene Communities berechnet, die Accounts sind entsprechend erkannter Communities eingefärbt. Die Größe des Knotens ist nach Eingangsgrad geordnet, das heisst das diejenigen, denen innerhalb des Netzwerks am meisten gefolgt wird, entsprechend größer dargestellt werden.

Die Extraktion vom 28. November beinhaltet deutlich mehr unterschiedliche Teilnehmer mit teilweise recht großen Followings, insbesondere etwa @kathrinpassig, trotzdem lässt sich eine Konstanz feststellen. Die Gruppe der größten Knoten ist im Vergleich beider Graphen relativ konstant und besteht aus 6-7 Accounts, die hauptsächlich durch AkademikerInnen betrieben werden. Die beiden Großgruppen Orange/Lila und Hellgrün/Pink können grob als  kulturwissenschaftliche respektive literaturwissenschaftliche Communities gekennzeichnet werden. Am Rand der Community befinden sich Dunkelgrün/Hellblau Studierende und/oder MedienvertreterInnen wie JournalistInnen.

Auch wenn also der Hashtag nicht abgeschottet ist und unterschiedliche Gruppen dort zu Wort kommen, findet der Hauptaustausch zwischen einigen wenigen HauptvertreterInnen mit akademischen Positionen statt. Das ist an sich nichts schlimmes, kann einen aber an die These der geisteswissenschaftlichen Öffnung zweifeln lassen.

## Geisteswissenschaftliche Community
Da ich mich dafür interessierte, wie die maßgeblichen Akteure im #Twitterphilologie-Netzwerk verknüpft sind, machte ich mich daran, eben dies zu erkunden, indem ich die Following-Netzwerke von @Johannes42, @geierandrea2017 und @beritmiriam extrahierte und visualisierte. Der Prozess dauerte verglichen mit den #Twitterphilologie-Netzwerken recht lange, da die Zahl der Knoten und Vernetzungen deutlich umfangreicher war als im limitierten Raum des Hashtags. Das sieht man dem kombinierten Netzwerk der drei Nutzer an:

[![Abb. 3]({{site.url}}{{site.baseurl}}/assets/images/twitterphilologie/netzwerkgeierfranzenberit.png)]({{site.url}}{{site.baseurl}}/assets/images/twitterphilologie/netzwerkgeierfranzenberit.png)
Abb. 3: Kombiniertes Netzwerk der Nutzer Johannes42, geierandrea2017 und beritmiriam.
{: style="color:gray; font-size: 80%; text-align: center;"}

Die grobe Übersicht lässt vier größere Gruppen erkennen, je mit einigen herausragenden VertreterInnen. In der Mitte finden sich bekannte und einflussreiche Nutzer aus verschiedenen Sphären, zu den faszinierendsten Knoten zählt meines Erachtens nach die amerikanische Zeitschrift @NewYorker, die einen der wenigen nicht deutschsprachigen Accounts im Netzwerk darstellt und trotzdem eine zentrale Stellung einnimmt.

[![Abb. 3c]({{site.url}}{{site.baseurl}}/assets/images/twitterphilologie/netzwerk-mitte.png)]({{site.url}}{{site.baseurl}}/assets/images/twitterphilologie/netzwerk-mitte.png)
Abb. 3c: Detailaufnahme Kombiniertes Netzwerk.
{: style="color:gray; font-size: 80%; text-align: center;"}

Im grün-orangenen Bereich finden sich hauptsächlich geistes- und kulturwissenschaftliche Accounts, wobei zu erkennen ist, dass die LiteraturwissenschaftlerInnen in der Twitternutzung kein Monopol besitzen: Viele der orange markierten Accounts gehören twitternden HistorikerInnen, etwa @cjahnz oder @richterhedwig. Auch die VertreterInnen der Digital Humanities lassen sich hier finden, etwa @peertrilcke.

[![Abb. 3e]({{site.url}}{{site.baseurl}}/assets/images/twitterphilologie/netzwerk-orangegruen.png)]({{site.url}}{{site.baseurl}}/assets/images/twitterphilologie/netzwerk-orangegruen.png)
Abb. 3e: Detailaufnahme Kombiniertes Netzwerk.
{: style="color:gray; font-size: 80%; text-align: center;"}

[![Abb. 3d]({{site.url}}{{site.baseurl}}/assets/images/twitterphilologie/netzwerk-orange.png)]({{site.url}}{{site.baseurl}}/assets/images/twitterphilologie/netzwerk-orange.png)
Abb. 3d: Detailaufnahme Kombiniertes Netzwerk.
{: style="color:gray; font-size: 80%; text-align: center;"}

Auf der linken Seite, im blauen Bereich, gruppieren sich hauptsächlich Personen und Institutionen aus dem Literatur- und Kulturbereich wie Verlage (@verbrecherei), Zeitschriften (@volltext) und BloggerInnen (@buzzaldrinsblog), aber auch Bibliotheken wie @stadtbibmuc und AutorInnen wie @sasa_s.

[![Abb. 3a]({{site.url}}{{site.baseurl}}/assets/images/twitterphilologie/netzwerk-blau.png)]({{site.url}}{{site.baseurl}}/assets/images/twitterphilologie/netzwerk-blau.png)
Abb. 3a: Detailaufnahme Kombiniertes Netzwerk.
{: style="color:gray; font-size: 80%; text-align: center;"}

Unter der Farbe Pink sind im Netzwerk feuilletonistisch beziehungsweise gesellschafts- und kulturpolitisch aktive Accounts gruppiert. Das Feld ist recht heterogen und beinhaltet Akteure wie @janboehm, @SophiePassmann, @marga_owski, @antjeschrupp oder @marthadear. Die Größe der Knoten zeigt: hier sind populäre und einflussreiche Accounts gruppiert.

[![Abb. 3f]({{site.url}}{{site.baseurl}}/assets/images/twitterphilologie/netzwerk-pink.png)]({{site.url}}{{site.baseurl}}/assets/images/twitterphilologie/netzwerk-pink.png)
Abb. 3f: Detailaufnahme Kombiniertes Netzwerk.
{: style="color:gray; font-size: 80%; text-align: center;"}

Zuletzt lässt sich noch eine kleine Gruppe nicht deutscher Accounts erkennen, die nicht das kulturelle Prestige des @NewYorker geniessen, aber trotzdem in der Peripherie Teil am Netzwerk haben. Es sind zumeist Accounts von AuslandsgermanistInnen (@HerrBinar, @MurnaneBarry). Der Austausch ist also (noch) nicht groß, aber es gibt Verbindungen.

[![Abb. 3b]({{site.url}}{{site.baseurl}}/assets/images/twitterphilologie/netzwerk-gruenblau.png)]({{site.url}}{{site.baseurl}}/assets/images/twitterphilologie/netzwerk-gruenblau.png)
Abb. 3b: Detailaufnahme Kombiniertes Netzwerk.
{: style="color:gray; font-size: 80%; text-align: center;"}

Was das Netzwerk insgesamt zeigt: Auf Twitter sind Literatur, Feuilleton und Germanistik beziehungsweise Kulturwissenschaft nicht sehr weit auseinander. Kulturtwitter ist kein Dorf, aber eine Kleinstadt.
