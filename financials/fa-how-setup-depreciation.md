---
title: Abschreibungsmethoden einrichten| Microsoft Docs
description: "Sie geben in einem Abschreibungsbuch an, wie Sie Anlagen abschreiben oder anzeigen möchten."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: write down
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 92331aaa8e7d6aa83c0ec9e8bbbd350d30957cfc
ms.contentlocale: de-ch
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-fixed-asset-depreciation"></a>Richten Sie eine neue Anlagenabschreibung ein
 Sie können unterschiedliche Abschreibungsmethoden für Bilanzen und Steuern verwenden. Viele Grossunternehmen verwenden die lineare Abschreibung in ihren Bilanzen, da dies im Allgemeinen höhere Gewinne anzeigt. Für steuerliche Zwecke verwenden viele Unternehmen beschleunigte Abschreibungsmethoden. Weitere Informationen finden Sie unter [AfA-Methoden](fa-depreciation-methods.md).

 Nachdem Sie die erforderlichen AfA-Bücher erstellt haben, müssen Sie jeder Anlage mindestens ein AfA-Buch zuweisen. Ein Abschreibungsbuch, das einer Anlage zugewiesen ist, wird als Anlagen-Abschreibungsbuch bezeichnet. Entsprechend wird das Fenster für zugewiesene AfA-Bücher **Anlagen-AfA-Bücher** genannt.

## <a name="to-create-a-depreciation-book"></a>So erstellen Sie ein Anlagen-Abschreibungsbuch
In einem Abschreibungsbuch können Sie festlegen, wie eine Anlage abgeschrieben wird. Sie können mehrere Abschreibungsbücher einrichten, um die verschiedenen Abschreibungsarten zu erleichtern.  

1. Wählen Sie in der rechten oberen Ecke ![Nach Seite oder Bericht suchen]das Symbol (media/ui-search/search_small.png "")Nach Seite oder Bericht suchen und geben **AfA-Buchliste** ein. Wählen Sie dann den zugehörigen Link aus.
2. Im Feld **AfA-Bücher Übersicht** wählen Sie die Aktion **Neu** aus.
3. Füllen Sie im Fenster **AfA-Buch-Karte** die Felder nach Bedarf aus. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
>   Hinweis: Sie können Anlagentransaktionen im Fenster **Anlagen Fibu Buch.-Blatt** oder im Fenster **Anlagen Buch - Blatt** erfassen, abhängig davon, ob die Transaktionen für Finanzberichte oder zur internen Verwaltung bestimmt sind. Führen Sie den nächsten Schritt aus, um festzulegen, welche Art von Erf.-Journal für die verschiedenen Anlagenaktivitäten standardmässig verwendet wird.
4. Aktivieren Sie im Inforregister **Integration** das Kontrollkästchen für jede Anlagenaktivität, deren Transaktionen Sie mithilfe des Fensters **Anlagen Fibu Buch.-Blatt** buchen möchten.
5. Wiederholen Sie die Schritte 2 bis 4 für jede Abschreibungs- oder Buchungsmethode, die Sie den Anlagen als Abschreibungsbuch zuweisen möchten.

## <a name="to-assign-a-depreciation-book-to-a-fixed-asset"></a>So verknüpfen Sie ein Abschreibungsbuch mit einer Anlage
1. Alternativ wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Anlagen** ein. Wählen Sie dann den zugehörigen Link aus.
2. Wählen Sie die Anlage aus, für die Sie ein Anlagen-Abschreibungsbuch einrichten möchten.
3. Füllen Sie im Inforegister **AfA-Buch** die Felder nach Bedarf aus.
4. Wenn Sie mehrere AfA-Bücher der Anlage zuweisen müssen, wählen Sie die Aktion **Weitere AfA-Bücher hinzufügen** aus.
5. Alternativ wählen Sie die Aktion **AfA-Bücher** aus , um eine oder mehrere Anlagen-AfA-Bücher anzugeben.

    > [!NOTE]  
>   Hinweis: Wenn Sie die manuelle Abschreibungsmethode verwenden, müssen Sie die Abschreibung manuell im Anlagen Fibu Erf.-Journal eingeben. Die Funktion **AfA berechnen** berücksichtigt keine Anlagen mit der AfA-Methode "Manuell". Sie können diese Methode für Anlagen verwenden, die nicht abgeschrieben werden, wie z. B. Land.

## <a name="to-assign-a-depreciation-book-to-multiple-fixed-assets-with-a-batch-job"></a>So weisen Sie ein Abschreibungsbuch mehreren Anlagen mit einer Stapelverarbeitung zu
Falls Sie ein AfA-Buch mit mehreren Anlagen verknüpfen möchten, können Sie die Stapelverarbeitung **Anlagen-AfA-Buch erstellen** verwenden, um die Anwendung die erforderlichen AfA-Bücher automatisch erstellen zu lassen.  

