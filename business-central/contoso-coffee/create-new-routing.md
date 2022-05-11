---
title: Neuen Arbeitsplan erstellen
description: Exemplarische Vorgehensweise, um zu erfahren, wie Sie alle Informationen für einen neuen Arbeitsplan manuell in Business Central eingeben.
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics365-business-central
author: edupont04
ms.author: andreipa
ms.openlocfilehash: deb1ef6ab18cbd6562ae18cc17495fe3e5021db1
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: de-CH
ms.lasthandoff: 03/31/2022
ms.locfileid: "8525425"
---
# <a name="walkthrough-create-a-new-routing"></a>Exemplarische Vorgehensweise: Erstellen Sie einen neuen Arbeitsplan

In diesem Artikel führen wir Sie durch die Schritte zur Verwendung der Contoso Coffee-Demodaten zum manuellen Einrichten eines neuen Produktionsarbeitsplans in [!INCLUDE [prod_short](../includes/prod_short.md)].  

## <a name="scenario"></a>Szenario

Oscar, der Verfahrenstechniker bei Contoso Coffee, beschliesst, einen neuen Arbeitsplan mit dem Namen *Neuer Pfad* zu erstellen. Da sich dieser Arbeitsplan von allen anderen Arbeitsplänen bei Contoso Coffee unterscheidet, muss er alle Informationen für den Arbeitsplan manuell eingeben.  

## <a name="steps"></a>Schritte

1. Erstellen Sie die Arbeitsplan-Kopfzeile.  

    1. Wählen Sie die ![Glühbirne, die die „Wie möchten Sie weiter verfahren“-Funktion öffnet.](../media/ui-search/search_small.png "Tell me-Funktion") Symbol. Geben Sie **Arbeitspläne** ein und wählen Sie dann den zugehörigen Link.  

    2. Wählen Sie die Aktion **Neu** und füllen Sie dann die Felder wie in der folgenden Tabelle beschrieben aus.  

        |Feld  |Wert  |
        |---------|---------|
        |**Nr.** |1099|
        |**Description** |Neuer Pfad|
2. Erstellen Sie die Arbeitsplanpositionen.

    1. Fügen Sie auf dem Inforegister **Positionen** eine neue Position hinzu und füllen Sie die Felder gemäss der Beschreibung in der folgenden Tabelle aus.  

        |Feld  |Wert  |
        |---------|---------|
        |**Arbeitsgangnr.** |10|
        |**Typ** |Arbeitsplatzgruppe|
        |**Nr.** |100|
        |**Einrichtungszeit** |20|
        |**Bearbeitungszeit** |15|

    2. Fügen Sie eine neue Position hinzu und füllen Sie die Felder gemäss der Beschreibung in der folgenden Tabelle aus.  

        |Feld  |Wert  |
        |---------|---------|
        |**Arbeitsgangnr.** |20|
        |**Typ** |Arbeitsplatzgruppe|
        |**Nr.** |200|
        |**Einrichtungszeit** |30|
        |**Bearbeitungszeit** |5|
3. Zertifizieren Sie den Arbeitsplan.

    1. Wählen Sie im Feld **Status** *Zertifiziert* aus.  

Der neue Arbeitsplan ist nun eingerichtet.  

## <a name="see-also"></a>Siehe auch

[Einführung in Contoso Coffee Demo Data](contoso-coffee-intro.md)  