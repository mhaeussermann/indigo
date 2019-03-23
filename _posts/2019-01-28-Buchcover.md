---
title: "Reclaimbook – Ein Buchcover-Generator"
layout: post
lang: de
ref: reclaim-project
tag: Projekt
projects: true
summary: "Ein Buchcover-Generator"
category: projekt
author: mhaeussermann
---
![Demo]({{site.url}}{{site.baseurl}}/assets/images/cover-generator-demo.gif)

**Reclaimbook** ist eine simple Webapp, basierend auf HTML, CSS und JavaScript, und zugleich eine ästhetisch ansprechende Darstellungsform für AI-generierte Buchtitel. Beim Klick auf den *Vorschlag*-Button wird zufällig einer von 1.647 Buchtiteln eingesetzt, beim Klick auf den *Bild speichern*-Button wird das entsprechende Cover als png-Datei abgespeichert.

Diese Buchtitel wurden mit Hilfe von Max Woolfs [textgenrnn](https://github.com/minimaxir/textgenrnn) generiert, auf Basis eines Trainingssets von 2.735 deutschsprachigen Buchtiteln, hauptsächlich des 19. Jahrhunderts, aus dem [Corpus of German-Language Fiction (txt)](https://figshare.com/articles/Corpus_of_German-Language_Fiction_txt_/4524680). Aufgrund des relativ kleinen Trainingssets wurden Titel teilweise reproduziert, dies wurde jedoch nicht bereinigt, um eine spielerische Unsicherheit hinsichtlich der Frage der Authentizität beizubehalten.

Der Buchcover-Generator kann [hier]({{site.url}}{{site.baseurl}}/reclaimbook/) ausprobiert werden.
