---
title: 'Designdetails: Konten in der Fibu | Microsoft Docs'
description: 'Um Lagerbestände und Kapazitätsposten mit der Finanzbuchhaltung abzustimmen, werden die zugehörigen Wertposten auf verschiedene Konten in der Finanzbuchhaltung gebucht.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/08/2021
ms.author: edupont
---
# <a name="design-details-accounts-in-the-general-ledger" />Designdetails: Konten in der Finanzbuchhaltung
Um Lagerbestände und Kapazitätsposten mit der Finanzbuchhaltung abzustimmen, werden die zugehörigen Wertposten auf verschiedene Konten in der Finanzbuchhaltung gebucht. Weitere Informationen finden Sie unter [Designdetails: Abstimmung mit der Fibu](design-details-reconciliation-with-the-general-ledger.md).  

## <a name="from-the-inventory-ledger" />Vom Bestandsposten
Die folgende Tabelle zeigt die Beziehung zwischen den verschiedenen Arten von Bestandswertposten und die Konten und Gegenkonten im Fibukonto an.  

|**Lagerpostenart**|**Wertpostenart**|**Abweichungsart**|**Soll-Kosten**|**Konto**|**Gegenkonto**|  
|--------------------------------|--------------------------|-----------------------|-----------------------|-----------------|---------------------------|  
|Einkauf|Direkte Kosten||Ja|Lager (Interim)|Lagerzugangskonto (Interim)|  
|Einkauf|Direkte Kosten||Nr.|Lagerbest.|Direkte Kosten verrechnet|  
|Einkauf|Indirekte Kosten||Nr.|Lagerbest.|Gemeinkosten verrechnet|  
|Einkauf|Abweichung|Einkauf|Nr.|Lagerbest.|Einkaufsabweichung|  
|Einkauf|Neubewertung||Nr.|Lagerbest.|Lagerkorrektur|  
|Einkauf|Rundung||Nr.|Lagerbest.|Lagerkorrektur|  
|Verkauf|Direkte Kosten||Ja|Lager (Interim)|LAGERVERBR (Interim)|  
|Verkauf|Direkte Kosten||Nr.|Lagerbest.|LAGERVERBR|  
|Verkauf|Neubewertung||Nr.|Lagerbest.|Lagerkorrektur|  
|Verkauf|Rundung||Nr.|Lagerbest.|Lagerkorrektur|  
|Zugang,Abgang,Lagerplatzumlagerung|Direkte Kosten||Nr.|Lagerbest.|Lagerkorrektur|  
|Zugang,Abgang,Lagerplatzumlagerung|Neubewertung||Nr.|Lagerbest.|Lagerkorrektur|  
|Zugang,Abgang,Lagerplatzumlagerung|Rundung||Nr.|Lagerbest.|Lagerkorrektur|  
|(Produktions-) Verbrauch|Direkte Kosten||Nr.|Lagerbest.|WIP|  
|(Produktions-) Verbrauch|Neubewertung||Nr.|Lagerbest.|Lagerkorrektur|  
|(Produktions-) Verbrauch|Rundung||Nr.|Lagerbest.|Lagerkorrektur|  
|Verbrauch für Montage|Direkte Kosten||Nr.|Lagerbest.|Lagerkorrektur|  
|Verbrauch für Montage|Direkte Kosten||Nr.|Direkte Kosten verrechnet|Lagerkorrektur|  
|Verbrauch für Montage|Indirekte Kosten||Nr.|Gemeinkosten verrechnet|Lagerkorrektur|  
|(Fertig produzierte Artikel; Istmeldungen)|Direkte Kosten||Ja|Lager (Interim)|WIP|  
|(Fertig produzierte Artikel; Istmeldungen)|Direkte Kosten||Nr.|Lagerbest.|WIP|  
|(Fertig produzierte Artikel; Istmeldungen)|Indirekte Kosten||Nr.|Lagerbest.|Gemeinkosten verrechnet|  
|(Fertig produzierte Artikel; Istmeldungen)|Abweichung|Material|Nr.|Lagerbest.|Materialabweichung|  
|(Fertig produzierte Artikel; Istmeldungen)|Abweichung|Kapazität|Nr.|Lagerbest.|Kapazitätsabweichung|  
|(Fertig produzierte Artikel; Istmeldungen)|Abweichung|Fremdarbeit|Nr.|Lagerbest.|Fremdarbeitskostenabweichung|  
|(Fertig produzierte Artikel; Istmeldungen)|Abweichung|Kapazitätsgemeinkosten|Nr.|Lagerbest.|Kap.-Gemeinkostenabweichung|  
|(Fertig produzierte Artikel; Istmeldungen)|Abweichung|Produktionsgemeinkosten|Nr.|Lagerbest.|Prod.-Gemeinkostenabweichung|  
|(Fertig produzierte Artikel; Istmeldungen)|Neubewertung||Nr.|Lagerbest.|Lagerkorrektur|  
|(Fertig produzierte Artikel; Istmeldungen)|Rundung||Nr.|Lagerbest.|Lagerkorrektur|  
|Montageausstoss|Direkte Kosten||Nr.|Lagerbest.|Lagerkorrektur|  
|Montageausstoss|Neubewertung||Nr.|Lagerbest.|Lagerkorrektur|  
|Montageausstoss|Indirekte Kosten||Nr.|Lagerbest.|Gemeinkosten verrechnet|  
|Montageausstoss|Abweichung|Material|Nr.|Lagerbest.|Materialabweichung|  
|Montageausstoss|Abweichung|Kapazität|Nr.|Lagerbest.|Kapazitätsabweichung|  
|Montageausstoss|Abweichung|Kapazitätsgemeinkosten|Nr.|Lagerbest.|Kap.-Gemeinkostenabweichung|  
|Montageausstoss|Abweichung|Produktionsgemeinkosten|Nr.|Lagerbest.|Prod.-Gemeinkostenabweichung|  
|Montageausstoss|Rundung||Nr.|Lagerbest.|Lagerkorrektur|  

