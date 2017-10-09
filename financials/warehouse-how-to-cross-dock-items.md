---
title: "Vorgehensweise: Crossdock für Artikel | Microsoft Docs"
description: "Die Crossdocking-Funktionalität ist verfügbar, wenn Sie Ihren Lagerort so eingerichtet haben, dass die Bearbeitung des Wareneingangs und der Einlagerung erforderlich ist."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/23/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 5e167129e8a8bc5f10a0f9de4c384c06de030bbb
ms.contentlocale: de-ch
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-cross-dock-items"></a>Vorgehensweise: Crossdocking von Artikeln
Die Crossdocking-Funktionalität ist verfügbar, wenn Sie Ihren Lagerort so eingerichtet haben, dass die Bearbeitung des Wareneingangs und der Einlagerung erforderlich ist.  

Wenn Sie Crossdocks für Artikel durchführen, nehmen Sie sie an und liefern sie aus, ohne sie zwischendurch einzulagern, wodurch sich der Prozess der Einlagerung und Kommissionierung beschleunigt und die Bewegung der Artikel begrenzt wird. Crossdock für Artikel kann sowohl für den Warenausgang als auch für Fertigungsaufträge ausgeführt werden. Wenn Sie einen Warenausgang vorbereiten oder Artikel für die Produktion kommissionieren und Sie Lagerplätze verwenden, kommissioniert die Anwendung automatisch die Artikel aus einem Crossdockinglagerplatz, bevor sie andere Lagerplätze berücksichtigt. Sie müssen im Crossdockbereich nachsehen, um festzustellen, ob die Artikel, die Sie benötigen, verfügbar sind, bevor Sie die Artikel aus ihrem normalen Lagerbereich holen.  

Wenn Sie Crossdocking-Mengen berechnet haben, werden Einlagerungszeilen für den Crossdocklagerplatz für Crossdocking-Berechnungen erzeugt, wenn Sie den Wareneingang buchen. Andere Einlagerungszeilen werden wie üblich erzeugt.  

Wenn Sie die zugeordneten Artikel sofort buchen möchten, um sie für die Kommissionierung verfügbar zu machen, müssen Sie ebenfalls eine Einlagerung für die anderen Artikel aus der Wareneingangszeile, nämlich die, die eingelagert werden müssen, erfassen. Wenn Crossdock nur für einige der Artikel der Wareneingangszeile ausgefüht wird, müssen Sie sich daher bemühen, die anderen Artikel so schnell wie möglich einzulagern. Alternativ dazu kann Ihre Lagerpolitik so aussehen, dass Sie – wenn möglich – für ganze Wareneingangszeilen Crossdockings durchführen möchten.  

In der Einlagerungsanweisung können Sie zu Ihrem Vorteil Anweisungszeilen löschen (sowohl Zeilen der Art "Entnahme" als auch "Einlagerung" für jede Wareneingangszeile), die Wareneingänge betreffen, die vollständig eingelagert werden sollen. Diese Zeilen können später als Einlagerungszeilen aus dem Einlagerungsvorschlag oder dem gebuchten Wareneingang erzeugt werden. Wenn sie gelöscht sind, können Sie die Zeilen, die Crossdockartikel betreffen, einlagern und registrieren.  

Wenn Sie das Feld **Einlagerungsvorschl. verwenden** auf der Lagerortkarte ausgewählt und den Wareneingang mit berechneten Crossdockings gebucht haben, werden alle Wareneingangszeilen im Vorschlag verfügbar. Die Informationen zum Crossdock sind verloren und können nicht wiederhergestellt werden. Wenn Sie daher die Crossdocking-Funktionalität nutzen möchten, sollten Sie Zeilen in den Einlagerungsvorschlag übertragen, indem Sie Einlagerungsanweisungen löschen, anstatt die automatische Übertragungsfunktion im Feld **Einlagerungsvorschl. verwenden** zu nutzen.  

Wenn Sie den Wareneingang buchen, und sich kein Häkchen im Feld **Einlagerungsvorschl. verwenden** befindet, erscheinen die Artikel, für die Crossdockings durchgeführt werden sollen, als einzelne Zeilen in der Einlagerungsanweisung. Das Feld **Crossdockinformation** in jeder Einlagerungszeile zeigt an, ob die Zeile zugeordnete Artikel, Artikel aus demselben Wareneingang, die alle eingelagert werden sollen, oder Artikel, die eingelagert werden sollen und aus einer Wareneingangszeile stammen, in der einige Artikel zugeordnet werden sollen, enthält. Mit diesem Feld können die Mitarbeiter schnell sehen, warum nicht die volle Menge eingelagert werden soll.  

