---
title: 'Gewusst wie: Drucken von MWST-Abrechnungen (Schweiz) (ältere Version)'
description: Die Schweizer MWST-Abrechnung ist der Standardberechnungsbericht für die Realisierung der MWST Sie können diesen Bericht drucken und ihn für die quartalsweise Steuerberichterstellung verwenden.
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
ms.openlocfilehash: 63d16ae6f310a72b8c3767f2db1c73d36415f37d
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 03/31/2019
ms.locfileid: "914704"
---
# <a name="print-swiss-vat-statements-older-version"></a>Drucken von MWST-Abrechnungen (Schweiz) (ältere Version)

> [!NOTE]  
>  In diesem Thema wird für Rückwärtskompatibilität mit dem Bericht **Schweizer MWST-Abrechnung** behandelt. Informationen zur Verwendung der späteren Schweizer MWST-Abrechnung, siehe Schweizer MWST-Abrechnung.  

Die **Schweizer MWST-Abrechnung** ist der Standardberechnungsbericht für die Realisierung der MWST Sie können diesen Bericht drucken und ihn für die quartalsweise Steuerberichterstellung verwenden. Das **Schweizer MWST-Abrechnung** enthält Folgendes:  

- Ein MWST-Posten.  
- MWST-Regulierungsposten.  
- Ein Abrechnungsbogen.  

## <a name="to-print-the-swiss-vat-statement"></a>So drucken Sie die MWST-Abrechnung (Schweiz)  

1.  Alternativ wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](../../media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und öffnen **MWST-Abrechnung Schweiz**. Wählen Sie dann den zugehörigen Link aus.  

    > [!NOTE]  
    >  Sie erhalten eine Meldung die angibt, dass **Schweizer MWST-Abrechnung** in der Landessprache geöffnet wird.  

2.  Füllen Sie auf dem Inforegister **Optionen** die Felder wie in der folgenden Tabelle beschrieben aus.  

    |Feld|Description|  
    |---------------------------------|---------------------------------------|  
    |**Geschlossen mit Journalnummer**|Wählen Sie die Finanzbuchhaltungserf.-Journale aus, die die Buchungsquelle der Mehrwertsteuerberichtigungsbuchungen enthalten. In diesem Feld werden die Buchhaltungsperioden ausgewertet, die bereits ausgeglichen wurden.|  
    |**Verfügbar bis (Datum)**|Wählen Sie das Datum, um offene oder erledigte MWST-Posten zu bearbeiten.|  
    |**Buchungen anzeigen**|Gibt an, ob alle MWST-Posten für jede Gruppe gedruckt werden.|  
    |**Ausgleichsbuchungen anzeigen**|Gibt an, ob MWST-Posten und Fibuposten mit abgeschlossenen Zusammenfassungen oder erneut gebuchte Steuern gedruckt werden.|  
    |**Normalsatz (MWST %)**|Wählen Sie die aktuellen typischen Mehrwertsteuersätze aus, die verwendet werden, um die richtigen Sätze den Geschäfts- und Produktgruppen, die in den Mehrwertsteuereinstellungen definiert werden, zuzuweisen.|  
    |**Reduzierter Satz (MWST %)**|Wählen Sie die aktuellen reduzierten Steuersätze aus, die verwendet werden, um die richtigen Sätze den Geschäfts- und Produktgruppen, die in den Mehrwertsteuereinstellungen definiert werden, zuzuweisen.|  
    |**Sondersatz MWST %**|Wählen Sie die aktuellen besonderen Steuersätze aus, die verwendet werden, um die richtigen Sätze den Geschäfts- und Produktgruppen, die in den Mehrwertsteuereinstellungen definiert werden, zuzuweisen.|  
    |**Vorsteuerabzug Investition/Betriebsaufwand (Fibukonto)**|Wählen Sie das Fibukonto für die MWST aus.|  
    |**Eigenverbrauch Gesch. Gruppe**|Wählen Sie in der Geschäfts- und Produktgruppe für den Eigenverbrauch aus.|  
    |**Service Fremde Geschl Gruppe**|Wählen Sie das Auslandsdienstgeschäft und die Produktgruppe aus.|  
    |**Exporte Gesch. Gruppe**|Wählen Sie in der Geschäfts- und Produktgruppe für den Export aus.|  

3.  Wählen Sie die Schaltfläche **Drucken** aus, um den MwSt-Bericht zu drucken, oder die Schaltfläche **Vorschau**, um den Bericht auf dem Bildschirm anzuzeigen.  

## <a name="see-also"></a>Siehe auch  
 [Mehrwertsteuer (Schweiz)](swiss-value-added-tax.md)   
 [MWST-Sätze für die Schweiz](vat-rates-for-switzerland.md)
