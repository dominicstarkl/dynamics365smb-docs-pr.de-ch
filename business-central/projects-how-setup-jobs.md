---
title: Preise und Projektbuchungsgruppen einrichten| Microsoft Docs
description: Beschreibt, wie allgemeine Projektinformationen und Preise für Projektartikel, Ressourcen und Fibukonten und Projektbuchungsgruppen eingerichtet werden.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.workload: na
ms.search.keywords: project management
ms.date: 04/01/2019
ms.author: edupont
ms.openlocfilehash: 34dfdb463d3423d823b8f1439361d05296ca3c8a
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 03/31/2019
ms.locfileid: "918870"
---
# <a name="set-up-jobs"></a>Einrichten von Projekten

Als Projekt-Manager können Sie Projekte einrichten, die jedes der Projekte definieren, das Sie in [!INCLUDE [prodshort](includes/prodshort.md)] verwalten. Auf der Seite **Projekteinrichtung** müssen Sie festlegen, wie Sie bestimmte Projektfunktionen verwenden möchten.

Für jedes Projekt geben Sie dann die einzelnen Projektkarten mit Informationen zu Preisen für Projektressourcen Projektartikel, Projekt und Fibukonten an, und Sie müssen Projektbuchungsgruppen einrichten.

## <a name="to-set-general-information-for-jobs"></a>Um allgemeine Informationen für Projekte einzurichten:
1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Job einrichten** ein, und wählen dann den zugehörigen Link aus.
2. Füllen Sie die Felder je nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]
> Dies Auswirkungen des Felds **Verbrauchslink standardmäßig anwenden** sind sehr umfangreich und werden deshalb im folgenden Abschnitt erläutert.

### <a name="to-set-up-job-usage-tracking"></a>Projektverbrauch-Tracking einrichten

Wenn Sie ein Projekt erstellen, werden Sie wissen wollen, ob Ihr Verbrauch mit dem Plan übereinstimmt. Um diesen Vorgang zu vereinfachen, können Sie einen Link zwischen Ihren Projektplanungszeilen und dem tatsächlichen Verbrauch erstellen. So können Sie Ihre Kosten verfolgen und schnell sehen, wie viel Arbeit noch zu tun ist. Standardmäßig ist de Projektplanungszeilentyp **Plan**, aber die Verwendung der Zeilenart **Plan und fakturierbar** hat ähnliche Effekte.

Wenn Sie das Feld **Verbraucherlink standardmäßig anwenden** ausgewählt haben, können Sie die Projektplanungszeile überprüfen. Sie können die Menge der Ressource, des Artikels oder des Fibukontos einrichten und dann festlegen, welche Menge Sie in das Projekterfassungsjournal übertragen möchten. Das Feld **Restmenge** auf der Projektplanungszeile zeigt Ihnen an, was noch übertragen und im Erfassungsjournal gebucht werden muss.

> [!TIP]  
> Sie können Projektverbrauch-Tracking für ein bestimmtes Projekt aktivieren oder deaktivieren. Der Wert des Felds **Verbrauchslink anwenden** auf der neuen Projektkarte setzt die Einstellung auf der Seite **Projekteinrichtung** außer Kraft.  

Wenn das Kontrollkästchen **Verbrauchslink standardmäßig anwenden** aktiviert ist und die Projektplanungszeile auf **Fakturierbar** eingestellt ist, wird eine Projektplanungszeile vom Typ **Plan** erstellt, nachdem Sie eine Projekt-Erf.-Journalzeile gebucht haben.

> [!IMPORTANT]
> Wenn Projektverbrauch-Tracking aktiviert ist, entweder auf der Seite **Projekteinrichtung** oder im einzelnen Projekt, und das Feld **Projekttyp** in der Projektjournalzeile leer ist, dann werden die neuen Projektplanungszeilen der Zeilenart **Plan** erstellt, wenn Sie Projektjournalzeilen buchen.  
>  
> Wenn Projektverbrauch-Tracking *nicht* aktiviert ist, entweder auf der Seite **Projekteinrichtung** oder im einzelnen Projekt, und das Feld **Projekttyp** in der Projektjournalzeile leer ist, dann werden keine Projektplanungszeilen erstellt, wenn Sie Projektjournalzeilen buchen. Weitere Informationen finden Sie unter [Nutzung von Projekten](projects-how-record-job-usage.md).

1. Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Projekt einrichten** ein. Wählen Sie dann den zugehörigen Link aus.
2. Aktivieren sie das Kontrollkästen **Verbrauchslink standardmäßig anwenden**.

