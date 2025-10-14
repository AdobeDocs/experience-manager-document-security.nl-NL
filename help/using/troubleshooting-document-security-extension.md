---
title: Problemen oplossen AEM Documentbeveiligingsextensie voor Microsoft Office
description: Als u problemen ondervindt bij het installeren, configureren of gebruiken van de AEM Document Security Extension for Microsoft Office, volgt u de instructies in dit document.
uuid: 61001ca8-a25a-4879-98ac-563a6eb126e7
contentOwner: khsingh
content-type: reference
topic-tags: using
discoiquuid: bdc3f174-e417-4d3e-b3af-972cdcc10133
exl-id: 98f24032-0774-47f8-bcc5-1ee37b417833
source-git-commit: 3b6a686966fb8d006bed8cc4a4bf5eebe0dfb030
workflow-type: tm+mt
source-wordcount: '284'
ht-degree: 0%

---

# Problemen oplossen AEM Documentbeveiligingsextensie voor Microsoft Office{#troubleshooting-aem-document-security-extension-for-microsoft-office}

## Problemen met installatie en configuratie oplossen {#troubleshootinginstallationandconfiguration}

Als u problemen hebt die en de Uitbreiding van de Veiligheid van het AEMDocument voor Microsoft Office installeren, zorg ervoor dat u zorgvuldig de instructies volgde die in worden vermeld - alvorens u installeert - sectie van het [&#x200B; installatie &#x200B;](installing-configuring-aemdsext.md) artikel.

Als u alles volgens de documentatie hebt geïnstalleerd en geconfigureerd, controleert u de volgende secties op problemen die lijken op wat u ervaart.

### Documentbeveiligingsextensie kan niet worden geladen voor Microsoft Office-toepassingen {#document-security-extension-fails-to-load-for-microsoft-office-applications}

Met de eigenschap LoadBehavior in Windows-register wordt het runtimegedrag van de insteekmodule voor documentbeveiliging aangegeven. Als de eigenschap LoadBehavior is ingesteld op 3, worden alle plug-ins automatisch geladen. Voordat u de extensie Documentbeveiliging voor Microsoft Office installeert, moet u controleren of de eigenschap value LoadBehavior is ingesteld op 3.

1. Maak een back-up van het Windows-register voordat u er wijzigingen in aanbrengt. Voor gedetailleerde instructies, zie [&#x200B; hoe te de Registratie van Vensters wijzigen &#x200B;](https://learn.microsoft.com/en-us/troubleshoot/windows-server/performance/windows-registry-advanced-users).
1. Navigeer in de Register-editor naar toHKEY_CURRENT_USER\Software\Microsoft\Office\Word\Addins\Adobe.DRMIntegration.WordAddin of HKEY_LOCAL_MACHINE\Software\Microsoft\Office\Word\Addins\Adobe.DRM.
1. Plaats de waarde van het **bezit LoadBehavior** aan 3.

1. Sluit de Register-editor.

Voor gedetailleerde informatie over LoadBehavior, zie de [&#x200B; Ingangen van de Registratie voor toe:voegen-ins VSTO &#x200B;](https://learn.microsoft.com/en-us/visualstudio/vsto/registry-entries-for-vsto-add-ins?view=vs-2022&redirectedfrom=MSDN#LoadBehavior) artikel.

## Problemen met beheertaken oplossen {#admintasks}

In deze sectie worden mogelijke problemen met uw geïnstalleerde AEM Document Security Extension besproken.

### Microsoft Office-toepassingen worden niet probleemloos gestart bij het installeren van Document Security Extension {#microsoft-office-applications-dont-start-smoothly-on-installing-document-security-extension}

Schakel de bufferoverloopbeveiliging in de McAfee VirusScan-console uit om ervoor te zorgen dat Office-toepassingen probleemloos starten terwijl Documentbeveiligingsextensie is geïnstalleerd en McAfee VirusScan is ingeschakeld met On-Access Scan.
