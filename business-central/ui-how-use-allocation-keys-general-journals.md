---
title: "Verwenden von Umlageschlüsseln in Fibu Buch.-Blättern | Microsoft Docs"
description: "Erfahren Sie, wie Sie Verteilungsschlüssel in Buch.-Blättern verwenden können."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cost accounting
ms.date: 03/29/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 29a55ec7b0e9b7c625b81361cc5e2e028dc5e3f5
ms.contentlocale: de-ch
ms.lasthandoff: 03/22/2018

---
# <a name="use-allocation-keys-in-general-journals"></a>Verwenden von Umlageschlüsseln in Fibu Buch.-Blättern
Die Posten einer Fibu Erf.-Journalzeile lassen sich beim Buchen des Erf.-Journals auf verschiedene Konten verteilen. Die Verteilung kann nach Anzahl, Prozent oder Betrag vorgenommen werden.

## <a name="to-set-up-allocation-keys"></a>Einrichten von Verteilungsschlüsseln
1. Alternativ wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben die **Wiederkehrendes Buch-Blatt** ein. Wählen Sie dann den zugehörigen Link aus.
2. Wählen Sie im Fenster **Fibu Erf.-Journalnamen** den **Erfassungsjournalnamen**.
3. Sie können entweder Zuordnungen in einer vorhandene Charge in der Liste ändern oder eine neue Charge mit Zuordnungen erstellen.
   * Um eine neue Chargennummer zu erstellen, wählen Sie die Aktion **Neu** und gehen Sie zum nächsten Schritt.
   * Um die Zuordnungen eines vorhandenen Erfassungsjournals zu ändern, wählen Sie das Erfassungsjournal und gehen Sie zum Schritt 7.    
4. Geben Sie im Feld **Name** einen Namen für das Buch.-Blatt ein, wie beispielsweise REINIGUNG. Geben Sie im Feld **Beschreibung** eine Beschreibung ein, wie z. B. Reinigungsausgaben Erfassungsjournal.
5. Wenn Sie fertig sind, schliessen Sie das Fenster. Ein neues, leeres wiederkehrendes Erfassungsjournal wird geöffnet.
6. Füllen Sie die Felder in der Zeile aus.
7. Wählen Sie die Aktion **Verteilung** aus.
8. Erstellen Sie für jede Verteilung eine Zeile. Sie müssen entweder das Feld **Verteilung %**, **Anzahl Verteilungen** oder **Betrag** ausfüllen. Sie müssen ebenfalls das Feld **Kontonr.** ausfüllen und, wenn Sie auf globale Dimensionen verteilen, auch die Felder "globale Dimensionen".
9. Wenn Sie in der Zeile einen Prozentsatz eingeben, wird der Betrag im Feld **Betrag** automatisch berechnet. Diese Beträge haben das gegenteilige Vorzeichen von dem Gesamtbetrag im Feld **Betrag** des wiederkehrenden Erfassungsjournals.
10. Nachdem Sie die Zuteilungszeilen eingegeben haben, wählen Sie **OK** aus, um zum Fenster **Wiederk. Fibu Erf.-Journal** zurückzukehren. Das Feld **Zugewiesener Betrag (USD)** ist ausgefüllt und entspricht dem Feld **Betrag**.
11. Buchen Sie die Erf.-Journalzeile.

## <a name="to-change-an-allocation-key-that-has-already-been-set-up"></a>Ändern eines bereits eingerichteten Umlageschlüssels
1. Alternativ wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben die **Wiederkehrendes Buch-Blatt** ein. Wählen Sie dann den zugehörigen Link aus.
2. Wählen Sie im Fenster **Wiederk. Fibu Erfassungsjournal** das Erfassungsjournal mit der Verteilung aus.
3. Wählen Sie die Zeile mit der Verteilung, und wählen Sie dann die Aktion **Zuweisungen** aus.
4. Ändern Sie die relevanten Felder und wählen Sie dann die Schaltfläche **OK** aus.

## <a name="see-also"></a>Siehe auch
[Arbeiten mit Fibu Buch.-Blättern](ui-work-general-journals.md)A  
[Journale und Dokumente buchen](ui-post-documents-journals.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
