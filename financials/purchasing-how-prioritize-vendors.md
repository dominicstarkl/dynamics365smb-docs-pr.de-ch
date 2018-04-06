---
title: "Weisen Sie einem Kreditor eine Prioritätsstufe zu| Microsoft Docs"
description: "Sie können sowohl Zahlen Ihren Kreditoren oder Lieferanten zuweisen, um sie zu priorisieren und Zahlungsvorschläge in Finance and Operations, Business edition zu erleichtern."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: supplier, payment priority
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: d44e06f4dd33332e8d96e712e93ed05c7f0a920b
ms.contentlocale: de-ch
ms.lasthandoff: 03/22/2018

---
# <a name="prioritize-vendors"></a>Kreditoren priorisieren
[!INCLUDE[d365fin](includes/d365fin_md.md)] kann verschiedene Zahlungen an Kreditoren vorschlagen. Dies können z. B. Zahlungen sein, die in Kürze fällig sind, oder Zahlungen, bei denen Sie einen Rabatt erhalten können. Weitere Informationen finden Sie unter [Erstellen von Zahlungsvorschlägen für Kreditoren](payables-how-suggest-vendor-payments.md).

Zuerst müssen Sie den Kreditoren priorisieren, indem Sie ihm Nummern zuweisen.

## <a name="to-prioritize-vendors"></a>So priorisieren Sie Kreditoren
1. Wählen Sie das Symbol ![Nach Seite oder Bericht suchen] (media/ui-search/search_small.png "Nach Seite oder Bericht suchen")und geben **Bankkonten** ein. Wählen Sie dann den zugehörigen Link aus.
2. Wählen Sie die entsprechende Kreditor, und klicken Sie dann auf **Bearbeiten**.
3. Geben Sie im Feld **Priorität** eine Zahl ein.

[!INCLUDE[d365fin](includes/d365fin_md.md)] geht davon aus, dass die niedrigsten Nummern (ausser 0) die höchste Priorität haben. Wenn Sie also z. B. 1, 2 und 3 verwenden, erhält 1 die höchste Priorität.

Falls Sie einem Kreditor keine Priorität zuweisen wollen, lassen Sie das Feld **Priorität** leer. Wenn Sie dann die Funktion "Zahlungsvorschlag" verwenden, wird dieser Kreditor nach den Kreditoren aufgeführt, die eine Priorität haben. Sie können so viele Prioritäten einrichten wie Sie benötigen.

## <a name="see-also"></a>Siehe auch
[Einkaufeinrichten](purchasing-setup-purchasing.md)  
[Verwalten von Verbindlichkeiten|](payables-manage-payables.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