Die Anwendung speichert keine eigenen Datensätze über Artikel, für die Crossdockings durchgeführt wurden, sondern erfasst sie als normale Einlagerungsanweisungen.  

## <a name="to-set-up-the-warehouse-for-cross-docking"></a>So richten Sie die Logistik für Crossdockings ein:  
1.  Richten Sie mindestens einen Crossdocklagerplatz ein, wenn Sie Lagerplätze verwenden. Richten Sie eine Crossdockzone ein, wenn Sie die gesteuerte Einlagerung und Kommissionierung verwenden.  

    Bei einem Crossdocklagerplatz ist das Feld **Crossdocklagerplatz** ausgewählt, und es müssen die Lagerplatzarten **Wareneingang** und **Kommissionierung** ausgewählt sein. Weitere Informationen finden Sie unter [Vorgehensweise: Erstellen von Lagerplätzen](warehouse-how-to-create-individual-bins.md) und [Vorgehensweise: Lagerplatzarten einrichten](warehouse-how-to-set-up-bin-types.md).  

    Wenn Sie Zonen verwenden, erstellen Sie eine Zone für Ihre Crossdocklagerplätze, und wählen Sie das Feld **Crossdocklagerplatzzone** aus. Weitere Informationen finden Sie unter [Vorgehensweise: Einrichten von Lagerplätzen](warehouse-how-to-set-up-locations-to-use-bins.md).  

2.  Wählen Sie das Symbol ![Nach Seite oder Bericht suchen] (media/ui-search/search_small.png "Nach Seite oder Bericht suchen") aus und geben Sie **Lagerplätze** ein. Wählen Sie dann den zugehörigen Link aus.  
3.  Öffnen Sie das Fenster **Lagerort**, und wählen Sie den Lagerort aus, den Sie für das Lager bezüglich Zuordnungen einrichten möchten, und wählen Sie die Aktion **Bearbeiten** aus.  
4.  Wählen Sie im Inforegister **Lager** das Kontrollkästchen **Crossdocking verwenden** aus, und tragen Sie im Feld **Crossd.-Fälligkeitsdatum ber.** die Zeit für die Suche nach Crossdockmöglichkeiten ein.

    Die Option **Crossdocking verwenden** ist nur verfügbar, wenn die Felder **Wareneingang erforderlich**, **Warenausgang erforderlich**, **Kommissionierung erforderlich** und **Einlagerung erforderlich** ausgewählt sind.  

5.  Wenn Sie Lagerplätze verwenden, tragen Sie im Inforegister **Lagerplätze** in das Feld **Crossdocklagerplatzcode** den Code des Lagerplatzes ein, der als Vorgabelagerplatz für Zuordnungen verwendet werden soll.  
6.  Wählen Sie ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") aus und geben Sie **Lagerhaltungsdaten** ein und wählen Sie den zugehörigen Link aus.  
7.  Für jeden Artikel oder alle Lagerhaltungsdaten, die Sie zum Crossdocking verwenden möchten, wählen Sie den Artikel aus, und wählen Sie die **Bearbeiten** Aktion aus.
8. Im Fenster **Lagerhaltungsdatenkarte** wählen Sie das Kontrollkästchen **Zuordnung verwenden** aus.  

> [!NOTE]  
>  Crossdock ist nur möglich, wenn Ihr Lagerort so eingerichtet wurde, dass die Bearbeitung des Wareneingangs und der Einlagerung erforderlich ist.  

