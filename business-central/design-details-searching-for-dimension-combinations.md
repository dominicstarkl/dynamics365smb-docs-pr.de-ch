---
title: 'Designdetails: Suche nach Dimensionskombinationen | Microsoft Docs'
description: Wenn Sie eine Seite schliessen, nachdem Sie einen Satz von Dimensionen bearbeitet haben, prüft Business Central, ob die bearbeitete Zusammenstellung von Dimensionen vorhanden ist. Wenn der Satz nicht vorhanden, wird ein neuer Satz erstellt und die Dimensionskombination-ID wird zurückgegeben.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: cde720526fdad4c9e4352f08f649d6bd3fc51540
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 03/31/2019
ms.locfileid: "912377"
---
# <a name="design-details-searching-for-dimension-combinations"></a>Designdetails: Suche nach Dimensionskombinationen
Wenn Sie eine Seite schliessen, nachdem Sie einen Satz von Dimensionen bearbeitet haben, prüft [!INCLUDE[d365fin](includes/d365fin_md.md)], ob die bearbeitete Zusammenstellung von Dimensionen vorhanden ist. Wenn der Satz nicht vorhanden, wird ein neuer Satz erstellt und die Dimensionskombination-ID wird zurückgegeben.  

## <a name="building-search-tree"></a>Erstellungs-Suchstruktur  
 Tabelle 481 D**imensionssatz-Strukturknoten** wird verwendet, wenn [!INCLUDE[d365fin](includes/d365fin_md.md)] prüft, ob ein Satz von Dimensionen bereits in Tabelle 480 **Dimensionssatzposten** existiert. Die Auswertung wird ausgeführt, indem die Suchstruktur rekursiv verläuft, beginnend bei der oben ausgerichteten numerierte 0. Die oberste Ebene 0 stellt einen Dimensionssatz ohne Dimensionssatzposten dar. Die untergeordneten Elemente dieses Dimensionssatzes stellen Dimensionssätze mit nur einem Dimensionssatzposten dar. Die untergeordneten Elemente dieser Dimensionssätze stellen Dimensionssätze mit zwei untergeordneten Elementen dar usw.  

### <a name="example-1"></a>Beispiel 1  
 Das folgende Diagramm stellt eine Suchstruktur mit sechs Dimensionssätzen dar. Nur der unterscheidene Dimensionssatzposten wird im Diagramm angezeigt.  

 ![Beispiel der Dimensionsstruktur](media/nav2013_dimension_tree.png "Beispiel der Dimensionsstruktur")  

 Die folgende Tabelle enthält eine vollständige Liste der Dimensionssatzposten, die jeden Dimensionssatz ergeben.  

|Dimensionssätze|Dimensionssatzposten|  
|--------------------|---------------------------|  
|0 Ausgewählt|keine|  
|1 Ausgewählt|AREA 30|  
|2 Ausgewählt|AREA 30, DEPT ADM|  
|3 Ausgewählt|AREA 30, DEPT PROD|  
|4 Ausgewählt|AREA 30, DEPT ADM, PROJ VW|  
|5 Ausgewählt|AREA 40|  
|6 Ausgewählt|AREA 40, PROJ VW|  

### <a name="example-2"></a>Beispiel 2  
 In diesem Beispiel wird gezeigt, wie [!INCLUDE[d365fin](includes/d365fin_md.md)] bestimmt, ob ein Dimensionssatz, der aus den Dimensionssatzposten AREA 40, DEPT PROD besteht, vorhanden ist.  

 Ausserdem aktualisiert[!INCLUDE[d365fin](includes/d365fin_md.md)] die Tabelle **Dimensionssatz-Strukturknoten**, um sicherzustellen, dass die Suchstruktur wie das folgende Diagramm aussieht. Daher wird Dimensionssatz 7 zu einem untergeordneten Element des Dimensionssatzes 5.  

 ![Beispiel der Dimensionsstruktur in NAV 2013](media/nav2013_dimension_tree_example2.png "Beispiel der Dimensionsstruktur in NAV 2013")  

### <a name="finding-dimension-set-id"></a>Suchen der Dimensionssatz-ID  
 Auf konzeptioneller Ebene werden **Übergeordnete Kennung**, **Dimension** und **Dimensionswert**, in der Suchstruktur, als Primärschlüssel kombiniert und verwendet, da [!INCLUDE[d365fin](includes/d365fin_md.md)] die Struktur in derselben Reihenfolge wie die Dimensionsposten durchläuft. Die GET-Funktion (Datensatz) wird verwendet, um nach der Dimensionssatz-ID zu suchen Das folgende Codebeispiel zeigt, wie Sie die Dimensionssatz-ID finden, wenn es drei Dimensionswerte gibt.  

```  
DimSet."Parent ID" := 0;  // 'root'  
IF UserDim.FINDSET THEN  
  REPEAT  
      DimSet.GET(DimSet."Parent ID",UserDim.DimCode,UserDim.DimValueCode);  
  UNTIL UserDim.NEXT = 0;  
EXIT(DimSet.ID);  

```  

Um jedoch die Möglichkeit von [!INCLUDE[d365fin](includes/d365fin_md.md)] zu gewährleisten, um eine Dimension und einen Dimensionswert umzubenennen, wird die Tabelle 349 **Dimensionswert** mit einem Intergerfeld **Dimensionswert-ID** erweitert. Diese Tabelle wandelt die Feldpaare **Dimension** und **Dimensionswert** zu einem Integerwert um. Wenn Sie die Dimension sowie den Dimensionswert umbenennen, wird der Integerwert nicht geändert.  

```  
DimSet."Parent ID" := 0;  // 'root'  
IF UserDim.FINDSET THEN  
  REPEAT  
      DimSet.GET(DimSet.ParentID,UserDim."Dimension Value ID");  
  UNTIL UserDim.NEXT = 0;  
EXIT(DimSet.ID);  

```  

## <a name="see-also"></a>Siehe auch  
 [Funktion ABRUFEN (Datensatz)](/dynamics-nav/GET-Function--Record-)    
 [Designdetails: Dimensionssatzposten](design-details-dimension-set-entries.md)   
 [Dimensionssatz-Eintrags-Übersicht](design-details-dimension-set-entries-overview.md)   
 [Designdetails: Tabellenstruktur](design-details-table-structure.md)   
 [Designdetails: Codeunit 408 Dimension Management](design-details-codeunit-408-dimension-management.md)   
 [Designdetails: Codebeispiele von geänderten Mustern in Änderungen](design-details-code-examples-of-changed-patterns-in-modifications.md)
