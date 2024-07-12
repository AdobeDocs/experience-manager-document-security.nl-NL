---
title: Problemen oplossen AEM Documentbeveiligingsextensie voor Microsoft Office
description: Als u problemen ondervindt bij het installeren, configureren of gebruiken van de AEM Document Security Extension for Microsoft Office, volgt u de instructies in dit document.
uuid: 61001ca8-a25a-4879-98ac-563a6eb126e7
contentOwner: khsingh
content-type: reference
topic-tags: using
discoiquuid: bdc3f174-e417-4d3e-b3af-972cdcc10133
exl-id: 98f24032-0774-47f8-bcc5-1ee37b417833
source-git-commit: 28137f26afc024d411857d44887bf69fe1ee2b81
workflow-type: tm+mt
source-wordcount: '284'
ht-degree: 0%

---

# Problemen oplossen AEM Documentbeveiligingsextensie voor Microsoft Office{#troubleshooting-aem-document-security-extension-for-microsoft-office}

## Problemen met installatie en configuratie oplossen {#troubleshootinginstallationandconfiguration}

Als u problemen hebt die en AEM de Uitbreiding van de Veiligheid van het Document voor Microsoft Office installeren vormen, zorg ervoor dat u zorgvuldig de instructies volgde die in worden vermeld - alvorens u installeert - sectie van [ installatie ](installing-configuring-aemdsext.md) artikel.

Als u alles hebt geïnstalleerd en geconfigureerd volgens de documentatie, controleert u de volgende secties op problemen die lijken op de problemen die u ondervindt.

### Documentbeveiligingsextensie kan niet worden geladen voor Microsoft Office-toepassingen {#document-security-extension-fails-to-load-for-microsoft-office-applications}

Met de eigenschap LoadBehavior in Windows-register wordt het runtimegedrag van de insteekmodule voor documentbeveiliging aangegeven. Als de eigenschap LoadBehavior is ingesteld op 3, worden alle plug-ins automatisch geladen. Voordat u de Document Security Extension for Microsoft Office installeert, moet u ervoor zorgen dat de eigenschap value LoadBehavior is ingesteld op 3.

1. Maak een back-up van het Windows-register voordat u de wijzigingen aanbrengt. Voor gedetailleerde instructies, zie [ hoe te de Registratie van Vensters wijzigen ](https://support.microsoft.com/en-us/kb/136393).
1. Navigeer in de Register-editor naar toHKEY_CURRENT_USER\Software\Microsoft\Office\Word\Addins\Adobe.DRMIntegration.WordAddin of HKEY_LOCAL_MACHINE\Software\Microsoft\Office\Word\Addins\Adobe.DRM.
1. Plaats waarde van het **bezit LoadBehavior** aan 3.

1. Sluit de Register-editor.

Voor gedetailleerde informatie over LoadBehavior, zie de [ Ingangen van de Registratie voor toe:voegen-ins VSTO ](https://msdn.microsoft.com/en-us/library/bb386106.aspx#LoadBehavior) artikel.

## Problemen met beheertaken oplossen {#admintasks}

In deze sectie worden mogelijke problemen met uw geïnstalleerde AEM Document Security Extension besproken.

### Microsoft Office-toepassingen worden niet probleemloos gestart bij het installeren van Document Security Extension {#microsoft-office-applications-dont-start-smoothly-on-installing-document-security-extension}

Om ervoor te zorgen dat Office-toepassingen probleemloos starten op een computer waarop Documentbeveiligingsextensie is geïnstalleerd en McAfee VirusScan is ingeschakeld met On-Access Scan, schakelt u de optie Buffer Overflow Protection uit in de McAfee VirusScan-console.
