---
title: 'Vorgehensweise: Umlagerung von Artikeln in erweiterten Basis-Lagerkonfigurationen | Microsoft Docs'
description: In erweiterten Lagerkonfigurationen, die Lagerorte mit gesteuerter Einlagerung und Kommissionierung verwenden, werden die Umlagerungen zwischen Lagerplätzen von einem erfahrenen Mitarbeiter durchgeführt, der die Umlagerungen im Lagerplatzumlagerungsvorschlag vorbereitet und von dort aus Lagerplatzumlagerungen erstellt, die die Mitarbeiter ausführen sollen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 442f25cdeefba42815e3e97dedad8713c3ecf1e4
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 03/31/2019
ms.locfileid: "912524"
---
# <a name="move-items-in-advanced-warehouse-configurations"></a>Umlagerung von Artikeln in erweiterten Lagerkonfigurationen
In erweiterten Lagerkonfigurationen, die Lagerorte mit gesteuerter Einlagerung und Kommissionierung verwenden, werden die Umlagerungen zwischen Lagerplätzen von einem erfahrenen Mitarbeiter durchgeführt, der die Umlagerungen im Lagerplatzumlagerungsvorschlag vorbereitet und von dort aus Lagerplatzumlagerungen erstellt, die die Mitarbeiter ausführen sollen.  

## <a name="to-move-items-with-the-warehouse-movement-worksheet"></a>Um Artikel mit dem Lagerplatzumlagerungsvorschlag umzulagern
Die Seite **Lagerplatzumlagerungsvorschlag** beinhaltet zwei Funktionen, die Sie dabei unterstützen, die Zeilen automatisch auszufüllen. Die erste Funktion ist die Funktion **Lagerplatzauffüllung berechnen**. Diese Funktion verwendet die Lagerplatzprioritäten, um eine Auffüllung der Lagerplätze mit höheren Prioritäten aus denen mit niedrigeren Prioritäten vorzuschlagen. Die zweite Funktion ist die Funktion **Lagerplatzinhalt holen**, die die Vorschlagszeilen mit dem gesamten Inhalt des Lagerplatzes oder der Lagerplätze füllt, die Sie festlegen.

1.  Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Lagerplatzumlagerungsvorschlag** ein, und wählen dann den zugehörigen Link aus.  
2.  Geben Sie die entsprechenden Lagerplatzumlagerungs-Informationen in die Vorschlagszeilen ein.  
3. Wählen Sie die Aktion **Lagerplatzumlagerung erstellen**aus, um einen Umlagerungsbeleg zu erstellen, der registriert werden kann, wenn die Lagerplatzumlagerung abgeschlossen ist.  

### <a name="to-register-the-warehouse-movement"></a>So registrieren Sie die Lagerplatzumlagerung:  
1.  Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Umlagerungen** ein, und wählen dann den zugehörigen Link aus.  
2.  Öffnen Sie die Lagerumlagerung, die Sie verarbeiten möchten.  
3.  Geben Sie in Zeilen der Aktionsart **Bereich** an, wo, welche und wann der fragliche Artikel umgelagert wird, indem Sie die Felder **Zonencode**, **Lagerplatzcode**, **Bewegungsmenge** oder **Fälligkeitsdatum** bearbeiten.  

    Wenn Ihr Lager so eingerichtet wurde, dass die Lagerplatzcodes der physischen Struktur des Lagers entsprechen, können Sie Mengen mehrerer Artikel aus aufeinander folgenden Gebindelagerplätzen (Palettenlagerplätzen) entnehmen und sie dann in Kommissionierlagerplätze (mit hoher Priorität) einlagern, die ebenfalls dicht nebeneinander liegen können.  
4.  Geben Sie in Zeilen der Aktionsart **Lagerentnahme** im Feld **Bewegungsmenge** eine Teilmenge des Lagerplatzinhalts ein, die Sie umlagern möchten. Alle anderen Felder in Zeilen der Aktionsart **Lagerentnahme** sind schreibgeschützt.  
5.  Um alle vorgeschlagenen Mengen zu verschieben, die im Feld **Menge** angegeben sind, wählen Sie die Aktion **Bewegungsmenge autom. ausfüllen** aus.  
6. Wählen Sie die Aktion **Registrieren** aus.  

> [!NOTE]  
>  Wenn der Lagerort die gesteuerte Einlagerung und Kommissionierung verwendet, können Sie keine Artikel manuell in einen Lagerplatz der Lagerplatzart EING hinein oder aus diesem heraus umlagern, da Artikel in einem solchen Lagerplatz als eingelagert registriert werden müssen, bevor sie Teil des verfügbaren Lagerbestands werden.

## <a name="to-register-the-movement-of-an-item-that-has-already-occurred"></a>So registrieren Sie eine Lagerplatzumlagerung eines Artikels, die bereits stattgefunden hat:  
Wenn Ihr Lagerort die gesteuerte Einlagerung und Kommissionierung verwendet und Sie Artikel ohne eine bereits bestehende Einlagerung, Kommissionierung oder Lagerplatzumlagerung in andere Lagerplätze umlagern müssen, können Sie die richtige Platzierung der Artikel im Lager mithilfe des **Logistik Umlag. Erfassungsjournals** registrieren.

1.  Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Logistik Umlag. Erf.-Journal** ein, und wählen dann den zugehörigen Link aus.  
2.  Füllen Sie die Felder **Artikelnr.**, **Von Zonencode**, **Von Lagerplatzcode**, **Nach Zonencode** und **Nach Lagerplatzcode** aus.  
3.  Wählen Sie die Aktion **Registrieren** aus.  

## <a name="see-also"></a>Siehe auch  
[Logistik](warehouse-manage-warehouse.md)  
[Lagerbesttand](inventory-manage-inventory.md)  
[Lagerortverwaltung einrichten](warehouse-setup-warehouse.md)     
[Montageverwaltung](assembly-assemble-items.md)    
[Designdetails: Logistik](design-details-warehouse-management.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
