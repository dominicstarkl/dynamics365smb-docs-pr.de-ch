---
title: Verarbeiten von Lager- und Fertigungskosten | Microsoft Docs
description: Obgleich viele der Kostenberechnungsfunktionen in untergeordneten Prozessen ohne Benutzereingriff ausgedrückt werden (beispielsweise Postenausgleich und automatische Lagerregulierung), sind eine Reihe von Feldern, Seiten und Berichten für Benutzer konzipiert, die die Kosten von Artikeln oder Arbeitsgängen direkt oder indirekt verwalten.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 53f1c002236877f536a85586d0af912d5e9a85c2
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 03/31/2019
ms.locfileid: "918618"
---
# <a name="handling-inventory-and-manufacturing-costs"></a>Verarbeiten von Lager- und Fertigungskosten
Obgleich viele der Kostenberechnungsfunktionen in untergeordneten Prozessen ohne Benutzereingriff ausgedrückt werden (beispielsweise Postenausgleich und automatische Lagerregulierung), sind eine Reihe von Feldern, Seiten und Berichten für Benutzer konzipiert, die die Kosten von Artikeln oder Arbeitsgängen direkt oder indirekt verwalten.  

 Das Zuordnen von Artikelzu-/-abschlägen zu Einkaufsbelegen ist ein Beispiel für eine indirekte Kostenberechnungsaufgabe. Das Aktualisieren des Einstandspreises von Produktionsstücklistenartikeln ist ein Beispiel für eine direktere Kostenberechnungsaufgabe.  

 In der folgenden Tabelle wird eine Reihe von Aufgaben mit Verknüpfungen zu den beschriebenen Themen erläutert.   

|**Bis**|**Siehe**|  
|------------|-------------|  
|Periodisches oder automatisches Aktualisieren des Einstandspreises von Artikeln, um Kostenänderungen bei eingehenden Posten (beispielsweise Posten für Einkäufe oder gefertigte Artikel) an die zugehörigen ausgehenden Posten (beispielsweise Verbrauch oder Umlagerung) weiterzugeben|[Artikelpreise justieren](inventory-how-adjust-item-costs.md)|  
|Verschaffen eines Überblicks über die Dynamik des durchschnittlichen Einstandspreises, um Entscheidungen zur Preisgestaltung zu treffen oder Kostenschwankungen nachzugehen, die auf Dateneingabefehler zurückzuführen sind|[Neue Artikel registrieren](inventory-how-register-new-items.md)|  
|Erstellen des festen Einstandspreises eines Fertigungsartikels durch Eingeben der drei Kostenelemente: Materialkosten, Kapazitätskosten und Fremdarbeiterkosten|[Informationen zur Berechnung von festen Einstandspreisen](finance-about-calculating-standard-cost.md)|  
|Berechnen des Einstandspreises eines Stücklistenartikels auf der Grundlage der Einstandspreise der zugrundeliegenden Komponenten|[Mit Fertigungsstücklisten arbeiten](inventory-how-work-BOMs.md)|  
|Abschliessen des Kostenberechnungs-Lebenszyklus eines gefertigten Artikels durch Regulieren der Kosten sowie Abstimmen der Wertposten mit der Finanzbuchhaltung|[Info zu Kosten des beendeten FA](finance-about-finished-production-order-costs.md)|  
|Ändern des Werts eines Artikels im Lagerbestand oder des Werts eines Lagerpostens (beispielsweise einer Einkaufstransaktion)|[Neubewerten von Lagerbestand](inventory-how-revalue-inventory.md)|
|Manuelles Rückgängigmachen eines Artikelausgleichs oder erneutes Ausgleichen von Lagerposten, die durch die Anwendung erstellt wurden|[Entfernen und erneutes Ausgleichen von Lagerposten](finance-how-to-remove-and-reapply-item-entries.md)|  
|Sie können das Feld **Eintrag anwenden** im Erf.-Journal verwenden, um manuell einen festen Ausgleich zwischen einer eingehenden Transaktion und der ursprünglichen ausgehenden Transaktion zu erstellen.|[Schliessen von offenen Lagerposten aus einem festen Ausgleich im Artikel Erf.-Journal](finance-how-to-close-open-item-ledger-entries-resulting-from-fixed-application-in-the-item-journal.md)|  

## <a name="see-also"></a>Siehe auch  
[Lagerkosten Verwalten](finance-manage-inventory-costs.md)
[Designdetails: Lagerkosten](design-details-inventory-costing.md)