## <a name="from-the-capacity-ledger" />Vom Kapazitätsposten
 Die folgende Tabelle zeigt die Beziehung zwischen den verschiedenen Arten von Kapazitätswertposten und die Konten und Gegenkonten im Fibukonto an. Kapazitätsposten stellen die Arbeitszeit dar, die bei Montage- oder Produktionsarbeiten verbraucht wird.  

|**Arbeitstyp**|**Kapazitätsposten Lfd. Nr.**|**Wertpostenart**|**Konto**|**Gegenkonto**|  
|-------------------|------------------------------------|--------------------------|-----------------|---------------------------|  
|Montage|Ressource|Direkte Kosten|Direkte Kosten verrechnet|Lagerkorrektur|  
|Montage|Ressource|Kosten|Gemeinkosten verrechnet|Lagerkorrektur|  
|Produktion|Arbeitsplatz/Arbeitsplatzgrupe|EK-Preis|Unf.-Arbeit-Konto|Direkte Kosten verrechnet|  
|Produktion|Arbeitsplatz/Arbeitsplatzgrupe|Kosten|Unf.-Arbeit-Konto|Gemeinkosten verrechnet|  

## <a name="assembly-costs-are-always-actual" />Montagekosten sind immer Ist-Kosten
 Wie in der obigen Tabelle gezeigt, werden Montagebuchungen in Interimskonten nicht repräsentiert. Dies liegt daran, dass der Begriff Umlaufbestand (WIP) in der Montageausstossbuchung nicht gilt, anders als in der Istmeldungsbuchung. Montagekosten werden nur als Ist-Kosten gebucht, nie als erwartete Kosten.  

 Weitere Informationen finden Sie unter [Designdetails: Montageauftragsbuchung](design-details-assembly-order-posting.md).  

## <a name="calculating-the-amount-to-post-to-the-general-ledger" />Berechnung des in die Finanzbuchhaltung zu buchenden Betrags
 Die folgenden Felder in der Tabelle **Werteintrag** werden verwendet, um den erwarteten Kostenbetrag zu berechnen, der in die Fibu gebucht wird:  

-   Einstandsbetrag (tatsächl.)  
-   Gebuchte Lagerregulierung  
-   Einstandsbetrag (erwartet)  
-   Auf Fibukonto geb. Soll-Kosten  

Die nachstehende Tabelle zeigt, wie die in die Finanzbuchhaltung zu buchenden Beträge für die beiden verschiedenen Kostenarten berechnet werden.  

|Kostenart|Berechnung|  
|---------------|-----------------|  
|Ist-Kosten|Einstandsbetrag (tatsächl.) – Gebuchte Lagerregulierung|  
|Soll-Kosten|Kostenbetrag (erwartet) – Auf Sachkonto geb. Soll-Kosten|  

## <a name="see-also" />Siehe auch
 [Designdetails: Lagerkostenberechnung](design-details-inventory-costing.md)   
 [Designdetails: Bestandsbuchung](design-details-inventory-posting.md)   
 [Designdetails: Soll-Kosten-Buchen](design-details-expected-cost-posting.md)  
 [Verwalten der Bestandsregulierung](finance-manage-inventory-costs.md)  
 [Finanzen](finance.md)  
 [Arbeiten mit [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