1. Alternativ wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Anlagen** ein. Wählen Sie dann den zugehörigen Link aus.
2. Wählen Sie die Anlage aus, die Sie einrichten möchten und der ein AfA-Buch zugewiesen werden soll, und wählen Sie dann die Aktion **Bearbeiten** aus.
3. Wählen Sie im Fenster **AfA-Buch - Karte** die Aktion **Anlagen-AfA-Bücher erstellen** aus.
4. Füllen Sie im Fenster **Anlagen-AfA-Buch erstellen** das Fenster **AfA-Buch** aus.
5. Klicken Sie im Feld **Kopieren von Anl.-Nr.** auf den AssistButton, und wählen Sie dann die Nummer der Anlage, die Sie als Basis für neue Abschreibungsbücher verwenden möchten.

    Wenn Sie dieses Feld ausfüllen, enthalten die Abschreibungsfelder in den neuen Anlagen-Abschreibungsbüchern die gleichen Informationen wie die entsprechenden Felder im Anlagen-Abschreibungsbuch, aus dem Sie kopieren. Lassen Sie dieses Feld leer, wenn Sie neue Anlagen-Abschreibungsbücher mit leeren Abschreibungsfeldern erstellen möchten.  
6. Im Inforegister **Anlage** können Sie einen Filter setzen, um die Anlagen auszuwählen, für die Sie Anlagen-AfA-Bücher erstellen wollen.
7. Wählen Sie die Schaltfläche **OK** aus.

## <a name="to-set-up-depreciation-posting-types"></a>So richten Sie Abschreibungsbuchungsarten ein:
Für jedes AfA-Buch müssen Sie festlegen, wie die verschiedenen Buchungsarten in [!INCLUDE[d365fin](includes/d365fin_md.md)] verarbeitet werden sollen. Beispielsweise ob Buchungen Soll- oder Habenposten sein sollen und ob die Buchungsart in der AfA-Grundlage enthalten sein soll.  

1. Wählen Sie in der rechten oberen Ecke ![Nach Seite oder Bericht suchen]das Symbol (media/ui-search/search_small.png "")Nach Seite oder Bericht suchen und geben **AfA-Buchliste** ein. Wählen Sie dann den zugehörigen Link aus.  
2. Wählen Sie das AfA-Buch aus, die Sie einrichten möchten und wählen Sie dann die Aktion **Anlagenbuchungsart Einr.** aus.
3. Füllen Sie im Fenster **Anlagenbuchungsart Einr.** die notwendigen Felder aus.

    > [!NOTE]  
>   Sie können in dem Fenster **Anlagenbuchungsart Einr.** keine Zeilen löschen oder einfügen. Sie können nur die bestehenden Zeilen ändern.

    Es wird empfohlen, die Einrichtung von AfA-Büchern, für die bereits Posten gebucht wurden, nicht zu ändern. Änderungen haben keinen Einfluss auf Posten, die bereits gebucht wurden, da andernfalls die Statistik für das Abschreibungsbuch verfälscht würde.

## <a name="to-set-up-default-templates-and-batches-for-fixed-asset-depreciation"></a>So richten Sie Standardvorlagen und -Standardstapelverarbeitungen für Anlagen-Abschreibung ein
Sie können für jedes Abschreibungsbuch Vorgaben für Vorlagen und Erfassungsjournalen definieren. Sie nutzen diese Standards, um Zeilen aus einem Buch.-Blatt in ein anderes zu kopieren, wenn die Batchaufträge **AfA berechnen** oder **Anlagen indexieren** Buch.-Blattzeilen erstellen oder wenn Anschaffungskosten im Versicherungs Buch.-Blatt doppelt vorhanden sind.  

1. Wählen Sie in der rechten oberen Ecke ![Nach Seite oder Bericht suchen]das Symbol (media/ui-search/search_small.png "")Nach Seite oder Bericht suchen und geben **AfA-Buchliste** ein. Wählen Sie dann den zugehörigen Link aus.  
2. Wählen Sie das AfA-Buch aus, für das Sie die Standardbuch.-Blätter festlegen möchten und wählen Sie dann die Aktion **Anlagen Buch.-Blatt Einr.** aus.  
3. Falls Sie eine Standardeinrichtung für jeden einzelnen Benutzer definieren möchten, wählen Sie das Feld **Benutzer-ID** aus, um über das Fenster **Benutzer** auszuwählen.  
4. Wählen Sie in den anderen Feldern die Erf.-Journalvorlage oder den Erf.-Journalnamen, die standardmässig verwendet werden müssen.  

## <a name="see-also"></a>Siehe auch
[Anlagen einrichten](fa-setup.md)  
[Anlagen](fa-manage.md)  
[Finanzen](finance.md)  
[Willkommen bei [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
