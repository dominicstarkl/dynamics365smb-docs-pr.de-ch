---
title: 'Designdetails: Aktive vs. historische Artikeltrackingposten | Microsoft Docs'
description: "Wenn Teile einer Belegzeilenmenge gebucht werden, wird nur diese bestimmte Menge in Lagerposten und deren Artikeltrackingnummern übertragen. Jedoch möchten Sie sicher auf alle relevanten Trackinginformationen des Artikels direkt aus der aktiven Belegzeile heraus zugreifen. Anders ausgedrückt, Sie möchten nicht nur die Posten, die mit der Restmenge verbunden sind, sondern Sie wünschen auch Informationen über die gebuchten Einheiten. Wenn Sie das Fenster **Artikeltrackingzeilen** anzeigen oder ändern, werden die Kollektivinhalte der Tabelle **Trackingspezifikation** (T336) und der Tabelle **Reservierungsposten** (T337) in einer temporären Version von T336 dargestellt. Dadurch ist sichergestellt, dass auf historische und aktive Artikeltrackingdaten als Einheit zugegriffen wird."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 0b0d49b4f9b9e77b311628c2d88b4891b32f8276
ms.contentlocale: de-ch
ms.lasthandoff: 09/22/2017

---
# <a name="design-details-active-versus-historic-item-tracking-entries"></a>Designdetails: Aktive vs. historische Artikeltrackingposten
Wenn Teile einer Belegzeilenmenge gebucht werden, wird nur diese bestimmte Menge in Lagerposten und deren Artikeltrackingnummern übertragen. Jedoch möchten Sie sicher auf alle relevanten Trackinginformationen des Artikels direkt aus der aktiven Belegzeile heraus zugreifen. Anders ausgedrückt, Sie möchten nicht nur die Posten, die mit der Restmenge verbunden sind, sondern Sie wünschen auch Informationen über die gebuchten Einheiten. Wenn Sie das Fenster **Artikeltrackingzeilen** anzeigen oder ändern, werden die Kollektivinhalte der Tabelle **Trackingspezifikation** (T336) und der Tabelle **Reservierungsposten** (T337) in einer temporären Version von T336 dargestellt. Dadurch ist sichergestellt, dass auf historische und aktive Artikeltrackingdaten als Einheit zugegriffen wird.  

 Die nachstehende Tabelle zeigt, wie T336 und T337 in einem Einkaufsszenario verwendet werden. Die fettgedruckten Zahlen stellen Werte dar, die der Benutzer manuell in das **Artikeltrackingzeilen**-Fenster eingibt.  

 Schritt 1: Erstellen Sie eine Einkaufszeile von sieben Stück mit Artikeltrackingnummern.  

||**Menge (Basis)**|**Bewegungsmge.**|**Zu fakturieren Menge (Basis)**|**Geb. Bewegungsmenge (Basis)**|**Fakturierte Menge (Basis)**|  
|-|----------------------------------------------|--------------------------------------------|------------------------------------------------------|-------------------------------------------------------|--------------------------------------------------------|  
|**T337**|7|0|0|0|0|  
|**T336**|0|0|0|0|0|  

 Schritt 2: Empfangen Sie vier Teile.  

||**Menge (Basis)**|**Bewegungsmge.**|**Zu fakturieren Menge (Basis)**|**Geb. Bewegungsmenge (Basis)**|**Fakturierte Menge (Basis)**|  
|-|----------------------------------------------|--------------------------------------------|------------------------------------------------------|-------------------------------------------------------|--------------------------------------------------------|  
|Fenster**Artikelverf.-Zeilen**|7|**4**|**0**|0|0|  
|**T337**|3|0|0|0|0|  
|**T336**|4|0|0|4|0|  

 Schritt 3: Empfangen Sie zwei Teile, und fakturieren Sie zwei Teile.  

||**Menge (Basis)**|**Bewegungsmge.**|**Zu fakturieren Menge (Basis)**|**Geb. Bewegungsmenge (Basis)**|**Fakturierte Menge (Basis)**|  
|-|----------------------------------------------|--------------------------------------------|------------------------------------------------------|-------------------------------------------------------|--------------------------------------------------------|  
|Fenster**Artikelverf.-Zeilen**|7|**2**|**2**|4|0|  
|**T337**|0|0|0|0|0|  
|**T336**|6|0|0|6|2|  

 Schritt 4: Empfangen Sie ein Stück.  

||**Menge (Basis)**|**Bewegungsmge.**|**Zu fakturieren Menge (Basis)**|**Geb. Bewegungsmenge (Basis)**|**Fakturierte Menge (Basis)**|  
|-|----------------------------------------------|--------------------------------------------|------------------------------------------------------|-------------------------------------------------------|--------------------------------------------------------|  
|Fenster**Artikelverf.-Zeilen**|7|**1**|**0**|6|2|  
|**T336**|7|0|0|7|2|  

 Fakturieren von 5 Stück.  

||**Menge (Basis)**|**Bewegungsmge.**|**Zu fakturieren Menge (Basis)**|**Geb. Bewegungsmenge (Basis)**|**Fakturierte Menge (Basis)**|  
|-|----------------------------------------------|--------------------------------------------|------------------------------------------------------|-------------------------------------------------------|--------------------------------------------------------|  
|Fenster**Artikelverf.-Zeilen**|7|0|**5**|7|2|  
|**T336**|7|0|0|7|7|  

## <a name="see-also"></a>Siehe auch  
 [Designdetails: Artikeltracking](design-details-item-tracking.md)   
 [Designdetails: Artikelverfolgungszeilenfenster](design-details-item-tracking-lines-window.md)
