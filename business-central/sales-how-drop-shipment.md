---
title: Erstellen Sie einen Verkaufsauftrag, der mit einer Einkaufsbestellung für eine direkte Lieferung verknüpft ist | Microsoft Docs
description: Beschreibt, wie Sie einen Verkaufsauftrag erstellen, der mit einer Bestellung verknüpft ist, um sicherzustellen, dass die Artikel vom Kreditor direkt an den Debitor versendet werden
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: direct shipment
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 7a87023445ea10aa19cc0cc4f60d76ce4cf3e365
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 03/31/2019
ms.locfileid: "929373"
---
# <a name="make-drop-shipments"></a>Direktlieferungen machen
Eine Direktlieferung ist die Lieferung von Artikeln, von einem Ihrer Kreditoren direkt an einen Ihrer Debitoren.

Wenn ein Verkaufsauftrag für Direktlieferung markiert wird und Sie eine Bestellung erstellen, in der der Debitor im Feld **Verk. an Deb.-Nr.** angegeben wird, können Sie die beiden Belege verknüpfen und somit den Kreditor anweisen, direkt an den Kunden zu versenden.

## <a name="to-create-a-sales-order-for-drop-shipment"></a>So erstellen Sie einen Verkaufsauftrag für eine Direktlieferung
Um eine Direktlieferung vorzubereiten, erstellen Sie einen normalen Verkaufsauftrag für einen Artikel, ausser dass Sie in der Verkaufsauftragszeile angeben müssen, dass für den Verkauf Direktlieferung benötigt wird.

1. Legen Sie einen Verkaufsauftrag für einen Artikel an. Weitere Informationen finden Sie unter [Produkte verkaufen](sales-how-sell-products.md)
2. Aktivieren Sie in der Verkaufsauftragszeile für den Direktlieferungsartikel das Kontrollkästchen **Direktlieferung**. Verwenden Sie die Funktion **Spalten auswählen**, wenn das Feld nicht sichtbar ist. Weitere Informationen finden Sie unter [Personalisieren Ihres Arbeitsbereichs](ui-personalization-user.md).

## <a name="to-create-the-purchase-order-for-drop-shipment"></a>So erstellen Sie Bestellungen für Direktlieferungen:
Um eine Direktlieferung für den Artikel, der verkauft werden soll, vorzubereiten, erstellen Sie eine normale Bestellung, ausser dass Sie in der Bestellung angeben müssen, dass direkt an den Debitoren geliefert wird, nicht an Sie selbst.

1. Erstellen Sie eine Bestellung. Füllen Sie keines dieser Felder in den Zeilen aus. Weitere Informationen finden Sie unter [Erfassen eines Einkaufs](purchasing-how-record-purchases.md).
2. Wählen Sie im Feld **Verk. an Deb.-Nr.** den Debitor aus, an die Sie verkaufen.
3. Wählen Sie die Aktion **Direktlieferungen** aus, und dann die Aktion **Auftrag holen**.
4. Auf der Seite **Verkaufsliste** wählen Sie den Auftrag, den Sie im Abschnitt [So erstellen Sie einen Verkaufsauftrag für Direktlieferung](sales-how-drop-shipment.md#to-create-a-sales-order-for-drop-shipment) vorbereitet haben.
5. Wählen Sie die Schaltfläche **OK** aus.

Die Zeileninformation aus dem Auftrag werden in die Bestellzeile eingetragen.

Sie können nun den Kreditor anweisen, die Artikel an Ihren Kunden zu versenden, indem Sie ihm beispielsweise die Bestellung als PDF-Datei senden.     

## <a name="to-view-the-linked-purchase-order-from-the-sales-order"></a>So zeigen Sie den verknüpften Auftrag aus der Bestellung an
* Wählen Sie die Verkaufsauftragszeile der Direktlieferung aus, dann die Aktion **Bestellung**, die Aktion **Direktlieferung** und die Aktion **Bestellung**.

## <a name="to-post-a-drop-shipment"></a>So buchen Sie eine Direktlieferung:
Wenn der Kreditor die Artikel geliefert hat, können Sie den Verkaufsauftrag als geliefert buchen. Sie können auch die Bestellung buchen, aber nur mit der Option **Erhalten** bis der Verkaufsauftrag fakturiert wurde.

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Aufträge** ein, und wählen dann den zugehörigen Link aus.
2. Öffnen Sie den Verkaufsauftrag, den Sie in [So erstellen Sie einen Verkaufsauftrag für Direktlieferung]() erstellt haben.
3. Geben Sie im Feld **Zu liefernde Menge** an, wieviele der Bestellmengen geliefert werden sollen, die gesamte Menge oder eine Teilmenge.
4. Wählen Sie die Aktion **Buchen** oder **Buchen und Senden** aus.
5. Wählen Sie dann entweder die Option **Liefern**, um zu einem späteren Zeitpunkt zu fakturieren oder **Liefern und Fakturieren**, um sofort zu fakturieren.

## <a name="see-also"></a>Siehe auch
[Spezialaufträge erstellen:](sales-how-to-create-special-orders.md)  
[Einkauf von Artikeln für einen Verkauf](purchasing-how-purchase-products-sale.md)  
[Produkte verkaufen](sales-how-sell-products.md)  
[Erfassen eines Einkaufs](purchasing-how-record-purchases.md)  
[Verkauf](sales-manage-sales.md)  
[Lagerbesttand](inventory-manage-inventory.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
