---
title: Gebuchte fertig gestellte Menge stornieren
description: 'Es kann vorkommen, dass die Buchung einer fertig gestellten Menge storniert werden muss. In diesem Thema wird die Vorgehensweise zum Stornieren von Ausgangsbuchungen beschrieben.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 5510
ms.date: 06/22/2021
ms.author: edupont
---
# <a name="reverse-output-posting" />Gebuchte fertig gestellte Menge stornieren

Es kann vorkommen, dass die Buchung einer fertig gestellten Menge storniert werden muss. Dies ist z. B. der Fall, wenn eine fehlerhafte Dateneingabe passiert ist und eine falsche fertiggestellte Menge in einem Fertigungsauftrag gebucht wurde.  

## <a name="to-reverse-an-output-posting" />Eine Ausgangsbuchung stornieren

1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](media/ui-search/search_small.png "Tell me-Funktion") Symbol. Geben Sie **Erfassung Erf.-Journal** ein und wählen Sie dann den zugehörigen Link. Wählen Sie Ihren Stapel aus.  
2. Füllen Sie die Felder je nach Bedarf aus. Weitere Informationen finden Sie unter [Produktionsausgabe und Laufzeiten über Stapelverarbeitung buchen](production-how-to-post-output-quantity.md)
3. Wählen Sie im Feld **Ausgleich mit Lfd. Nr.** den zugeordneten Lagerposten aus. Dadurch werden der Kapazitäts- und der Lagerposten storniert.  
4. Erfen Sie die Stornierung, indem Sie das Erf.-Journal buchen.  

Die Posten im FA-Istmeldungsprotokoll werden im HauptLagerposten als positiver Ausgleich gebucht.  

## <a name="see-also" />Siehe auch

 [Produktion](production-manage-manufacturing.md) [Produktion einrichten](production-configure-production-processes.md)  
 [Planung](production-planning.md)  
 [Bestand](inventory-manage-inventory.md)  
 [Einkauf](purchasing-manage-purchasing.md)  
 [Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