## <a name="to-cross-dock-items-without-viewing-the-opportunities"></a>So ordnen Sie Artikel zu, ohne sich die Möglichkeiten anzeigen zu lassen:  
1.  Wählen Sie ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Wareneingang** ein und wählen den entsprechenden Link aus.  
2.  Erstellen Sie Wareneingänge für einen Artikel, der angekommen ist und möglicherweise in Crossdockings einbezogen werden kann. Weitere Informationen finden Sie unter [Vorgehensweise: Wareneingang von Artikeln](warehouse-how-receive-items.md).  
3.  Füllen Sie das Feld **Zu liefernde Menge** aus, und wählen Sie dann die Aktion **Crossdocking berechnen** aus.  

    Ausgehende Herkunftsbelege, die die Artikel benötigen und die das Lager innerhalb der Datumsformelperiode verlassen sollen, werden identifiziert.  [!INCLUDE[d365fin](includes/d365fin_md.md)] berechnet Mengen, damit Sie soviel wie möglich zuordnen und auf diese Art vermeiden können, Artikel einzulagern, ohne zu viele Artikel im Crossdockbereich anzusammeln. Der Wert im Feld **Menge für Crossdocking** ist die Summe aller ausgehenden Zeilen, die den Artikel in der Vorausschauperiode benötigen, abzüglich der Menge der Artikel, die bereits in den Crossdockbereich eingelagert wurden. Oder es ist der Wert im Feld **Zu liefernde Menge** in der Lieferzeile, je nachdem, welcher geringer ist. Sie können nicht mehr Crossdockings durchführen, als Sie erhalten haben.  

4.  Wenn Sie für die Menge wie vorgeschlagen Crossdockings durchführen möchten, buchen Sie den Wareneingang. Sie können sich auch entscheiden, die zuzuordnende Menge auf einen höheren oder niedrigeren Wert zu setzen, und dann den Wareneingang zu buchen.  

    Die zuzuordnenden Mengen erscheinen jetzt als Zeilen in der Einlagerungsanweisung, vorausgesetzt, das Feld **Einlagerungsvorschl. verwenden** ist deaktiviert. Die nicht zugeordneten Mengen werden auch Zeilen in der Einlagerungsanweisung.  

    Wenn Sie Lagerplätze verwenden, wurden die zugeordneten Artikel dem Vorgabe-Crossdocklagerplatz zugeordnet, der auf der Artikelkarte festgelegt wurde.  

5.  Löschen Sie die Zeilen **Entnahme** und **Einlagerung** für Artikel, die nicht zugeordnet werden sollen.  
6.  Drucken Sie die Einlagerungsanweisungen für die übrigen Zeilen und lagern Sie die Mengen des Wareneingangs, die eingelagert werden sollen, in die jeweiligen Lagerplätze oder in einen geeigneten Bereich im Lager ein. Lagern Sie die Crossdockartikel in den Bereich oder Lagerplatz ein, der nach der Lagerpolitik für ihn vorgesehen ist. Es ist auch möglich, dass die Lagerrichtlinien vorsehen, dass Sie die Artikel einfach im Wareneingangsbereich lassen.  
7.  Wenn Sie zugeordnete Artikel als eingelagert und zum Kommissionieren registrieren möchten, wählen Sie die Aktion **Registrieren** aus.  

## <a name="to-cross-dock-items-after-viewing-the-opportunities"></a>So ordnen Sie Artikel zu, nachdem Sie die Verkaufschancen angezeigt haben:  
1.  Wählen Sie ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Wareneingang** ein und wählen den entsprechenden Link aus.  
2.  Erstellen Sie Wareneingänge für einen Artikel, der angekommen ist und möglicherweise in Crossdockings einbezogen werden kann. Weitere Informationen finden Sie unter [Vorgehensweise: Wareneingang von Artikeln](warehouse-how-receive-items.md).  

    Sie können sich die Herkunftsbelegzeilen ansehen, die den Artikel anfordern, bevor Sie den Wareneingang buchen.  
3.  Wählen Sie die Aktion **Crossdocking berechnen** aus.  

    Im Fenster **Crossdockmöglichkeiten** können Sie die wichtigsten Details zu den Zeilen sehen, die den Artikel benötigen, wie z. B. die Belegart, die erforderliche Menge und das Fälligkeitsdatum. Diese Informationen können Ihnen bei der Entscheidung helfen, wo Sie die Artikel im Crossdockbereich einlagern und wie Sie sie gruppieren.  