## <a name="to-set-up-prices-for-job-resources"></a>So richten Sie Verkaufspreise für Projektressourcen ein
Sie können bestimmte Verkaufspreise für Ressourcen für ein Projekt einrichten. Dazu verwenden Sie die Seite **Res.-VK-Preise Projekt**.

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Aufträge** ein, und wählen dann den zugehörigen Link aus.  
2. Wählen Sie die entsprechende Projekte und wählen Sie dann die Aktion **Ressource** aus.
3. Füllen Sie auf der Seite **Projektressourcen-Preise** die notwendigen Felder aus.

Die optionalen Informationen in den Feldern **Projektaufgabennr.**, **Arbeitstyp**, **Währungscode**, **Zeilenrabatt %** und **Einstandspreisfaktor** werden auf den Projektplanungszeilen und Verbrauchsbuchungsblättern verwendet, wenn diese Ressource eingegeben und dem Projekt hinzugefügt wird.  

Der Wert im Feld **Einheitspreis** für die Ressource wird in den Projektplanungszeilen und Projektbuchungsblättern verwendet, wenn diese Ressource, eine der Ressourcengruppe zugeordnete Ressource bzw. eine beliebige Ressource eingegeben wird.  

> [!NOTE]  
>   Dieser Preis hat immer Vorrang vor allen Preisen, auf der vorhandenen Seite des Typs **Ressourcen-VK-Preis/Ressourcengruppen-VK-Preise** eingerichtet sind.

## <a name="to-set-up-prices-for-job-items"></a>So richten Sie Preise für Projektartikel ein
Sie können bestimmte Preise für Artikel für ein Projekt einrichten. Dazu verwenden Sie die Seite **Projektartikelpreise**.

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Aufträge** ein, und wählen dann den zugehörigen Link aus.  
2. Wählen Sie die entsprechende Projekte und wählen Sie dann die Aktion **Artikel** aus.
3. Füllen Sie auf der Seite **Projektartikelpreise** die notwendigen Felder aus.

Die optionalen Informationen in den Feldern **Projektaufgabennummer**, **Währungscode** und **Zeilenrabatt %** werden in den Projektplanungszeilen und Projektbuchungsblättern verwendet, wenn dieser Artikel eingegeben wird.  

Dies ist der Wert im Feld **Einheitspreis** der in den Projektplanungszeilen und Projektbuchungsblättern verwendet wird, wenn dieser Artikel eingegeben wird.  

> [!NOTE]  
>   Dieser Preis hat immer Vorrang vor dem regulären Kundenpreis (Mechanismus für "bester Preis") für Artikel. Wenn Sie den Mechanismus für den regulären Kundenpreis verwendet wollen, erstellen Sie keine Projektartikelpreise für das Projekt.

## <a name="to-set-up-prices-for-job-general-ledger-accounts"></a>Preise für Projektbuchungskonten einrichten
Sie können bestimmte Preise für die Aufwandsfibuposten eines Projekts einrichten. Dazu verwenden Sie die Seite **Projekt-Fibukontopreise**.

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Aufträge** ein, und wählen dann den zugehörigen Link aus.  
2. Wählen Sie die entsprechende Projekte und wählen Sie dann die Aktion **Sachkonto** aus.  
3. Füllen Sie auf der Seite **Fibukonto-Preise** die notwendigen Felder aus.

Die optionalen Informationen in den Feldern **Projektaufgabennr.**, **Währungscode**, **Zeilenrabatt %**, **Einheitskostenfaktor** und **Einheitskosten** werden auf den Projektplanungszeilen und Verbrauchsbuchungsblättern verwendet, wenn diese Ressource eingegeben und dem Projekt hinzugefügt wird.  

Füllen Sie das Feld **Einheits-Preis** für das Aufwandssachkonto aus. Dies ist der Verkaufspreis, der in den Projektplanungszeilen und Projektbuchungsblättern verwendet wird, wenn dieses Sachkonto eingegeben wird.

## <a name="to-set-up-job-posting-groups"></a>Projektbuchungsgruppen einrichten
Ein Aspekt der Projektenplanung besteht darin, zu entscheiden, welche Buchungskonten für die Projektkalkulation verwendet werden. Damit Projekte gebucht werden können, müssen Sie Konten für die Buchung für jede Projektbuchungsgruppe einrichten. Eine Buchungsgruppe stellt eine Verknüpfung zwischen dem Projekt und der Art dar, wie es im Fibuposten zu behandeln ist. Wenn Sie ein Projekt erstellen, geben Sie eine Buchungsgruppe an, und standardmässig wird jede Aufgabe, die Sie erstellen, dieser Buchungsgruppe zugeordnet. Wenn Sie Aufgaben erstellen, können Sie jedoch die Voreinstellung überschreiben und eine Buchungsgruppe auswählen, die geeigneter ist.  

