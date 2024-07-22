---
title: Documentbeveiliging AEM voor Microsoft Office - Opmerkingen bij de release
description: Lees de opmerkingen bij de release voordat u AEM Document Security 6.2 Extension for Microsoft Office installeert.
uuid: f6ab73d4-ac4e-4fff-9bb8-917b75401653
content-type: reference
topic-tags: installing
discoiquuid: c9342c28-8289-4831-a613-4bc03431f557
exl-id: 582f10bb-60d2-46ed-b81d-5818a040edc6
source-git-commit: 3b6a686966fb8d006bed8cc4a4bf5eebe0dfb030
workflow-type: tm+mt
source-wordcount: '1010'
ht-degree: 0%

---

# Documentbeveiliging AEM voor Microsoft Office - Opmerkingen bij de release{#aem-document-security-for-microsoft-office-release-notes}

## Nieuwe functies in AEM documentbeveiliging voor Microsoft Office {#whats-new-in-aem-document-security-for-microsoft-office}

* **Steun voor Bureau 2019**: De Uitbreiding van de Veiligheid van het document voor Microsoft Office heeft steun voor Microsoft Office 2019 toegevoegd. De toepassing werkt ook met Microsoft Office 2019-bureaubladtoepassingen die zijn geïnstalleerd als onderdeel van Office 365.

>[!NOTE]
>
>In het document worden de volgende termen door elkaar gebruikt:
>
>* Adobe Experience Manager Document Security for Microsoft Office
>* Adobe Experience Manager Document Security Extension voor Microsoft Office
>* Documentbeveiligingsextensie voor Microsoft Office

## Documentbeveiligingsextensie voor Microsoft Office installeren en configureren AEM {#installing-and-configuring-aem-document-security-extension-for-microsoft-office}

Deze versie van Document Security Extension voor Microsoft Office is compatibel met Adobe LiveCycle Rights Management ES2 en hoger en de Document Security Add-on voor AEM formulieren.

Controleer de gegevens in dit document voordat u AEM Document Security Extension for Microsoft Office installeert. Voor gedetailleerde installatieinstructies, zie [ het Installeren van en het Vormen de Uitbreiding van de Veiligheid van het AEM van het Document voor Microsoft Office ](installing-configuring-aemdsext.md) artikel.

## Opgeloste problemen {#fixed-issues}

* Tekenreeksen worden verticaal weergegeven en er worden onjuiste regeleinden aan de inhoud toegevoegd. (CQ-4201054)

## Bekende problemen {#known-issues}

### Plug-ins van andere leveranciers worden niet ondersteund {#third-party-plug-ins-not-supported}

AEM Document Security Extension for Microsoft Office werkt niet met plug-ins van derden. Verwijder eventuele plug-ins van derden voor Microsoft Office voordat u de Document Security Extension for Microsoft Office installeert.

### Uitgeschakelde menuopties in Microsoft Word, Excel en PowerPoint {#disabled-menu-options-in-microsoft-word-excel-and-powerpoint}

AEM Document Security Extension for Microsoft Office gebruikt ingebouwde beveiligingsfuncties om documenten, werkbladen en presentaties te beschermen. Hiermee worden enkele opties in het menu Excel, Word en PowerPoint uitgeschakeld.

### Beperkingen voor Microsoft Office 2013, 2016 en 2019 {#restrictions-for-microsoft-office}

In Microsoft Office zijn de volgende opties niet beschikbaar tijdens een beveiligde sessie:

* Microsoft Office 2016 of Microsoft Office 2019

   * Bestand > Opslaan als
   * Bestand > Historie
   * Bestand > Delen
   * Bestand > Exporteren
   * Bestand > Publish
   * Bestand > Account
   * Bestand > Info > Protect-document/werkboek/presentatie > Coderen met wachtwoord
   * Bestand > Info > Protect-document > Een digitale handtekening toevoegen
   * Bestand > Info > Protect-document > Markeren als definitief
   * Optie Delen rechtsboven

* Microsoft Office 2013

   * Bestand > Opslaan als
   * Bestand > Delen
   * Bestand > Exporteren
   * Bestand > Account
   * Bestand > Info > Protect-document/werkboek/presentatie > Coderen met wachtwoord
   * Bestand > Info > Protect-document > Een digitale handtekening toevoegen
   * Bestand > Info > Protect-document > Markeren als definitief

### Een beveiligd document openen vanaf SharePoint Server {#opening-a-protected-document-from-sharepoint-server}

Als u een beveiligd document wilt openen in Documentbeveiligingsextensie voor Microsoft Office vanaf SharePoint Server, opent u eerst het bijbehorende Microsoft Office-programma (Word, Excel of PowerPoint). Als u dit document niet wilt openen, wordt het mogelijk niet geopend. Er wordt een foutbericht weergegeven waarin wordt aangegeven dat u de toepasselijke plug-in installeert. Daarom wordt u aangeraden het bijbehorende Microsoft Office-programma te openen voordat u een beveiligd document opent in Documentbeveiligingsextensie voor Microsoft Office vanaf SharePoint Server.

(Optioneel) U wordt aangeraden de cachemap te wissen voordat u een beveiligd document opent in Document Security Extension for Microsoft Office vanaf SharePoint Server.

Wanneer u een beveiligd document opent vanaf SharePoint Server, worden alle machtigingen voor het document uitgeschakeld, ongeacht het beleid dat is toegepast.

