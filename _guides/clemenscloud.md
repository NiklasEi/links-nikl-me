---
layout: clemenscloud
name: clemenscloud
title: Clemenscloud - Guide
description: Ein kurzer guide für die Clemenscloud mit einer Anleitung für das Einrichten der Handy und Desktop App.
---


1. [Clemenscloud](#clemenscloud)
   * [Accountverwaltung](#accountverwaltung)
   * [Dateien verwalten](#dateien-verwalten)
   * [Dateien teilen](#dateien-teilen)
2. [Handy App](#handy-app)
   * [Automatisches Hochladen](#automatisches-hochladen)
   * [Kontakte sichern](#kontakte-sichern)
3. [Desktop App](#desktop-app)
   
   
   
# Clemenscloud

Auf meinem Server läuft unter [cloud.eicker.me](https://cloud.eicker.me) ein Programm, mit dem Daten gespeichert, geteilt und zwischen verschiedenen Geräten synchronisiert werden können (siehe [Nextcloud website](https://nextcloud.com/) für mehr Infos). Jeder in der Familie kann von mir einen Account erstellt bekommen und hat dann unbegrenzten Speicherplatz. Es gibt eine Android App, eine Apple App und Desktop Apps für Windows, OS X und Linux. Mit der Handy-App kannst du zum Beispiel deine Handybilder und Videos automatisch hochladen lassen und hast damit eine Sicherheitskopie, falls dein Handy abhanden kommt oder mal baden gehen sollte.

Außerdem ermöglicht die cloud problemlos große Datenmengen mit anderen zu teilen (siehe [Dateien teilen](#dateien-teilen)) und kann Sicherheitskopien deiner Kontakte anlegen (siehe [Kontakte sichern](#kontakte-sichern)).

Das alles lässt sich sehr schnell und einfach einrichten.

### Accountverwaltung

Nach dem ersten Login bitte ich darum, dass du dein Anfangspasswort änderst und eine E-mail Adresse in dein Profil einträgst. Beides wird in den Einstellungen gemacht, die du über deinen Avatar oben-rechts finden kannst. Die E-mail Adresse ist kein Muss, aber wenn du sie angibst, kannst du eigenständig dein Passwort zurücksetzten, falls du das mal vergessen solltest 😉

In den Einstellungen kann auch eine Menge anderer Sachen geändert werden, wie zum Beispiel die Sprache, falls dir die Grundeinstellung nicht gefällt.

### Dateien verwalten

Wenn du dich anmeldest, bist du standardmäßig in der "Alle Dateien" Ansicht, in die du jederzeit zurück kannst, indem du oben links auf das Ordnersymbol klickst. Dateien können hier einfach durch drag-and-drop oder durch Klicken auf das "+" über der Dateienliste hochgeladen werden. Wenn du auf das Plus klickst, kannst du auch neue Ordner erstellen, um Chaos zu vermeiden.

Alle Dateien sind erstmal nur für dich sichtbar und niemand sonst hat Zugriff darauf! Geteilte Dateien oder Ordner werden, wie unten in dem Bild gezeigt, markiert.

![Dateien](/assets/img/clemenscloud/dateien.png)

### Dateien teilen

Dateien können durch Klicken auf das Teilensymbol (oben im Bild markiert) für andere zugänglich gemacht werden. Keine Sorge, das kann jeder Zeit rückgängig gemacht oder bearbeitet werden. 

Es gibt zwei unterschiedliche Möglichkeiten, um Dateien zu teilen:
1. Mit Gruppen oder anderen Personen in der Cloud
2. Per Link

Wenn du einen Ordner oder eine Datei mit einer oder mehreren Gruppen oder Personen teilst, erscheint bei diesen Accounts der geteilte Inhalt unter "Alle Dateien". Je nachdem, welche Rechte du vergeben hast, können die anderen die Dateien nur sehen und herunterladen, oder auch verändern.

Beim Teilen per Link kann ein Passwort für den Download eingerichtet werden und ein Ablaufdatum, nachdem der Link automatisch nicht mehr zur Verfügung steht.

# Handy App

Die App heißt Nextcloud und kann ganz normal vom Appstore aus installiert werden. Nach der Installation musst du einmalig dein Konto einrichten.

1. Als Serveradresse `https://cloud.eicker.me/nextcloud` eingeben.

   ![Dateien](/assets/img/clemenscloud/app1.png)

2. Der App Zugriff auf dein Konto gewähren. Im zweiten Schritt musst du dich dafür einloggen.

   ![Dateien](/assets/img/clemenscloud/app2.png) ![Dateien](/assets/img/clemenscloud/app3.png)
   
3. Die App muss Zugriff auf deine Handy Dateien haben, sonst kann nichts hoch- oder runtergeladen werden.
   
   ![Dateien](/assets/img/clemenscloud/app4.png)
   
### Automatisches Hochladen

Optional kann jetzt noch das automatische Hochladen von Bildern und/oder Videos aktiviert werden. Dazu musst du das Menü über die drei Striche oben-links öffnen und auf "Automatisches Hochladen" klicken.

![Dateien](/assets/img/clemenscloud/app5.png)

Jetzt wird eine Liste mit verschiedenen Kategorien von Dateien gezeigt. Für jede Kategorie kann das automatische Hochladen einzeln eingestellt werden. Dafür musst du nur auf die kleine Wolke klicken. Eine durchgestrichene Wolke bedeutet, es wird nicht hochgeladen. Eine blaue Wolke bedeutet die App läd automatisch alle neuen Bilder in die Cloud.

![Dateien](/assets/img/clemenscloud/app6.png)

Wenn du die Synchronisation für die Kategorie Kamera eingestellt hast, kannst du einen Test machen, indem du ein Bild machst und guckst, ob es in der Cloud auftaucht. Standardmäßig läd die App Bilder und Videos nur hoch, wenn eine W-lan Verbindung besteht! Wenn du ein begrenztes mobiles Datenvolumen hast, solltest du diese Einstellung nicht ändern.

Um auch die älteren Bilder in der Cloud zu speichern, kannst du einen manuellen Upload starten (am besten über Nacht).

### Kontakte sichern

Die App ermöglicht auch die automatische oder manuelle Sicherung all deiner Kontakte. Die Kontaktliste wird als `.vcf` Datei exportiert und in dem versteckten Ordner `.Contacts-Backup` abgelegt. Die Dateien können, wie im Abschnitt [Importieren](#importieren) beschrieben, eingelesen werden. Wenn du ein neues Handy bekommst, kannst du einfach die letzte Sicherung importieren und alle Kontakte sind wieder in deinem Handy.

#### Exportieren

1. Öffne die Einstellungen der Nextcloud App.

   ![export_1](/assets/img/clemenscloud/contacts/export_1_menu.png){:.appscreenshot}

2. Klick unten auf "Kontakte sichern".

   ![export_2](/assets/img/clemenscloud/contacts/export_2_einstellungen.png){:.appscreenshot}

3. Hier kannst du entweder automatische, tägliche Sicherungen mit dem Schalter "Automatisch sichern" aktivieren, oder eine manuelle Sicherung durch klicken auf "Jetzt Sichern" starten.

   ![export_3](/assets/img/clemenscloud/contacts/export_3.png){:.appscreenshot}

4. Um die Sicherungen in deinem cloud Ordner zu sehen, muss die Einstellung "Versteckte Dateien anzeigen" aktiviert werden. Hier gelten Ordner oder Dateien mit einem Punkt am Anfang des Names als versteckt.

   ![export_4](/assets/img/clemenscloud/contacts/export_4_einstellungen.png){:.appscreenshot}

5. Du findest die Sicherungen jetzt in dem Ordner `.Contacts-Backup` mit zeitkodierten Namen.

   ![export_5](/assets/img/clemenscloud/contacts/export_5_folder.png){:.appscreenshot}
   ![export_6](/assets/img/clemenscloud/contacts/export_6_files.png){:.appscreenshot}

#### Importieren

Je nach Betriebssystem deines Handys und der Version, kann es kleine Unterschiede im Ablauf geben.

1. In deinen Kontakten das Menü öffnen.

   ![Import_1](/assets/img/clemenscloud/contacts/import_1.png){:.appscreenshot}

2. Die Aktion "Verwalten von Kontakten" auswählen.

   ![Import_2](/assets/img/clemenscloud/contacts/import_2.png){:.appscreenshot}

3. Der nächste Schritt ist "Kontakte importieren/exportieren".

   ![Import_3](/assets/img/clemenscloud/contacts/import_3.png){:.appscreenshot}

4. Wähle "Importieren".

   ![Import_4](/assets/img/clemenscloud/contacts/import_4.png){:.appscreenshot}

5. Jetzt kommt es auf den Speicherort deiner Nextcloud App an. Wahrscheinlich wurde sie mit standard Einstellungen installiert, also musst du im nächsten Schritt "Interner Speicher" auswählen. Das Handy durchsucht jetzt den internen Speicher nach Visitenkartendateien und listet alle gefunden auf.

   ![Import_5](/assets/img/clemenscloud/contacts/import_5.png){:.appscreenshot}

6. Suche die neuste Sicherung in der Liste, wähle sie aus und bestätige die Wahl mit "Fertig".

   ![Import_6](/assets/img/clemenscloud/contacts/import_6.png){:.appscreenshot}

7. Jetzt kann gewählt werden, wo die Kontakte gespeichert werden sollen. Da schon Sicherungen der Kontakte in der cloud existieren (also keine Synchronisation via Google-Konto nötig ist), kann hier einfach "Telefon" gewählt werden. Zum Abschluss unten auf "Importieren" klicken.

   ![Import_7](/assets/img/clemenscloud/contacts/import_7.png){:.appscreenshot}
   ![Import_8](/assets/img/clemenscloud/contacts/import_8.png){:.appscreenshot}

# Desktop App

Die Nextcloud Anwendung kann für verschiedene Betriebssysteme [heruntergeladen werden](https://nextcloud.com/install/#install-clients). Nach der Installation muss zuerst das Konto eingerichtet werden.

Als Serveradresse bitte immer `https://cloud.eicker.me/nextcloud` verwenden.

Das Programm erstellt einen lokalen Ordner, der mit deinem Cloudordner synchronisiert wird. Das bedeutet, du hast jetzt automatisch deine Handybilder auf dem PC, falls auch die Handy App wie oben beschrieben eingerichtet ist. Außerdem können so sehr schnell und bequem Dateien in der Cloud abgesichert werden, indem du sie einfach in den lokalen Ordner kopierst.

Die Synchronisation funktioniert voll automatisiert in alle Richtungen. Jede Änderung in dem Handyordner oder Ordner auf dem PC wird in der Cloud übernommen und umgekehrt. Es ist also eine Sache von Sekunden Dateien vom Computer auf das Handy zu ziehen, und das ohne Kabel 😉 