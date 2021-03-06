---
title: 'Gewusst wie: Drucken von ESR.-Rechnungen'
description: Sie können einen Einzahlungsschein mit Referenznummer (ESR) auf mehrere Arten drucken.
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
ms.openlocfilehash: 7897b15140e8ee3dbe63ab4707c8bfbc89008e2b
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 03/31/2019
ms.locfileid: "932002"
---
# <a name="print-esr-invoices"></a>Drucken von ESR-Rechnungen
Zum Drucken von Einzahlungsscheinen mit Referenznummer (ESR) stehen folgende Methoden zur Auswahl:  

- Als Teil der Verkaufsrechnung ESR.  
- Als separaten Beleg, dem ESR-Coupon.  

Der Bericht "Verkauf ESR Rechnung" entspricht der Verkaufsrechnung mit beigefügtem zusätzlichem ESR-Abschnitt. Indem Sie den Verkauf ESR-Couponsbericht verwenden, können Sie den blauen Einzahlungsbeleg drucken.  

> [!NOTE]  
>  Sie müssen bei der Installation des ESR-Zahlungsmoduls einen Drucker und Einstellungen auswählen, damit der Einzahlungsbeleg korrekt gedruckt wird. Weitere Informationen finden Sie unter Druckerauswahl – Tabelle.  

Im folgenden Verfahren wird das Drucken von ESR-Verkaufsrechnungen beschrieben, dieselben Schritte gelten jedoch auch für ESR-Abschnitte.  

## <a name="to-print-esr-invoices"></a>So drucken Sie ESR-Rechnungen  

1.  Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](../../media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **ESR-Rechnung** ein und wählen den zugehörenden Link aus.  
2.  Füllen Sie im Stapelverarbeitungsauftrag **Verkauf ESR Rechnung** die Felder auf dem Inforegister **Optionen** wie in der folgenden Tabelle beschrieben aus.  

    |Feld|Description|  
    |---------------------------------|---------------------------------------|  
    |**Anzahl Kopien**|Geben Sie die gewünschte Anzahl der Berichtskopien ein.|  
    |**ESR-Bank**|Wählen Sie die ESR-Bankleitzahl aus, die in dem Bericht gedruckt werden soll.<br /><br /> Wenn der Wert in diesem Feld <Blank> und der ESR-Zahlungsformcode nicht auf der Seite **ESR-Einrichtung** definiert ist, wird die ESR-Hauptbank, die auf der Seite **ESR-Einrichtung** ausgewählt wird, gedruckt.|  
    |**Aktivität protokollieren**|Gibt an, ob die Aktivitäten, die Sie mit Ihren Kontakten haben, protokolliert werden.|  
    |**ESR-System**|Wählen Sie das ESR-System aus, über das Sie neue ESR-Coupons an Kunden schicken können. Wählen Sie **Gemäss ESR-Bank**, um das ESR-System der im Feld **ESR-Bank** angegebenen Bank zu verwenden.|  

3.  Wählen Sie die Schaltfläche **Drucken** aus, um den Bericht zu drucken, oder die Schaltfläche **Vorschau**, um den Bericht auf dem Bildschirm anzuzeigen.  

Sie können den Bericht "Verkauf ESR Rechnung" oder "Verkauf ESR Abschnitt" auch erneut drucken.  

## <a name="see-also"></a>Siehe auch  
 [Elektronische Zahlungen mit ESR (Schweiz)](swiss-electronic-payments-using-esr.md)   
 [Importieren von ESR-Zahlungen](how-to-import-esr-payments.md)