4.  Wählen Sie die Aktion **Menge für Crossdocking autom. ausfüllen** aus, um anzeigen zu lassen, wie die die Mengen in den Wareneingangszeilen berechnet werden. Wenn Sie die Anzahl der Artikel im Feld **Menge für Crossdocking** in den einzelnen Zeilen ändern, wird die Berechnung aktualisiert, während Sie Änderungen vornehmen. Dies bedeutet nicht, dass der spezielle Warenausgang oder Fertigungsauftrag tatsächlich die Artikel, die für das Crossdocking vorgeschlagen wurden, erhalten wird, da diese Veränderungen nur zu Testzwecken vorgenommen werden. Der Prozess kann jedoch informativ sein, wenn mehr als eine Einheit beteiligt ist.  
5.  Wenn Sie eine Menge für den Artikel einer bestimmten Auftragszeile reservieren möchten, setzen Sie Ihren Cursor in diese Zeile und wählen Sie dann die Aktion **Reservieren** aus. Im Fenster **Reservierung** können Sie jetzt eine verfügbare Menge des Artikels für diesen speziellen Auftrag reservieren. Diese Reservierung ist wie jede andere Reservierung und hat keine höhere Priorität, weil sie im Zusammenhang mit einem Crossdocking erstellt wurde. Weitere Informationen finden Sie unter [Vorgehensweise: Artikel reservieren](inventory-how-to-reserve-items.md).   
6.  Wenn Sie mit der Neuberechnung oder der Reservierung fertig sind, wählen Sie **OK**, um die überprüfte Berechnung in das Feld **Menge für Crossdocking** in der Wareneingangszeile zu bringen, oder klicken Sie auf **Abbrechen**, wenn Sie zum Wareneingang zurückkehren möchten, wo Sie das Crossdocking noch einmal berechnen können, wenn Sie möchten.  
7.  Buchen Sie jetzt den Wareneingang. Danach können Sie mit der Einlagerungsanweisung fortfahren, wie in den Schritten 3 bis 7 im Abschnitt "Um Artikel zuzuordnen, ohne sich die Möglichkeiten anzeigen zu lassen" beschrieben.  

> [!NOTE]  
>  In der Einlagerung können Sie fortfahren, die Mengen zu ändern – falls notwendig –, die eingelagert oder zugeordnet werden sollen. Sie können sich z. B. entscheiden, Crossdock für eine zusätzliche Menge auszuführen, um die Crossdockregistrierung zu beschleunigen.  

## <a name="to-view-cross-docked-items-in-a-shipment-or-pick-worksheet"></a>So zeigen Sie zugeordnete Artikel in Warenausgängen oder Kommissioniervorschlägen an:  
Wenn Sie Lagerplätze verwenden, können Sie jedes Mal, wenn Sie einen Warenausgang oder den Kommissioniervorschlag öffnen, eine aktualisierte Berechnung der Menge jedes Artikels in den Crossdocklagerplätzen sehen. Diese Information ist wertvoll, wenn Sie auf einen Artikel warten. Wenn Sie sehen, dass der Artikel in einem Crossdocklagerplatz verfügbar ist, können Sie schnell eine Kommissionierung für alle Artikel des Warenausgangs erstellen. Im Kommissioniervorschlag können Sie die Zeilen wie gewünscht ändern und dann eine Kommissionierung erstellen.  

Sie müssen die Artikel zuerst im Crossdockbereich suchen, wenn Sie Artikel für den Warenausgang kommissionieren. Wenn Sie sich beim Wareneingangsprozess die Herkunftsbelege notiert haben, die die Crossdockbasis waren, haben Sie einen besseren Überblick darüber, ob die Artikel im Crossdockbereich gefunden werden können oder nicht.  

Wenn ein Fertigungsauftrag freigegeben wurde, sind die Zeilen im Kommissioniervorschlag verfügbar und Sie können im Feld  **Menge in Crossdocklagerplätzen** sehen, ob die Artikel, auf die Sie warten, angekommen sind und in die zugeordneten Lagerplätze eingelagert wurden. Wenn Sie eine Kommissionieranweisung erstellen, schlägt die Anwendung vor, dass Sie zuerst die zugeordneten Artikel kommissionieren und erst dann in den festen Lagerplätzen nach weiteren Artikeln suchen.  

Wenn Sie keine Lagerplätze verwenden, müssen Sie daran denken, den Crossdockbereich von Zeit zu Zeit zu überprüfen, oder Sie müssen sich auf die Nachrichten aus dem Wareneingang verlassen, dass die Artikel für die Produktion angekommen sind.  

## <a name="see-also"></a>Siehe auch  
[Logistik](warehouse-manage-warehouse.md)  
[Lagerbesttand](inventory-manage-inventory.md)  
[Lagerortverwaltung einrichten](warehouse-setup-warehouse.md)     
[Montageverwaltung](assembly-assemble-items.md)    
[Designdetails: Logistik](design-details-warehouse-management.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
