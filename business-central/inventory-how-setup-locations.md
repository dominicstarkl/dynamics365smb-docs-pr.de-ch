---
title: Einrichten einer Lagerortkarte und definieren von Umlagerungsrouten| Microsoft Docs
description: Sie stellen eine Lagerortkarte für jedes Bundesland, den von Lagerartikel speichern, beispielsweise, ein Lager oder eine Vertriebsstelle und Einrichtungsrouten, um Artikel zwischen Lagerorten umlagern erstellen.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, distribution center
ms.date: 04/01/2019
ms.author: SorenGP
ms.openlocfilehash: d94f1bb2fe45263f013119954622b995e902b30f
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 03/31/2019
ms.locfileid: "937860"
---
# <a name="set-up-locations"></a>Einrichten von Lagerorten
Wenn Sie Artikel a mehr als einem Ort oder Lagerort kaufen, lagern oder verkaufen, müssen Sie jeden Lagerplatz mit einer Lagerortkarte einrichten und Umlagerungsrouten definieren.

Sie können dann Belegzeilen für einen bestimmten Lagerplatz erstellen, Verfügbarkeit nach Lagerplatz anzeigen und Lagerbestand zwischen Lagerplätzen umlagern. Weitere Informationen finden Sie unter [Lagerbestand verwalten](inventory-manage-inventory.md).

## <a name="to-create-a-location-card"></a>So erstellen Sie eine Lagerortkarte
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Standort** ein, und wählen dann den zugehörigen Link aus.
2. Wählen Sie die Aktion **Neu** aus.
3. Füllen Sie auf der Seite **Lagerortkarte** die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Wiederholen Sie die Schritte 2 und 3 für jeden Lagerplatz, an dem Sie Lagerbestand aufbewahren möchten.

> [!NOTE]  
> Viele Felder auf der Lagerortkarte beziehen sich auf Auftragsabwicklung von Artikel in eingehenden und ausgehenden Lagerprozessen. Weitere Informationen finden Sie unter [Lagerortverwaltung einrichten](warehouse-setup-warehouse.md).

## <a name="to-create-a-transfer-route"></a>So erstellen Sie eine Umlagerungsroute
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Transferrouten** ein, und wählen dann den zugehörigen Link aus.
2. Wählen Sie von jedem beliebigen Fenster **Standortkarten** die Aktion **Umlagerungsrouten** aus.
3. Wählen Sie die Aktion **Neu** aus.
4. Füllen Sie auf der Seite **Lagerortkarte** die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Sie können jetzt die Lagerartikel zwischen zwei Lagerplätzen umlagern. Weitere Informationen finden Sie unter [Lagerbestand zwischen Lagerplätzen umlagern](inventory-how-transfer-between-locations.md).    

## <a name="see-also"></a>Siehe auch
[Verwalten des Lagerbestands](inventory-manage-inventory.md)  
[Lagerbestand zwischen Lagerplätzen umlagern](inventory-how-transfer-between-locations.md)    
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Sie können auswählen, welche Funktionen angezeigt werden](ui-experiences.md)  
[Allgemeine Geschäftsfunktionen](ui-across-business-areas.md)
