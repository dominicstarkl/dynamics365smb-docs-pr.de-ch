---
title: Migrieren von Daten von Dynamics GP mit der Datenmigrations-Erweiterung | Microsoft Docs
description: Verwenden Sie die GP-Datenmigrationserweiterung, um Debitoren, Kreditoren, Lagerartikel, Fibukonten, Transaktionen zu offenen Verbindlichkeiten und Forderungen von Dynamics GP auf Business Central zu migrieren.
documentationcenter: ''
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, import, implement
ms.date: 04/01/2019
ms.author: edupont
ms.openlocfilehash: cf401500c34d8d40acc153a591229684770afa64
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 03/31/2019
ms.locfileid: "917490"
---
# <a name="the-dynamics-gp-data-migration-extension"></a>Die Dynamics GP-Datenmigrations-Erweiterung 
Diese Erweiterung erleichtert die Verwendung der GP-Datenmigrationserweiterung, um Debitoren, Kreditoren, Lagerartikel, Fibukonten, Transaktionen zu offenen Verbindlichkeiten und Forderungen von Dynamics GP auf [!INCLUDE[prodshort](includes/prodshort.md)] zu migrieren. Wenn Ihr Geschäft Dynamics GP heute verwendet, können Sie die relevanten Daten exportieren und dann eine unterstützte Einrichtungsanleitung öffnen, um die Daten hochzuladen und in [!INCLUDE[prodshort](includes/prodshort.md)] zu migrieren. Die Migrationserweiterungsarbeiten für alle unterstützten Versionen von Microsoft Dyanmics GP. Weitere Informationen finden Sie unter [Geschäftsdaten aus anderen Finanzsystemen zu importieren](across-import-data-configuration-packages.md).

## <a name="exporting-data-from-dynamics-gp"></a>Exportieren von Daten aus Dynamics GP
Sie müssen Ihre bestehenden Debitoren, Kreditoren, Lagerartikel und Fibukonten mit der Datenexportfunktionalität in Dynamics GP exportiert haben. Wenn Sie die Daten zum Export auswählen, können folgende Typen ausgewählt werden:

* Konto  
* Debitor  
* Option  
* Kreditor  

Bei Erstellung der Exportdatei erhalten Sie eine ZIP-Datei, die mehrere TXT-Dateien enthält. Der Inhalt wird durch Ihe Auswahl beim ExportDatenvorgang bestimmt.  Es gibt auch zusätzliche TXT-Dateien, die erstellt werden, die unterstützende Informationen enthalten, die für die Einrichtung innerhalb Ihres neuen [!INCLUDE[prodshort](includes/prodshort.md)]-Unternehmens benötigt werden.

Die Dynamics GP-Datenmigrationserweiterung ordnet automatisch die exportierten Daten zu, so dass Sie Ihre bestehenden Daten rasch im [!INCLUDE[prodshort](includes/prodshort.md)] Unternehmen bereitstehen.

## <a name="whats-new-in-the-october-2018-release"></a>Neuigkeiten in der Version im Oktober 2018

In dieser Version haben wir die Datenmenge erweitert, die wir von Dynamics GP nach [!INCLUDE[prodshort](includes/prodshort.md)] migrieren.

Im Migrations-Assistenten können Sie jetzt auswählen, wie Sie den Dynamics GP-Kontenplan migrieren möchten. Sie können den vorhandenen Kontenplan migrieren, oder auf Grundlage des vorhandenen Kontenplans einen neuen erstellen.  

Wenn Sie den vorhandenen Kontenplan verwenden, werden die Konten als das Hauptkontosegment von Dynamics GP eingerichtet und zusätzliche Segmente werden als Dimensionen in [!INCLUDE[prodshort](includes/prodshort.md)] eingerichtet.  

Wenn Sie einen neuen Kontenplan erstellen, gelangen Sie im Assistenten zu einer zusätzlichen Kontoinformationsseite, sodass Sie die Arbeitsmappe herunterladen, erforderliche Änderungen vornehmen und die Arbeitsmappe erneut importieren können, um die Konten zu ändern.  

Sie müssen die Excel-Arbeitsmappe herunterladen und jeder Kontonummer im Excel-Arbeitsblatt eine neue Kontonummer zuordnen. Jedes Konto benötigt eine eigene Nummer, oder Sie erhalten einen Fehler bei der Migration. Wenn Sie die Zuordnung abgeschlossen haben, können Sie den Migrations-Assistenten fortsetzen, indem Sie die Excel-Arbeitsmappe importieren, die Sie soeben aktualisiert haben. Der Assistent überprüft, dass jede Zeile über eine eindeutige Kontonummer verfügt und dass keine Zeilen eine leere neue Kontonummer haben.  

Mit den Optionen zur Änderung der Zuordnung des Kontenplans, werden Sie auch eine Änderung beim Datentyp bemerken, der bei den Kontonummern des Fibu Erf.-Journals erfolgt.  

- Wenn Sie die vorhandenen Kontonummern verwenden, wird der Anfangswert Bestand des Hauptsegments (neue Kontonummer) als eine Summierung der Hauptsachkontennummer zum Zeitpunkt der Migration transferiert.  
- Wenn Sie neue Kontonummern erstellen, werden zusammengefasste Informationen zum Äquivalent von zwei Geschäftsjahren auf Grundlage der Finanzzeiträume transferiert, die Sie in Dynamics GP eingerichtet haben.

In früheren Versionen von [!INCLUDE[prodshort](includes/prodshort.md)], hat der Assistent eine zusammenfassende Transaktion der Debitor/Kreditor-Bilanz in Dynamics GP migriert. Nun werden die detaillierten offenen Transaktionen für Debitoren und Kreditoren zum Zeitpunkt der Migration transferiert. Was bedeutet das? Wenn für Ihren Debitor im Forderungen-Modul 3 Transaktionen ausstehen, überträgt der Assistent diese Transaktionen mit dem ausstehenden Betrag als Belegbetrag in [!INCLUDE[prodshort](includes/prodshort.md)]. Dasselbe gilt für das Verbindlichkeiten-Modul für Kreditoren.  

Lagerartikel werden mit der Bewertungsmethode mit Kosten importiert, die ausgewählt wurde, als Einrichtungsassistent des Unternehmens ausgeführt wurde. Serviceartikel werden der FIFO-Bewertungsmethode automatisch zugeordnet. Derzeit bringen wir den Lagerbestand der Artikel zum Zeitpunkt der Migration ein.  Diese Menge wird in einen leeren Lagerort eingebracht.  

Die letzte Option, die im Datenmigrationsassistenten für Dynamics GP angezeigt wird, ist die Möglichkeit, die Buchungsoption anzugeben. Diese Einstellung gibt an, ob Sie alle Transaktionen in Fibu-Erf.-Journalzeilen buchen möchten, sobald Daten von der Migration in [!INCLUDE[prodshort](includes/prodshort.md)] verschoben werden, oder ob Sie die Erfassung manuell durchführen möchten, sodass alle Transaktionen auf der Fibu Erf.-Journal-Seite stapelweise angezeigt werden, damit Sie die Informationen vor dem Erfassen überprüfen können. Diese Option finden Sie in der Kontenplanoptionsseite.


## <a name="see-also"></a>Siehe auch
[Geschäftsdaten aus anderen Finanzsystemen migrieren](across-import-data-configuration-packages.md)  
[Anpassen [!INCLUDE[prodshort](includes/prodshort.md)] Erweiterungen nutzenb](ui-extensions.md)  
