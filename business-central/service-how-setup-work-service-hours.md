---
title: 'Vorgehensweise: Einrichten von Arbeits- und Servicezeiten | Microsoft Docs'
description: Sie können die üblichen Arbeitszeiten in Ihrer Firma festlegen. Anhand von diesen Servicezeiten werden die Reaktionszeiten (Datum und Zeit) für Serviceaufträge und -offerten berechnet und Reaktionszeitwarnungen ausgegeben.
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
ms.openlocfilehash: dfa339b19d9b6b86bb9153ce7856cb6134463ec8
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 03/31/2019
ms.locfileid: "915564"
---
# <a name="set-up-work-hours-and-service-hours"></a>Einrichten von Arbeits- und Servicezeiten
Normalerweise verfolgt ein Servicemanagementsystem Ressourcenstunden und den Serviceauftragsstatus, um die Arbeitsauslastung und Serviceanforderungen zu prognostizieren. [!INCLUDE[d365fin](includes/d365fin_md.md)] verfügt über integrierte Tools, die so angepasst werden können, dass diese Arten von Informationen erfasst werden.  
  
Nach dem Festlegen der standardmässigen Servicestunden des Unternehmens können Antwortzeiten für Serviceaufträge berechnet oder Warnhinweise gesendet werden, wenn Serviceanrufe eingehen. Die Warnfunktion wird in Verbindung mit dem Objektaufrufplaner implementiert.   
  
Da Sie an einem Serviceauftrag arbeiten, werden Sie den Status aktualisieren wollen, sodass Sie den Fortschritt überwachen können. Der Serviceauftragsstatus spiegelt den Reparaturstatus aller Serviceartikel des Serviceauftrags wider. Weitere Informationen finden Sie unter [Serviceauftrag und Reparaturstatus verstehen](service-order-repair-status.md). 

## <a name="to-set-up-default-service-hours"></a>So richten Sie Servicestandardzeiten ein  
Verwenden Sie die Seite **Standardservicezeiten**, um die üblichen Arbeitszeiten in Ihrer Firma festzulegen. Anhand von diesen Servicezeiten werden die Reaktionszeiten (Datum und Zeit) für Serviceaufträge und -angebote berechnet und Reaktionszeitwarnungen ausgegeben. Wenn Sie keine vertragsspezifischen Servicezeiten in Verträgen einrichten, werden die Standardservicezeiten für den Servicevertrag verwendet.  
  
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Standard-Servicestunden** ein, und wählen dann den zugehörigen Link aus.  
2. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
  
> [!IMPORTANT]  
>  Wenn Sie die Zeilen auf der Seite **Standardservicezeiten** leer lassen, ist der Vorgabewert "24 Stunden" nur für Werktage gültig.  
  
## <a name="to-set-up-work-hour-templates"></a>Um Arbeitszeitvorlagen einzurichten
Sie können die Seite **Arbeitszeitvorlagen** verwenden, um Vorlagen einzurichten, die die typischen Arbeitszeiten Ihrer Firma enthalten. Sie können z. B. Vorlagen für Techniker in Vollzeit oder in Teilzeit einrichten. Sie können Arbeitszeitvorlagen verwenden, wenn Sie Ressourcenkapazitäten hinzufügen.  
  
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Arbeitsstunden-Vorlage** ein, und wählen dann den zugehörigen Link aus.  
2. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
  
> [!Note]
> Nachdem Sie Arbeitsstunden für jeden Tag eingeben, wird der Wert im Feld **Stunden pro Woche** berechnet.  

## <a name="to-set-up-contract-specific-service-hours"></a>So richten Sie vertragsspezifische Servicezeiten ein  
Die Seite **Servicezeiten** können Sie verwenden, um spezifische Servicezeiten für den Debitor dieser Serviceverträge einzurichten. Anhand von Servicezeiten werden die Reaktionszeiten (Datum und Zeit) für Serviceaufträge und -angebote berechnet, die zu dem Servicevertrag gehören.  
  
Wenn Sie keine vertragsspezifischen Servicezeiten in Verträgen einrichten, werden die Servicestandardzeiten für den Servicevertrag verwendet.  
  
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Serviceverträge** ein, und wählen dann den zugehörigen Link aus.  
2. Öffnen Sie den relevanten  **Servicevertrag**, für den Sie bestimmte Servicezeiten einrichten möchten.  
4. Um Servicezeiten basierend auf den Servicestandardzeiten einzurichten, wählen Sie die Aktion **Servicestandardzeiten kopieren**.  
5. Bearbeiten Sie die Felder in den Servicezeiteneinträgen. Löschen Sie Einträge oder fügen Sie sie ein, um die Servicezeiten für den Vertrag einzurichten. Beachten Sie, dass die Felder **Tag**, **Startzeit** und **Endzeit** für jede Zeile ausgefüllt werden müssen.  
6. Wenn Sie möchten, dass die Servicezeiten ab einem bestimmten Datum gelten, müssen Sie das Feld **Startdatum** ausfüllen.  
7. Wenn die Servicezeiten auch an Feiertagen gelten sollen, dann versehen Sie das Feld **An Feiertagen gültig** mit einem Häkchen.  

## <a name="see-also"></a>Siehe auch  
[Zuordnungsstatus und Reparaturstatus](service-allocation-status-and-repair-status.md)  
[Einrichten der Serviceverwaltung](service-setup-service.md)  
[Serviceauftrags- und Reparaturstatus](service-order-repair-status.md)  