> [!NOTE]  
>   Die erforderlichen Konten der Kontenliste müssen eingegeben, bevor Sie Buchungsgruppen einrichten können. Weitere Informationen finden Sie unter [Einrichten oder ändern des Kontenplans](finance-setup-chart-accounts.md).  

1. Wählen Sie das Symbol ![Glühlampe, mit der die Funktion „Wie möchten Sie weiter verfahren“ geöffnet wird](media/ui-search/search_small.png "Wie möchten Sie weiter verfahren?") aus, geben Sie **Auftragsbuchungsruppen** ein, und wählen dann den zugehörigen Link aus.  
2. Wählen Sie die Aktion **Neu** und füllen Sie dann die Kontenfelder wie in der folgenden Tabelle beschrieben aus.  

| Das Feld "Konto" | Description |
| --- | --- |
| **Code** |Ein Code für die Buchungsgruppe. Sie können bis zu 10 Zeichen, einschliesslich Leerzeichen, eingeben. |
| **Konto f. Kosten n. abgs. Arb.** |Das WIP-Konto für die berechneten Kosten der Projekt-WIP, bei dem es sich um ein Bilanz-Aktivkonto für Kapital handelt. |
| **Konto f. aufgel. Kosten n. abgs. Arb.** |Ein Konto für die Methode "Einstandswert" oder "Vertriebskosten" der WIP-Berechnung, bei dem es sich um ein Bilanz-Passivkonto für aufgelaufene Ausgaben handelt. Auf dieses Konto wird gebucht, wenn die WIP-Regulierung eine Erhöhung der in der Erfolgsrechnung gebuchten Verbrauchskosten erfordert. |
| **Projektkostenausgleich-Konto** |Das Gegenkonto zum Konto für WIP-Kosten, bei dem es sich um ein Gegenkonto zu einem Konto für einen negativen Aufwand handelt. |
| **Konto für ausgeglichene Artikelpreise** |Das Gegenkonto zum Konto für WIP-Kosten, bei dem es sich um ein Gegenkonto zu einem Konto für einen negativen Aufwand handelt. |
| **Konto für ausgeglichene Ressourcenpreise** |Das Gegenkonto zum Konto für WIP-Kosten, bei dem es sich um ein Gegenkonto zu einem Konto für einen negativen Aufwand handelt. |
| **Kostenausgleich-Konto** |Das Gegenkonto zum Konto für WIP-Kosten, bei dem es sich um ein Gegenkonto zu einem Konto für einen negativen Aufwand handelt. |
| **Projektkostenregulierung-Konto** |Das Gegenkonto zum WIP-Konto für aufgelaufene Kosten, bei dem es sich um ein Aufwandskonto handelt. |
| **Aufwandssachkonto (Budget)** |Das Verkaufskonto, das für Aufwandsfibuposten in Projektaufgaben mit dieser Buchungsgruppe verwendet werden soll. Wenn dieses Feld leer gelassen wird, wird das für die Projektplanungszeile eingegebene Fibukonto verwendet. |
| **Konto f. aufgel. Verkäufe n. abgs. Arb.** |Das WIP-Konto für den berechneten Verkaufswert der WIP, bei dem es sich um ein Bilanzblatt für aufgelaufene Einnahmen handelt. Auf dieses Konto wird gebucht, wenn die WIP-Regulierung eine Erhöhung der deklarierten Einnahmen erfordert. |
| **Konto f. fakt. Verkäufe n. abgs. Arb.** |Das Konto für den fakturierten WIP-Verkaufswert, der nicht deklariert werden kann. Es handelt sich dabei um ein Bilanzblatt für nicht realisierte Einnahmen. |
| **Projektverkaufsausgleich-Konto** |Das Gegenkonto zum WIP-Konto für fakturierte Verkäufe, bei dem es sich um ein Ertragsgegenkonto handelt. |
| **Projektverkaufsregulierungs-** Konto |Das Gegenkonto zum WIP-Konto für den Umsatz, bei dem es sich um ein Ertragskonto handelt. |
| **Konto deklarierte Kosten** |Das Aufwandskonto, das die deklarierten Kosten für das Projekt enthält. Dabei handelt es sich normalerweise um ein Soll-Aufwandskonto. |
| **Konto deklarierte Verkäufe** |Das Ertragskonto, das den deklarierten Umsatz für das Projekt enthält. Dabei handelt es sich normalerweise um ein Haben-Ertragskonto. |

## <a name="see-also"></a>Siehe auch

[Projektmanagement einrichten](projects-setup-projects.md)  
[Video: So erstellen Sie ein Projekt in Dynamics 365 Business Central](https://www.youtube.com/watch?v=VqaPWr7BWmw)  
[Projekte verwalten](projects-manage-projects.md)  
[Finanzen](finance.md)  
[Einkauf](purchasing-manage-purchasing.md)  
[Verkauf](sales-manage-sales.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
