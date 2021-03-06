---
title: 'Vorgehensweise: Buchen von Kapazitäten | Microsoft Docs'
description: 'Im Kapazitäts Erf.-Journal buchen Sie verbrauchte Kapazität, die keinem Fertigungsauftrag zugeordnet ist. Zum Beispiel: Wartungsarbeit muss einem Arbeitsplatz oder einer Arbeitsplatzgruppe zugeordnet werden, aber nicht einem Fertigungsauftrag.'
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
ms.openlocfilehash: 58005b8b4d401f5eab8a934d7b00b610b64b4281
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 03/31/2019
ms.locfileid: "928314"
---
# <a name="post-capacities"></a>Kapazität buchen
Im Kapazitäts Erf.-Journal buchen Sie verbrauchte Kapazität, die keinem Fertigungsauftrag zugeordnet ist. Zum Beispiel: Wartungsarbeit muss einem Arbeitsplatz oder einer Arbeitsplatzgruppe zugeordnet werden, aber nicht einem Fertigungsauftrag.  

## <a name="to-post-capacities"></a>Kapazitäten buchen  
1.  Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Kapazitäts-Buch.-Blätter** ein, und wählen dann den zugehörigen Link aus.  
2.  Füllen Sie die Felder **Buchungsdatum** und **Belegnr.** aus.  
3.  Geben Sie in das Feld **Art** die Art der Kapazität entweder **Arbeitsplatz** oder **Arbeitsplatzgruppe** ein, die Sie buchen möchten.  
4.  Geben Sie im Feld **Nr.** Geben Sie die Nummer des Arbeitsplatzes oder der Arbeitsplatzgruppe ein.  
5.  Geben Sie in den anderen Feldern die entsprechenden Daten, wie zum Beispiel **Startzeit**, **Endzeit**, **Menge** und **Ausschuss** ein.  
6.  Um die Rechnung zu buchen, wählen Sie die Aktion **Buchen** aus.  

## <a name="to-view-work-center-ledger-entries"></a>Um sich die Arbeitsplatzgruppeneinträge anzeigen zu lassen:  
Auf den Seiten **Arbeitsplatzgruppenkarte** und **Arbeitsplatzkarte** können Sie gebuchte Kapazität aufgrund der Informationen zu beendeten Fertigungsaufträgen anzeigen.    
1.  Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Arbeitszentren** ein, und wählen dann den zugehörigen Link aus.  
2.  Öffnen Sie die relevante Karte **Arbeitsplatzgruppe** aus der Liste, und wählen Sie die **Kapazitätsposten** Aktion aus.  

Auf der Seite **Kapazitätsposten** werden die gebuchten Posten der Arbeitsplatzgruppe in der Reihenfolge der Buchungen angezeigt.   

## <a name="see-also"></a>Siehe auch  
[Bearbeitungen](production-manage-manufacturing.md)    
[Produktion einrichten](production-configure-production-processes.md)  
[Planung](production-planning.md)      
[Lagerbesttand](inventory-manage-inventory.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
