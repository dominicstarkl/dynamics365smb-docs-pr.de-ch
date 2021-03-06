---
title: Einrichten von Preisen und Kosten für Services | Microsoft Docs
description: 'Vorgehensweise: Einrichten von Preisen und zusätzlichen Kosten für Services.'
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: service, cost, service order
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 8683d82b4a6f56f415f3b66efa5be11b003fe878
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 03/31/2019
ms.locfileid: "926620"
---
# <a name="set-up-pricing-and-additional-costs-for-services"></a>Einrichten von Preisen und zusätzlichen Kosten für Services
Mithilfe der [!INCLUDE[d365fin](includes/d365fin_md.md)]-Preisfunktionen kann die Anwendung so eingerichtet und konfiguriert werden, dass Preise für Serviceartikel, Reparaturen und Aufträge übernommen und angepasst werden. Diese Preisentscheidungen werden anschliessend problemlos an den Abrechnungsprozess übertragen.  
  
Entsprechend den Implementierungsanforderungen können Sie Preisgruppen festlegen und sie bestimmten Zeiträumen, Debitoren oder Währungen zuordnen. Sie können feste, minimale oder maximale Preise abhängig von den Serviceverträgen einrichten, die mit Debitoren abgeschlossen wurden. Zuletzt können Sie beim Anpassen der Preise die Änderungen anzeigen und genehmigen, bevor Sie sie an das Hauptbuch übertragen.  

## <a name="to-set-up-a-service-price-group"></a>So richten Sie eine Servicepreisgruppe ein
Sie können Servicepreisgruppen einrichten, um Gruppen von Serviceartikeln zu bilden, die derselben Servicepreisgestaltung unterliegen. Sie verbinden die Servicepreisgruppen mit den Serviceartikeln in den Serviceartikelzeilen. Servicepreisgruppen können auch mit Serviceartikelgruppen verbunden werden.  

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Servicepreisgruppen** ein, und wählen dann den zugehörigen Link aus.  
2. Erstellen Sie eine neue Servicepreisgruppe.  
3. Füllen Sie die Felder **Code** und **Beschreibung** aus.  
4. Wählen Sie die Aktion **Einrichten** aus.  
2. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

 > [!Tip]
 > Die Felder **Anpassungstyp** und **Betrag** arbeiten zusammen, um zu definieren, ob diese Anpassung einen festen Betrag betrifft, oder ob sie nur gilt, wenn der gesamte Servicepreis den Betrag im Feld **Betrag** über- oder unterschreitet.  

## <a name="to-set-up-a-service-price-adjustment-group"></a>So richten Sie eine Servicepreiskorrekturgruppe ein  
Sie wählen für jede Art von Servicepreisgestaltung eine Servicepreiskorrekturgruppe. Sie können z. B. Preiskorrekturgruppen einrichten, mit denen der Preis für Fracht oder Ersatzteile korrigiert wird.  
  
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Servicepreisanpassungsgruppen** ein, und wählen dann den zugehörigen Link aus.  
2. Erstellen Sie eine neue Servicepreiskorrekturgruppe.  
3. Füllen Sie die Felder **Code** und **Beschreibung** aus.  
4. Geben Sie im Feld **Art** geben Sie die Art des Postens ein, den Sie anpassen möchten.  
  
    * Um nur einen bestimmten Posten zu korrigieren, geben Sie die Nummer des Postens in **Nr.** ein Feld Wenn Sie das Feld leer lassen, werden ALLE Posten der Art, die Sie im Feld **Art** festgelegt haben, korrigiert.  
    * Um die Servicepreise anzupassen, die nur für einen bestimmten Arbeitstyp passen, füllen Sie das Feld **Arbeitstyp** aus. Wenn Sie das Feld leer lassen, wird es ignoriert.  
  
5. Im Feld **Beschreibung** können Sie eine kurze Beschreibung der Servicepreiskorrektur hinterlegen.  
6. Um Servicepreise anzupassen, die sich nur auf eine bestimmte Produktbuchungsgruppe beziehen, füllen Sie das Feld **Gen. Prod. Buchungsgruppe** aus.

> [!Tip]
> Sie können **Details** auswählen, um zusätzliche Informationen für die Anpassungsgruppe hinzufügen. Sie können z. B. festlegen, welcher Artikel zur Servicepreiskorrekturgruppe gehört und ob es sich um einen Artikel, eine Ressource, eine Ressourcengruppe oder einen Zuschlag handelt.  

## <a name="to-set-up-additional-costs-for-services"></a>Einrichten zusätzlicher Kosten für Services
Wenn Sie mit Serviceartikeln und Serviceaufträgen arbeiten, können Sie zusätzliche Kosten, wie Reisekosten in bestimmten Servicegebieten oder die Grundgebühren erfassen. Wenn Sie einen Serviceauftrag erstellen, können Sie diese Kosten einfügen und eine Zeile mit dem Typ **Kosten** wird dem Auftrag hinzugefügt. Wenn Sie die Kosten in alle Serviceaufträge übernehmen möchten, können Sie Standardkosten einrichten. Wenn Sie beispielsweise immer eine Grundgebühr anwenden möchten.
  
### <a name="to-set-up-service-costs"></a>Um Servicekosten einzurichten
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Servicekosten** ein, und wählen dann den zugehörigen Link aus. 
2. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

### <a name="to-specify-a-default-cost-for-service-orders"></a>Um Standardkosten für Serviceaufträge anzugeben
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Service einrichten** ein, und wählen dann den zugehörigen Link aus. 
2. Geben Sie im Feld **Serviceauftragsgrundgebühr** die entsprechenden Servicekosten aus.

## <a name="see-also"></a>Siehe auch
[Einrichten der Serviceverwaltung](service-setup-service.md)  
[Service](service-service.md)  
