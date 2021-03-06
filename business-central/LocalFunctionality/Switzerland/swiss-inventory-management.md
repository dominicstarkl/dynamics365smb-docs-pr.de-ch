---
title: Lagerverwaltung (Schweiz)
description: Schweizer Erweiterungen enthalten spezielle Lagerverwaltungsfunktionen.
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
ms.openlocfilehash: 697e9501ba09daf63eecc2e17f7695f757bafb5a
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 03/31/2019
ms.locfileid: "931883"
---
# <a name="swiss-inventory-management"></a>Lagerverwaltung (Schweiz)
[!INCLUDE[d365fin](../../includes/d365fin_md.md)] enthält Schweizer Erweiterungen für Lagerverwaltung. Dies beinhaltet Folgendes:  

- Detaillierte Berichte.  Weitere Informationen finden Sie unter Verkaufstatistikbericht und Lagerlistenbericht.  
- Die Fähigkeit, eine Rechnung mit mehreren Lieferungen nachzuverfolgen.  
- Einschliessen eines Artikelkarten-Lagerortcodes als Standardlagerortcode für Verkaufszeilen und Artikelerfassungsjournale. Weitere Informationen finden Sie unter [Einrichten von Lagerorten](../../inventory-how-setup-locations.md).

## <a name="managing-item-details"></a>Verwalten von Artikeldetails  
Unternehmen haben u. U. verschiedene Lager für verschiedene Produktkategorien. In diesem Fall muss der von der Artikelkarte abgerufene Standardlagerortcode verwendet werden. Wenn Sie einen Lagerortcode für einen Artikel definieren, wird dieser auf die Verkaufszeilen und Artikelerfassungsjournale als Standardlagerortcode übertragen. Weitere Informationen finden Sie unter Verkaufszeile und Artikel Erf.-Journalzeile.  

Zusätzliche Informationen, wie Debitorennummer, Lieferadresscode und Debitorenvertriebsmitarbeitercode wird in Lagerposten gespeichert. Diese Informationen sollen dabei helfen, benutzerdefinierte Berichterstellungskriterien wie Einnahmen pro Debitor zu erstellen und Artikel oder Debitoren für Verkäufer bereitzustellen. Weitere Informationen erhalten Sie in der Tabelle "Lagerposten".  

## <a name="invoices-with-multiple-shipments"></a>Rechnungen mit mehreren Lieferungen  
Sind mehrere Lieferungen für einen Debitoren gebucht worden, können Sie Sammelrechnungen mit der Funktion **Lieferzeilen abrufen** erstellen. Weitere Informationen finden Sie auf der Seite „Versandzeilen abrufen“. Wenn Sie diese Funktion verwenden, enthält der Text, der in den Rechnungszeilen erstellt wird, die Informationen über die Nummer der Auslieferung und das Lieferdatum. Beispielsweise kann der Text als Lieferungsnummer erscheinen. 102040 von 25.01.01. Auf diese Weise können Sie Rechnungen mit mehreren Lieferungen verfolgen.  

## <a name="see-also"></a>Siehe auch  
 [Kopieren von vorhandenen Elementen in neue Elemente](how-to-copy-existing-items-to-new-items.md)  
 [Lokale Funktion (Schweiz)](switzerland-local-functionality.md)   
 [Einrichten von Lagerorten](../../inventory-how-setup-locations.md)
