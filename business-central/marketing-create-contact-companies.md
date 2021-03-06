---
title: Erstellen von Kontaktunternehmen| Microsoft Docs
ddescription: Outlines the tasks to create contact companies, including assigning relevant data about prospects and defining the business relationships you have with companies.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 75f055dcc862f3954aa0c50d6d22643940baa538
ms.sourcegitcommit: addfb47612cc2e4e98dfd7e338b6f41cde405d5c
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 04/16/2019
ms.locfileid: "938979"
---
# <a name="create-contacts"></a>Kontakt erstellen
Sie treffen regelmäßig Personen aus anderen Unternehmen, die ggf. zu Geschäftsbeziehungen wie einer Kundenbeziehung werden. Wenn solch ein neuer Kontakt geknüpft wird, müssen so viele Informationen wie möglich auf einer Kontaktkarte erfasst werden, um eine weitere Kommunikation zu ermöglichen.

## <a name="person-or-company"></a>Person oder Unternehmen
Sie können einen Kontakt als Person oder ein Unternehmen angeben, je nachdem, ob Sie den Namen der Kontaktperson zum Zeitpunkt der Erstellung kennen. Sie tun dies, wenn Sie das Feld **Art** auf der Seite **Kontaktkarte** ausfüllen. Außerdem können Sie Kontaktkarten für ein Unternehmen und mindestens eine dort arbeitende Person führen. Das erfolgt automatisch, wenn Sie das Feld **Unternehmensname** auf einer Kontaktkarte des Typs **Person** ausfüllen.

Die Funktionalität ist für beide Arten gleich, abgesehen davon, dass die Optionen für zusätzliche Informationen sich je nach Art ändern. Beispielsweise können Sie Verantwortlichkeiten nur einer Person und Branchengruppe nur einem Unternehmen zuweisen. Dieses wird in der Benutzeroberfläche angegeben, indem sich die Felder und Aktionen, die nicht angewendet werden können, ausgegraut werden. Sie können den Wert des Felds **Art** später ändern, oder Sie können die Felder im Inforegister **Übernahme** auf der Seite **Marketingeinrichtung** verwenden, um zu steuern, welche Daten zwischen einer Person und dem zugehörigen Unternehmen freigegeben werden. Weitere Informationen finden Sie unter [Einrichten von Kontakten](marketing-setup-contacts.md).

## <a name="to-create-a-contact-manually"></a>So werden Kontakte manuell erstellt:
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Kontakte** ein, und wählen dann den zugehörigen Link aus.
2. Wählen Sie die Aktion **Neu** aus.
3. Geben Sie im Feld **Nr.** eine Nummer für den Kontakt ein.

    Wenn Sie auf der Seiter **Marketing und Vertrieb einrichten** eine Nummernserie für Kontakte eingegeben haben, können Sie alternativ auch die EINGABETASTE drücken, um die nächste verfügbare Kontaktnummer einzufügen.  
