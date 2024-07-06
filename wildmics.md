# Wildmics Twitch Termine als iCal

## Einführung

Ich verpasse **regelmäßig** die Wildmics auf twitch, weshalb ich ein kleines Projekt gestartet habe. Per `API Call` die nächsten Termine von twitch.tv abrufen, diesen Kalender in `Home Assistant` einlesen, und mich benachrichtigen lassen, sobald ein bestimmtes Liveevent stattfindet.

Keine Angst, das Ganze funktioniert auch ohne Home Assistant! Zuerst benötigen wir eine gültige `.ics`-Datei. Hierfür gibt es zwei verschiedene Quellen (Stand *06. Juli 2024*):

1. https://api.twitch.tv/helix/schedule/icalendar?broadcaster_id=96555323
2. https://zeugen-kuehlwaldis.org/veranstaltungstipps.ics

Die erste URL beinhaltet automatisch von twitch.tv generierte Daten; diese sind immer aktuell.

Die zweite URL hingegen ist von [Florian Spitzohr](https://zeugen-kuehlwaldis.org); Florians Kalender wird von Hand aktualisiert und enthält mehr Informationen (bsp. eine Beschreibung, wohingegen der Abruf bei twitch.tv aktuell nur einen Titel generiert); allerdings kann es natürlich theoretisch mal passieren, dass Florian zum Beispiel Besseres zu tun hat, krank geworden ist, im Urlaub ist, morphogenetische Felder das Erstellen seiner Kalenderdatei blockieren, und, und, und / oder, oder, oder.

Wer die schönere, detailliertere Variante möchte, nimmt Florians Veranstaltungstipps, wer hingegen immer automatisch die von twitch.tv bereitgestellten Termine haben möchte, nimmt erstere Datei. Die von twitch.tv bereitgestellten Daten basieren auf den vom Wildmics Team bei Twitch eingetragenen Daten, daher sollten sie definitiv korrekt sein. Sollten ;-)

## Kalender abonnieren

#### Auf dem Android Smartphone

Auf dem Android Smartphone könnt Ihr die App `ICSx5` verwenden; dort abonniert Ihr einfach einen der o.g. Links und fertig. Ihr habt somit die Termine in Eurem Terminkalender.

#### Über Home Assistant

Wenn Ihr Euch mithilfe von Home Assistant an bestimmte Termine erinnern lassen möchtet, könnt Ihr den Kalender dort als iCal Quelle abonnieren und die Einträge filtern; bsp. könnt Ihr Euch dann **ausschließlich** dann per Signal, Telegram, WhatsApp, Home Assistant Mobile Companion, oder welchen Dienst auch immer Ihr bevorzugt, benachrichten lassen, wenn `#nachsitzen` oder `Hoaxilla` im Titel des jeweiligen Kalendereintrages steht.

Hierfür folgt eine detaillierte Beschreibung *hoffentlich* Mitte Juli 2024.

#### Auf dem iPhone

Da ich kein iPhone benutze, kann ich hier keine Anleitung bereitstellen; wenn jemand dies übernehmen möchte, dann möge diese Person bitte einen Pull Request für `wildmics.md` [hier](https://github.com/prankousky/prankousky.github.io) erstellen, und diesen Paragraphen hier mit einer entsprechenden Anleitung ersetzen. Ich vertraue dann darauf, dass die Anleitung dieser Person stimmt, da ich sie ja mangels iPhone nicht überprüfen kann.

---

**letzte Änderung** *2024-07-06*

**rev** *0.09*
