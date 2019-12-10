---
title: "Mapping 19th Lit - Eine Karte"
layout: post
lang: de
ref: mapping-project
tag: Projekt
projects: true
summary: "Eine Karte"
category: projekt
author: mhaeussermann
---
[![Mapping 19th Lit]({{site.url}}{{site.baseurl}}/assets/images/19thlitmap.png)](https://manuelhaeussermann.de/mapping-19th-lit/)

**Mapping 19th Lit** ist eine Karte, das als Abschlussprojekt von [Moacir P. de Sá Pereiras](https://moacir.com/) Kurs [The JavaScripting English Major](https://the-javascripting-english-major.org/), einem JavaScript-Einsteigerkurs, entstand.

Die Karte basiert auf dem [Corpus of German-Language Fiction](https://figshare.com/articles/Corpus_of_German-Language_Fiction_txt_/4524680), das 2.753 deutschsprachige Werke der Gutenberg-DE Edition (veröffentlicht 2013) enthält. Davon sind 1.436 während des 19. Jahrhunderts entstanden. Erste Versuche des Geotagging mit [spaCy](https://github.com/explosion/spaCy) waren wenig erfolgreich, insbesondere wegen des Ressourcenaufwands und der suboptimalen Anpassung auf ein historisches Datenset. Stattdessen wurde eine grobe Liste durch [Geotext](https://geotext.readthedocs.io/en/latest/) erstellt und anhand heuristischer Entscheidungen bereinigt (etwa Fälle von False Positives bei Städtenamen, die auch Personennamen sein können). Diese Top-50-Liste wurde zuletzt automatisiert mit Koordinaten versehen.

Die Karte ist [hier](https://manuelhaeussermann.de/mapping-19th-lit/) zu finden. Das Repository [hier](https://github.com/mhaeussermann/mapping-19th-lit).
