---
title: 'Elektronischer Zahlungsverkehr mit LSV+ [CH]'
description: Die elektronische Zahlungsform Lastschrift Verfahren (LSV+) oder Einzug ermöglicht Firmen das direkte Abrufen von Zahlungen von Debitorenbankkonten.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.form: '3010830, 3010831, 3010832,3010834, 3010835'
ms.date: 06/21/2021
ms.author: edupont
---
# <a name="swiss-electronic-payments-using-lsv-in-the-swiss-version" />Elektronische Zahlungen mit LSV+ in der Schweizer Version
Die elektronische Zahlungsform Lastschrift Verfahren (LSV+) oder Einzug, eine optimierte Version von LSV, ermöglicht Firmen das direkte Abrufen von Zahlungen von Debitorenbankkonten. Zum Abrufen von Debitorenzahlungen muss eine LSV-Datei an die Bank gesendet werden, die dann die Abbuchung der in der Datei angeforderten Zahlungen abwickelt.  

Die LSV+-Methode ist ein Einzugsverfahren mit Recht auf Widerspruch. BDD (Business Direct Debit) ist ein Einzugsverfahren ohne Recht auf Widerspruch. Die Formate der an die Bank gesendeten Dateien sind für LSV+ und BDD identisch.  

Bevor Sie das LSV-Modul verwenden, müssen die Einstellungen auf der Seite **LSV Einrichtung** festgelegt werden.

## <a name="automatic-esr-processing" />Automatische ESR-Verarbeitung
Sie können Zahlungsgutschrifttransaktionen im Einzahlungsschein mit Referenznummer (ESR)-Dateiformat von der Bank herunterladen. Wenn die ESR-Referenznummer in das LSV+-System integriert ist, können Sie verarbeitete LSV-Zahlungen in der ESR-Datei erhalten. Wenn LSV+-Zahlungen in Ihren importierten LSV-Dateien enthalten sind, werden die entsprechenden LSV-Journalzeilen automatisch geschlossen. Die automatische ESR-Verarbeitung wird nur bei Zahlungen in Schweizer Franken (CHF) durchgeführt. Hierzu müssen Sie folgende Schritte durchführen:  

- Nachdem Sie die LSV+-Datei an die Bank gesendet haben, übermitteln Sie innerhalb von drei Tagen nach dem angeforderten LSV-Verarbeitungsdatum einen Zahlungsbericht.  

- Importieren Sie die ESR-Dateien, und buchen Sie die ESR-Journale. Falls eine importierte ESR-Transaktion mit einer offenen LSV+-Zahlungszeile verknüpft ist, wird die entsprechende LSV-Journalzeile automatisch von ESR geschlossen.  

    > [!NOTE]  
    >  Beim Importieren einer ESR-Datei wird die LSV-Journalzeile unabhängig vom ESR-Transaktionstyp von ESR geschlossen, falls das entsprechende LSV-Journal gefunden wird.  

- Nach dem LSV-Verarbeitungsdatum können Sie die LSV-Journalzeilen überprüfen. Wenn alle LSV-Journalzeilen geschlossen sind, wird der **LSV-Status** zu **Beendet** aktualisiert.  

## <a name="see-also" />Siehe auch
 [Verarbeiten eines LSV-Einzugs](how-to-process-an-lsv-collection.md)   
 [Schliessen eines LSV-Einzugs](how-to-close-an-lsv-collection.md)   
 [Buchen von LSV+ Zahlungen](how-to-post-lsv-payments.md)   
 [Exportieren von Zahlungen mit LSV](how-to-export-payments-using-lsv.md)   
 [Elektronische Zahlungen (Schweiz)](swiss-electronic-payments.md)   
 [Elektronische Zahlungen mit ESR (Schweiz)](swiss-electronic-payments-using-esr.md)   
 [Zahlungen vornehmen](../../payables-make-payments.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
