---
title: 'Gewusst wie: Drucken einer Lager-Kommissionierliste aus Verkaufsaufträgen'
description: Sie können eine Lager-Kommissionierliste direkt aus einem Verkaufsauftrag, Verkaufsbeleg, Rechnungsbeleg und anderen ausgehenden Verkaufsauftragsbelegen drucken.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/27/2020
ms.author: edupont
ms.openlocfilehash: fadf974c41b34a5beb7b3b313847cc6a5bfcec78
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 09/09/2020
ms.locfileid: "3781649"
---
# <a name="print-the-picking-list"></a>Kommissionierliste drucken
Sie können eine Lager-Kommissionierliste direkt aus einem Verkaufsauftragsbeleg, Verkaufsbeleg, Rechnungsbeleg und anderen ausgehenden Verkaufsauftragsbelegen drucken.

Dieser Bericht wird normalerweise in Unternehmen ohne dedizierte Funktionen für die Lagerverwaltung verwendet, sodass ein Lagerarbeiter die Kommissionierliste einfach über den zugehörigen Verkaufsbeleg aufrufen oder drucken kann. In Unternehmen mit höherem Volumen oder komplexeren Prozessen wird die Kommissionierung in dedizierten Lagerbelegen geplant und durchgeführt. Weitere Informationen finden Sie unter [Artikel kommissionieren](warehouse-pick-items.md).

## <a name="to-print-a-picking-list-from-a-sales-order"></a>So drucken Sie eine Kommissionierliste aus einem Verkaufsauftrag  
Das folgende Verfahren basiert auf einer Auftragsabwicklung. Die Schritte sind für alle Verkaufsbelege ähnlich, mit denen der Versand von Artikeln eingeleitet werden kann.

1. Wählen Sie das Symbol ![Suche nach Seite oder Bericht](media/ui-search/search_small.png "Symbol 'Nach Seite oder Bericht suchen'"), geben Sie **Verkaufsaufträge** ein und wählen Sie dann den entsprechenden Link.  
2. Öffnen Sie den Verkaufsauftrag, für den Sie Artikel auswählen möchten.  
3. Wählen Sie die Aktion **Bericht** und dann die Aktion **Kommissionierliste nach Bestellung** aus.  
4. Wählen Sie die Schaltfläche **Drucken** aus, um die Auswahlliste zu drucken oder wählen Sie die Schaltfläche **Vorschau**, um den Bericht auf dem Bildschirm anzuzeigen.

Sie können die Kommissionierliste auch als Dokument speichern, um sie beispielsweise an jemanden zu senden oder dem Verkaufsauftrag als Anhang hinzuzufügen. Weitere Informationen finden Sie unter [Verwalten von Anhängen, Links und Notizen zu Karten und Belegen](ui-how-add-link-to-record.md).

> [!NOTE]
> Wenn Sie die Funktion **Stückliste explodieren** auf dem Verkaufsauftrag verwendet haben, werden im Bericht nur die Komponenten des zugehörigen Montageartikels angezeigt. Weitere Informationen finden Sie unter [Mit Stücklisten arbeiten](inventory-how-work-BOMs.md).

## <a name="see-also"></a>Siehe auch  
[Lagerbestand](inventory-manage-inventory.md)  
[Entnahme von Artikeln](warehouse-pick-items.md)  
[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)   