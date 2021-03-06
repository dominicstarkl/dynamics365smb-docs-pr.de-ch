---
title: Verwalten von Debitoren mit Dynamics 365 for Sales| Microsoft Docs
description: Sie können Dynamics 365 for Sales aus Business Central nutzen, um Daten zu verknüpfen und eine nahtlose Integration und Synchronisation der führenden Prozesse sicherzustellen.
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: integration, synchronize, map, Sales
ms.date: 04/01/2019
ms.author: bholtorf
ms.openlocfilehash: 30396e25dbf251e674744d1ba797c100b5762a46
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 03/31/2019
ms.locfileid: "915204"
---
# <a name="using-dynamics-365-for-sales-from-business-central"></a>Verwenden von Dynamics 365 for Sales aus Business Central heraus
Wenn Sie Dynamics 365 for Sales für Customer Engagement verwenden, können Sie nahtlose Integration in den Interessent-zu-Geld-Prozess nutzen, indem Sie [!INCLUDE[d365fin](includes/d365fin_md.md)] für Backend-Aktivitäten wie Auftragsverarbeitung, Lagerbestandsverwaltung und Finanzbearbeitung verwenden.

> [!NOTE]
> In diesem Thema wird davon ausgegangen, dass die Onlineversionen von [!INCLUDE[d365fin](includes/d365fin_md.md)] and Sales verwenden. Sie können online und lokale Versionen kombinieren, doch dafür ist besondere Konfiguration erforderlich. Weitere Informationen finden Sie unter [Vorbereiten der Integration in Dynamics 365 for Sales lokal](/dynamics365/business-central/dev-itpro/administration/prepare-dynamics-365-for-sales-for-integration).

Die Integration der Anwendungen ermöglicht den Zugriff auf Daten in Sales von [!INCLUDE[d365fin](includes/d365fin_md.md)] aus und in einigen Fällen auch umgekehrt. Sie können mit Datentypen, die bei beiden Diensten gleich sind, arbeiten und diese synchronisieren. Dazu zählen etwa Debitoren, Kontakte und Verkaufsinformationen. Außerdem können Sie die Daten an beiden Anwendungen auf dem aktuellen Stand halten.  

Beispielsweise kann ein Verkäufer in Sales die Preislisten verwenden aus [!INCLUDE[d365fin](includes/d365fin_md.md)] wenn Sie einen Verkaufsauftrag erstellen. Wenn Artikel in der Verkaufsauftragszeile in Sales hinzugefügt werden, sind sie in der Lage, den Lagerbestand (Verfügbarkeit) des Artikels anzuzeigen von [!INCLUDE[d365fin](includes/d365fin_md.md)].