5. Füllen Sie die verbleibenden Felder je nach Bedarf aus. [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-create-a-contact-from-a-customer-vendor-or-bank-account"></a>So erstellen Sie einen Kontakt aus einem Debitor, Kreditor oder Bankkonto
Wenn Sie Debitoren, Kreditoren und Bankkonten haben, für die Sie Kontaktkarten erstellen möchten, können Sie die Stapelverarbeitungen **Kontakte aus Debitoren/Kreditoren/Bankkonten erstellen** verwenden, um Kontakte auf der Basis von bestehenden Daten zu erstellen. Wenn Sie einen Kontakt auf diese Weise erstellen, werden die Kontaktinformationen anschließend mit den verbundenen Debitoren-, Kreditoren- oder den Bankkontoinformationen synchronisiert. Weitere Informationen finden Sie unter [Synchronisieren von Kontakten mit Debitoren, Kreditoren und Bankkonten](marketing-create-contact-companies.md#synchronizing-contacts-with-customers-vendors-and-bank-accounts).

> [!NOTE]  
> Bevor Sie Kontakte basierend auf vorhandenen Daten erstellen können, müssen Sie einen Geschäftsbeziehungscode für Debitoren, Kreditoren und Bankkonten auf dem Inforegister **Interkationen** auf der Seite **Marketingeinrichtung** angeben. Weitere Informationen finden Sie unter [Einrichten von Kontakten](marketing-setup-contacts.md).

1. Wählen Sie ![Glühlampe, die die Funktion "Teilen Sie mir mit, was Sie tun wollen"](media/ui-search/search_small.png "\"Teilen Sie mir mit, was Sie tun wollen\"") und Folgendes ein, je nachdem, von wo aus Sie Kontakte erstellen möchten, und wählen Sie dann den zugehörigen Link aus.
   * **Kontakte aus Debitoren erstellen**
   * **Kontakte aus Kreditoren erstellen**
   * **Kontakte aus Bankkonten erstellen**
2. Legen Sie auf der geöffneten Anforderungsseite in den Abschnitten **Debitor**, **Kreditor** oder **Bankkonto** die Filter fest, wenn Sie Kontakte aus bestimmten Debitoren, Kreditoren oder Bankkonten erstellen möchten.
3. Klicken Sie auf die Schaltfläche **OK**, um mit dem Erstellen von Kontakten zu beginnen.

Den neuen Kontakten werden die nächsten Kontaktnummern aus der Nummernserie zugewiesen. Den neu erstellten Kontakten wird automatisch die Geschäftsbeziehung zugewiesen, die auf der Seite **Marketing & Vertrieb Einr.** festgelegt wurde.

> [!TIP]  
> Sie können dies auch andersherum tun, z. B. indem Sie einen Debitor, einen Kreditor oder ein Bankkonto aus einem Kontakt erstellen. Weitere Informationen finden Sie unter [So erstellen Sie einen Kontakt als Debitor, Kreditor oder Bankkonto](marketing-create-contact-companies.md#to-create-a-contact-as-a-customer-vendor-or-bank-account).

## <a name="synchronizing-contacts-with-customers-vendors-and-bank-accounts"></a>Synchronisieren von Kontakten mit Debitoren, Kreditoren und Bankkonten
Wenn einige Ihrer Kontakte auch Debitoren, Kreditoren oder Bankkonten sind, können Sie deren Kontaktinformationen mit dem entsprechenden Debitor, Kreditor oder Bankkonto synchronisieren.

Die folgenden Vorteile existieren, wenn ein Kontakt mit einem Debitor, Kreditor oder einem Bankkonto synchronisiert wird.

* Sie müssen die Informationen nur an einer Stelle aktualisieren. Wenn Sie z. B. die Telefonnummer auf des Kontakts ändern, wird die Telefonnummer auf des Debitors-, Kreditors oder Bankkontos automatisch mit der gleichen Änderung aktualisiert.
* Wenn Sie beim Erstellen einer Debitoren-, Kreditoren- oder Bankkontokarte eine Nummernserie für Kontakte angegeben haben, wird automatisch eine Kontaktkarte für den Debitor, den Kreditor bzw. das Bankkonto erstellt.
* Über den Kontakt können Sie Verkaufsofferten und -Aufträge, Einkaufsanfragen und -Aufträge erstellen.
* Sie können Ihre Aktivitäten beim Durchführen von Aktionen erfassen lassen, z. B. das Drucken von Aufträgen oder Rahmenbestellungen, Erstellen von Verkaufsserviceaufträgen, Senden von E-Mails usw.
* Wenn Sie einen Kontakt löschen, der mit einem Debitor, Kreditor oder Bankkonto verknüpft ist, wird nur der Kontakt entfernt. Der Debitor, Kreditor oder das Bankkonto bleibt erhalten.
* Wenn Sie einen Debitor, einen Kreditor oder ein Bankkonto löschen, der bzw. das mit einem Kontakt verknüpft ist, bleibt der Kontakt erhalten.

> [!NOTE]  
> Bestimmte Informationen, wie Fakturierungs- und Buchungsdetails, erscheinen nicht auf der Kontaktkarte. Sie können sie manuell auf der Debitoren-, Kreditoren- und/oder Bankkontenkarte hinzufügen, wenn Sie Kontakte als Debitoren, Kreditoren oder Bankkonten erstellen.

Die Synchronisierung von allgemeinen Daten zwischen Kontakten und den entsprechenden Debitoren, Kreditoren oder Bankkonten wird auf drei Arten ausgeführt:

* Wenn Sie Kontakte mit bestehenden Debitoren, Kreditoren und/oder Bankkonten von der Kontaktkarte verknüpfen. Siehe auch [Verknüpfen eines Kontakts mit einem vorhanden Debitor, Kreditor oder Konto](marketing-create-contact-companies.md#to-link-a-contact-to-an-existing-customer-vendor-or-bank-account).
* Wenn Sie Debitoren, Kreditoren oder Bankkonten aus Kontakten erstellen. Siehe auch [So erstellen Sie einen Kontakt aus einem Debitor, Kreditor oder Bankkonto](marketing-create-contact-companies.md#to-create-a-contact-from-a-customer-vendor-or-bank-account).
* Wenn Sie Kontakte als Debitoren, Kreditoren oder Bankkonten erstellen. Siehe auch [So erstellen Sie einen Kontakt als Debitor, Kreditor oder Bankkonto](marketing-create-contact-companies.md#to-create-a-contact-as-a-customer-vendor-or-bank-account).

## <a name="to-link-a-contact-to-an-existing-customer-vendor-or-bank-account"></a>Verknüpfen eines Kontakts mit einem vorhanden Debitor, Kreditor oder Konto
Wenn Sie einen Kontakt und entweder einen Debitor, Kreditor oder ein Bankkonto für das gleiche Unternehmen haben, können Sie die beiden Einheiten verknüpfen, sodass die allgemeinen Daten synchronisiert werden.

1. Öffnen Sie den Kontakt, den Sie verknüpfen möchten.
2. Wählen Sie die Aktion **Mit vorhandenem verknüpfen** aus, und wählen Sie dann die Aktion **Debitor**, **Kreditor** oder **Bank**.
3. Wählen Sie auf der geöffneten Seite den Debitor, Kreditor oder das Bankkonto für die Verknüpfung aus.
4. Legen Sie im Feld **Felder übernehmen von** fest, welche Felder im Konfliktfall Priorität haben sollen. Wenn sich z. B. der Verkäufercode von der Debitorenkarte von dem auf der Kontaktkarte unterscheidet, können Sie entscheiden, dass der von der Kontaktkarte genommen werden soll, indem Sie **Kontakt** auswählen.
5. Wählen Sie die Schaltfläche **OK** aus.

## <a name="to-create-a-contact-as-a-customer-vendor-or-bank-account"></a>So erstellen Sie einen Kontakt als Debitor, Kreditor oder Bankkonto
Wenn Sie einen Debitor, Kreditor oder eine Bank für das Unternehmen haben, für das Sie einen Kontakt erstellen möchten, können Sie die Funktion **Erstellen als** verwenden. Wenn Sie einen Kontakt auf diese Weise erstellen, werden die Kontaktinformationen anschließend mit den verbundenen Debitoren-, Kreditoren- oder den Bankkontoinformationen synchronisiert. Weitere Informationen finden Sie unter [Synchronisieren von Kontakten mit Debitoren, Kreditoren und Bankkonten](marketing-create-contact-companies.md#synchronizing-contacts-with-customers-vendors-and-bank-accounts).

> [!NOTE]  
> Bevor Sie Debitoren, Kreditoren oder Bankkonten aus Kontakten erstellen können, müssen Sie einen Geschäftsbeziehungscode für Debitoren, Kreditoren und Bankkonten auf dem Inforegister **Interkationen** auf der Seite **Marketingeinrichtung** angeben. Weitere Informationen finden Sie unter [Einrichten von Kontakten](marketing-setup-contacts.md).

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Kontakte** ein, und wählen dann den zugehörigen Link aus.
2. Wählen Sie den Kontakt aus, den Sie als Debitor, Kreditor oder Bankkonto erstellen möchten.
3. Wählen Sie die Aktionen **Erstellen als**, und wählen Sie denn entweder **Debitor**, **Kreditor** oder **Bank**.
4. Wählen Sie die Schaltfläche **OK** aus.

Die Kontaktinformationen werden von der Kontaktkarte auf eine neue Debitoren-, Kreditoren- oder Bankkontenkarte übertragen. Sie können den einzelnen Karten spezifische Informationen, wie Fakturierungs- und Zahlungsdetails hinzufügen. Weitere Informationen finden Sie unter [Neue Debitoren registrieren](sales-how-register-new-customers.md).

## <a name="see-also"></a>Siehe auch
[Kontakte verwalten](marketing-contacts.md)  
[Kontakte einrichten](marketing-setup-contacts.md)  
[Arbeiten mit Business Central](ui-work-product.md)
