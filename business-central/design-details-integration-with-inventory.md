---
title: Design-Details – Integration mit dem Bestand
description: Der Anwendungsbereich Warehouse Management und der Anwendungsbereich Inventur interagieren bei der physischen Inventur und beim Inventur- oder Lagerabgleich miteinander.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/15/2021
ms.author: edupont
---
# <a name="design-details-integration-with-inventory" />Designdetails: Integration mit dem Lagerbestand

Die Funktionen Warehouse Management und Lager interagieren bei der physischen Inventur und beim Inventur- oder Lagerabgleich miteinander.  

## <a name="physical-inventory" />Physisches Lager

Die **Logistik-Inventur-Erf.-Journal**-Seite wird mit der **Inventur Erf.-Journal**-Seite für alle erweiterten Lagerorte verwendet. Der Bestand auf Lagerplatzebene wird berechnet, und eine gedruckte Liste wird für den Lagermitarbeiter bereitgestellt. Die Liste zeigt, welche Artikel an welchen Lagerplätzen gezählt werden müssen.  
  
Der Lagermitarbeiter gibt die gezählte Menge auf der**Logistik-Inventur-Erf.-Journal** Seite ein und bucht das Erf.-Journal.  
  
Wenn die gezählte Menge grösser als die Menge auf der Erf.-Journalzeile ist, wird eine Umlagerung für diese Differenz aus dem Standard-Ausgleichslagerplatz zum gezählten Lagerplatz gebucht. Dieses erhöht die Menge im gezählten Lagerplatz und vermindert die Menge im Standard-Ausgleichslagerplatz.  
  
Wenn die gezählte Menge geringer als die Menge auf der Erf.-Journalzeile ist, wird eine Umlagerung für diese Differenz aus dem gezählten Lagerplatz zum Standard-Ausgleichslagerplatz gebucht. Dieses reduziert die Menge im gezählten Lagerplatz und erhöht die Menge im Standard-Ausgleichslagerplatz.  
  
In erweiterten Lagerfunktionskonfigurationen wird der Wert im Feld **Menge (berechnet)** aus den Lagerposten einbezogen und der Wert im Feld **Menge (Phys. Lagerbestand)** aus den Lagerplatzposten ohne Ausgleichslagerplatzinhalt abgerufen. Das Feld **Menge** gibt die Differenz zwischen den ersten beiden Feldern an, die dem Inhalt des Regulierungslagerplatzes entsprechen sollte.  
  
Wenn Sie das Inventur Erf.-Journal buchen, werden der Lagerbestand und der Ausgleichslagerplatz aktualisiert.  

[!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]
  
## <a name="warehouse-adjustments-to-the-item-ledger" />Lagerplatz-Anpassungen mit dem Artikelposten

Sie verwenden die Seite **Artikel Erf.-Journal** und die Funktion **Ausgleich berechnen**, um den Lagerbestand im Artikelposten in Übereinstimmung mit einem Ausgleich anzupassen, der für die Artikelmenge in einem Lagerplatz vorgenommen wurde. Um eine Verbindung zwischen den Lagerbestand und der Logistik zu erstellen, müssen Sie einen Vorgabe-Ausgleichslagerplatz pro Lagerort festlegen.  
  
Der Standard-Regulierungslagerplatz registriert Artikel im Lager, wenn Sie einen Zugang für den Bestand buchen. Wenn Sie jedoch einen Lagerabgang buchen, wird die Menge am Lagerplatz ebenfalls verringert. In beiden Fällen werden Lagerposten und Lagerposten erstellt.  
  
> [!NOTE]  
> Bestandsberechnungen beinhalten nicht den Ausgleichsbehälter.  
  
Wenn Sie den Lagerplatzinhalt anpassen wollen, können Sie ein Logistik Artikel-Erf.-Journal verwenden, von dem Sie die Artikelnummer, den Zonencode, den Lagerplatzcode und die Menge angeben können, die Sie anpassen möchten.  
  
Wenn Sie eine positive Menge eingeben und die Zeile buchen, wird der Bestand an dem Lagerplatz erhöht, und die Menge des Standard-Ausgleichslagerplatzes wird entsprechend vermindert.  
  
## <a name="see-also" />Weitere Informationen

[Lagerverwaltung – Übersicht ](design-details-warehouse-management.md)  
[Designdetails: Verfügbarkeit im Lager](design-details-availability-in-the-warehouse.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