Andererseits können Auftragsbearbeiter in [!INCLUDE[d365fin](includes/d365fin_md.md)] Verkaufsaufträge verarbeiten, die automatisch oder manuell vom Vertrieb übertragen werden. Beispielsweise können sie Verkaufsauftragszeilen für Artikel oder Ressourcen erstellen und buchen, die in Sales als einzutragende Produkten eingegeben wurden. Weitere Informationen finden Sie im Abschnitt [Verarbeiten von Verkaufsauftragsdaten](marketing-integrate-dynamicscrm.md#handling-sales-order-data).

> [!IMPORTANT]  
> [!INCLUDE[d365fin](includes/d365fin_md.md)] kann nur in Dynamics 365 for Sales integriert werden. Andere Dynamics 365, die den Standardworkflow oder das Datenmodell in Sales ändern, zum Beispiel, Project Service Automation, können die Integration zwischen [!INCLUDE[d365fin](includes/d365fin_md.md)] und Sales unterbrechen.

### <a name="coupling-records"></a>Kopplungsdatensätze
Mit dem Leitfaden für das unterstütze Setup können Sie die zu synchronisierenden Daten auswählen. Später können Sie die Synchronisierung für bestimmte Datensätze einrichten. Dies wird als *Kopplung* bezeichnet. Beispielsweise können Sie ein bestimmtes Konto in Sales mit einem bestimmten Debitor in [!INCLUDE[d365fin](includes/d365fin_md.md)] koppeln. In diesem Abschnitt wird beschrieben, was berücksichtigt werden sollte, wenn Sie Datensätze koppeln.

Wenn Sie Konten in Sales als Debitor in [!INCLUDE[d365fin](includes/d365fin_md.md)] anzeigen möchten, müssen Sie die beiden Arten von Datensätzen koppeln. Dazu verwenden Sie auf der Listenseite **Debitoren** in [!INCLUDE[d365fin](includes/d365fin_md.md)] die **Kopplung einrichten**-Aktion. Dann legen Sie fest, welche [!INCLUDE[d365fin](includes/d365fin_md.md)]-Debitoren den Konten in Sales zugewiesen werden.

Sie können auch ein Konto in Sales erstellen (und koppeln), das zum Beispiel auf einem Debitorendatensatz in [!INCLUDE[d365fin](includes/d365fin_md.md)] basiert, wenn Sie **Konto in Dynamics 365 for Sales erstellen** verwenden, oder umgekehrt. Das ist mit **Debitor in [!INCLUDE[d365fin](includes/d365fin_md.md)] erstellen** möglich.

Wenn Sie eine Kopplung zwischen zwei Datensätzen einrichten, können Sie manuell anfordern, dass der aktuelle Datensatz, beispielsweise einen Debitor, sofort durch Kontodaten aus Sales (oder aus [!INCLUDE[d365fin](includes/d365fin_md.md)]) mithilfe der **Jetzt synchronisieren**-Aktion überschrieben werden. Die **Jetzt synchronisieren**-Aktion, die fragt, ob Sales oder [!INCLUDE[d365fin](includes/d365fin_md.md)]-Datensatzdaten überschrieben werden sollen.

In einigen Fällen müssen Sie projektspezifische Datenbestände vor anderen Datensätzen koppeln, wie in der folgenden Tabelle dargestellt.

|Daten|Was zuerst koppeln|
|-----|----|
|Debitoren und Konten|Verkäufer mit Sales-Benutzern koppeln|
|Artikel und Ressourcen|Maßeinheiten mit Sales-Einheitengruppe koppeln|
|Artikel und Ressourcenpreise|Debitorenpreisgruppen mit Verkaufspreisen koppeln|

> [!NOTE]  
> Wenn Ihre Preise oder Debitoren Fremdwährungen verwenden, stellen Sie sicher, dass Sie Währungen mit Sales-Transaktionswährungen koppeln.

In Sales hängen Verkaufsaufträge von Informationen wie Debitoren, Maßeinheiten, Währungen, Debitorenpreisgruppen, Artikeln und/oder Ressourcen ab. Damit Verkaufsaufträge arbeiten, müssen Sie Debitoren, Maßeinheiten, Währungen, Debitorenpreisgruppen, Artikel und/oder Ressourcen koppeln.

### <a name="fully-synchronizing-records"></a>Datensätze vollständig synchronisieren
Am Ende des Leitfaden für das unterstützte Setup können Sie die Aktion **Vollständige Synchronisierung ausführen** auswählen, um die Synchronisierung aller Datensätze mit allen [!INCLUDE[d365fin](includes/d365fin_md.md)] Datensätzen mit allen verknüpften Einträgen in Sales zu starten. Auf der Seite **Dynamics 365 for Sales – Überprüfung der vollständigen Synchronisierung** wählen Sie die Aktion **Starten** aus. Vollständige Synchronisierung kann einige Zeit dauern, aber Sie können in [!INCLUDE[d365fin](includes/d365fin_md.md)] weiterarbeiten, während sie im Hintergrund ausgeführt wird.

Um den Status aus einzelnen Projekte in einer vollständigen Synchronisierung zu prüfen, wählen Sie auf der Seite **Dynamics 365 for Sales – Überprüfen der vollständigen Synchronisierung** einen Datensatz, um Details anzeigen. Um den Status der Synchronisierung zu aktualisieren, aktualisieren Sie die Seite.

Auf der Seite **Microsoft Dynamics 365-Verbindungseinrichtung** können Sie Details über sämtliche Synchronisierungen sehen. Von hier können Sie die Seite **Integrationstabellenzuordnungen** auch öffnen, um Details über die Tabellen in [!INCLUDE[d365fin](includes/d365fin_md.md)] und Sales zu finden, die synchronisiert werden müssen.

## <a name="handling-sales-order-data"></a>Bearbeiten von Verkaufsauftragsdaten
Verkaufsaufträge, die Verkäufer in [!INCLUDE[crm_md](includes/crm_md.md)] einreichen, werden automatisch zu [!INCLUDE[d365fin](includes/d365fin_md.md)] übertragen, wenn Sie das Kontrollkästchen **Automatisches Erstellen von Verkaufsaufträgen** auf der Seite **Microsoft Dynamics 365-Verbindungseinrichtung** auswählen.
Alternativ können Sie eingereichte Verkaufsaufträge aus [!INCLUDE[crm_md](includes/crm_md.md)] mithilfe der Aktion **Erstellen in [!INCLUDE[d365fin](includes/d365fin_md.md)]**, die auf der Seite **Verkaufsaufträge - Dynamics 365 for Sales** verfügbar ist, manuell konvertieren.
In solchen Verkaufsaufträgen wird das **Name** Feld im ursprünglichen Auftrag dem Feld **Externe Belegnummer** im Verkaufsauftrag in [!INCLUDE[d365fin](includes/d365fin_md.md)] übertragen und zugeordnet.

Dies kann auch gehen, wenn der ursprüngliche Verkaufsauftrag geschriebene Produkte enthält, d.h. Artikel oder Ressourcen sind nicht in beiden Apps erfasst worden. In diesem Fall müssen Sie die Felder**Geschriebenen Produkttyp** und die **Geschriebene Produktnummer** ausfüllen auf der Seite **Debitoren & Verkauf Einr.**, damit solche nicht-registrierte Produktverkäufe in einem angegebenen Artikel/einer Ressourcennummer für Finanzanalyse zugeordnet werden.

Wenn die Artikelbeschreibung des ursprünglichen Verkaufsauftrags lang ist, wird eine zusätzliche Verkaufsauftragszeile der Art **Bemerkung** erstellt, um den Text in dem Verkaufsauftrag in [!INCLUDE[d365fin](includes/d365fin_md.md)]festzuhalten.

Aktualisierungen der Verkaufsauftrags-Kopffeldern, wie "Letztes Lieferdatum" oder "Gewünschtes Lieferdatum", die der VERKAUFSAUFTRAG-AUFTRAG-**Integrationstabellenzuordnung** zugeordnet sind, werden in regelmäßigen Abständen mit [!INCLUDE[crm_md](includes/crm_md.md)] synchronisiert. Arbeitsgänge wie das Freigeben eines Verkaufsauftrags und die Lieferung oder Fakturierung eines Verkaufsauftrags werden auf der Verkaufsauftragszeitachse in [!INCLUDE[crm_md](includes/crm_md.md)] gebucht. Weitere Informationen finden Sie unter [Einführung in die Aktivitätsfeeds](https://docs.microsoft.com/en-us/dynamics365/customer-engagement/developer/introduction-activity-feeds).

## <a name="handling-sales-quotes-data"></a>Bearbeiten von Verkaufsofferten
Verkaufsofferten, die in [!INCLUDE[crm_md](includes/crm_md.md)] aktiviert werden, werden automatisch zu [!INCLUDE[d365fin](includes/d365fin_md.md)] übertragen, wenn Sie das Kontrollkästchen **Automatisches Verarbeiten von Offerten** auf der Seite **Microsoft Dynamics 365-Verbindungseinrichtung** auswählen.
Alternativ können Sie aktivierte Verkaufsofferten aus [!INCLUDE[crm_md](includes/crm_md.md)] mithilfe der Aktion **Verarbeiten in [!INCLUDE[d365fin](includes/d365fin_md.md)]** auf der Seite **Verkaufsofferten - Dynamics 365 for Sales** manuell konvertieren.
In solchen Verkaufsofferten wird das **Name**-Feld in der ursprünglichen Offerte dem Feld **Externe Belegnummer** im Verkaufsauftrag in [!INCLUDE[d365fin](includes/d365fin_md.md)] übertragen und zugeordnet. Auch wird das Feld **Gültig bis** beim Offerte übertragen und dem Feld **Offerte gültig bis** auf der Verkaufsofferte in [!INCLUDE[d365fin](includes/d365fin_md.md)] zugeordnet.  

Verkaufsofferten unterliegen vielen Überarbeitungen, bis sie abgeschlossen werden. Manuelle und automatische Verarbeitung von Verkaufsofferten in [!INCLUDE[d365fin](includes/d365fin_md.md)] stellt sicher, dass vorherige Versionen von Verkaufsanfragen archiviert werden, bevor neue Überarbeitungen von Verkaufsanfragen von [!INCLUDE[crm_md](includes/crm_md.md)] verarbeitet werden.  

## <a name="see-also"></a>Siehe auch
[Vorbereiten der Integration in Dynamics 365 for Sales On-Premises](/dynamics365/business-central/dev-itpro/administration/prepare-dynamics-365-for-sales-for-integration)  
[Marketing & Vertrieb](marketing-relationship-management.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Sie können auswählen, welche Funktionen angezeigt werden](ui-experiences.md)  
[Benutzer und ihre Berechtigungen verwalten](ui-how-users-permissions.md)    
[Holen Sie Ihre Organisation und Benutzer zu Dynamics 365 (online)](/dynamics365/customer-engagement/admin/onboard-your-organization-and-users-to-dynamics-365-online)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