### Een beleid met een dynamisch watermerk toepassen op Microsoft Excel 2013, Microsoft Excel 2016 en Microsoft Excel 2019 zonder dat er een printer is geïnstalleerd {#apply-a-policy-with-a-dynamic-watermark-to-microsoft-excel-microsoft-excel-and-microsoft-excel-file-with-no-printer-installed}

Als u een beleid met een dynamisch watermerk toepast op Excel 2013-, 2016- of 2019-bestanden op een computer waarop geen printer is geïnstalleerd, treedt de fout op: &quot;Interne fout bij het toepassen van een dynamisch watermerk.&quot; Deze fout treedt ook op wanneer u het beveiligde bestand opnieuw opent. Het watermerk wordt niet toegepast en is niet zichtbaar via Weergave > Pagina-indeling.

### De Preventie van de Uitvoering van Gegevens van Vensters voor gesteunde toepassingen van het Bureau onbruikbaar {#disable-windows-data-execution-prevention-for-supported-office-applications}

U wordt aangeraden de instelling DEP (Windows Data Execution Prevention) uit te schakelen wanneer u de documentbeveiligingsextensie voor Microsoft Office-toepassingen gebruikt.

### Gedeelde Microsoft Office-bestanden kunnen niet worden beveiligd met Documentbeveiliging {#shared-microsoft-office-files-cannot-be-protected-using-document-security-extension}

Wanneer u een gedeeld Microsoft Office-bestand beveiligt met Documentbeveiligingsextensie, treedt een fout op en wordt het gedeelde bestand niet beveiligd.

### Office-toepassingen starten op een computer met Document Security Extension for Microsoft Office en McAfee VirusScan {#starting-office-applications-on-a-machine-containing-document-security-extension-for-microsoft-office-and-mcafee-virusscan}

Schakel de optie Buffer Overflow Protection uit in de McAfee VirusScan-console om ervoor te zorgen dat Office-toepassingen probleemloos worden gestart op een computer met Documentbeveiliging en McAfee VirusScan (On-Access Scan ingeschakeld).

### Documentbeveiligingsextensie voor Microsoft Office installeren op een computer met een niet-ondersteunde Microsoft Office-taal {#installing-document-security-extension-for-microsoft-office-on-a-machine-with-an-unsupported-microsoft-office-language}

Voordat u de extensie Documentbeveiliging voor Microsoft Office installeert op een computer met een Microsoft Office-toepassing met een niet-ondersteunde taal, moet u de Office-toepassing minstens één keer openen.

### De knop Offline synchroniseren is ingeschakeld, zelfs als een gebruiker geen offlinerechten heeft {#synchronize-offline-button-is-enabled-even-when-a-user-does-not-have-offline-permissions}

De knop Offline synchroniseren is beschikbaar, ook al heeft de gebruiker geen offline machtigingen voor het document. Het selecteren van de knop heeft echter geen effect.

### Geen ondersteuning voor proefversies van Microsoft Office {#no-support-for-trial-versions-of-microsoft-office}

Documentbeveiligingsextensie voor Microsoft Office ondersteunt geen trailversies van Microsoft Office. Voordat u de extensie installeert, moet u controleren of u een exemplaar met licentie van Microsoft Office hebt geïnstalleerd en of deze geactiveerd is.

### Kan geen beveiligde Microsoft Office-bestanden openen {#unable-to-open-a-protected-microsoft-office-files}

Als de beveiligde weergave van het Microsoft Office is ingeschakeld, kunnen met de Right Management Extension geen beveiligde Microsoft Excel-bestanden (XLS, XLSX) en beveiligde Microsoft PowerPoint-bestanden (PPT) vanaf een externe locatie worden geopend.

### Cellen van Microsoft Excel-document met een afbeeldings- of achtergrondkleur worden boven op een watermerk weergegeven {#cells-of-microsoft-excel-document-containing-an-image-or-background-color-appear-on-top-of-watermark}

Als een cel in een Excel-document een afbeeldings- of achtergrondkleur heeft en er een dynamisch watermerk wordt toegepast, bedekt de afbeelding of kleur het watermerk. Dit betekent dat het watermerk wordt bedekt door de afbeeldings- of achtergrondkleur in de cel.

### Probleem met bruikbaarheid van meerdere certificaten {#usability-issue-with-multiple-certificates}

Als er meerdere certificaten aanwezig zijn op de clientcomputer en de gebruiker het dialoogvenster voor certificaatselectie annuleert, wordt het dialoogvenster opnieuw weergegeven. De gebruiker moet het dialoogvenster tweemaal annuleren.

### Met Microsoft PowerPoint kunt u beveiligde documenten bewerken {#microsoft-powerpoint-allows-editing-protected-documents}

Als Microsoft PowerPoint probeert een beveiligd document te bewerken, wordt het bericht &quot;U bent niet gemachtigd om dit document te wijzigen. U kunt uw wijzigingen niet opslaan.&quot; Na het sluiten van het bericht kunnen gebruikers doorgaan met het toevoegen van tekst of het bewerken van het document. De wijzigingen die in de beveiligde documenten zijn aangebracht, worden echter niet opgeslagen.

Bovengenoemd gedrag is zoals verwacht in PowerPoint 2013, PowerPoint 2016 en PowerPoint 2019.
