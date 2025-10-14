---
title: Inleiding tot AEM Document Security Extension for Microsoft&reg; Office
description: Met Extensie Documentbeveiliging voor Microsoft&reg; Office kunt u vooraf gedefinieerde instellingen voor vertrouwelijkheid toepassen op uw Microsoft&reg; Office-bestanden.
uuid: a5428c50-fae3-4823-9e6f-0f5306e7248f
content-type: reference
topic-tags: using
discoiquuid: cf93f9f5-1fb6-4909-815e-0ffb8c6ea6d1
exl-id: 3e07c031-3f88-4bde-bdb3-b136ef5f9527
source-git-commit: 3b6a686966fb8d006bed8cc4a4bf5eebe0dfb030
workflow-type: tm+mt
source-wordcount: '1248'
ht-degree: 0%

---

# Inleiding tot AEM Document Security Extension voor Microsoft® Office{#introduction-to-aem-document-security-extension-for-microsoft-office}

De Uitbreiding van de Veiligheid van het Document van de Experience Manager® van de Adobe® voor Microsoft® Office zorgt ervoor dat slechts de mensen u toestaat Word, Excel, en de dossiers van PowerPoint kunnen gebruiken die uw intellectuele bezit bevatten. Met Documentbeveiligingsextensie voor Microsoft® Office kunt u vooraf gedefinieerde instellingen voor vertrouwelijkheid toepassen op uw bestanden.

De Document Security Extension for Microsoft® Office verbetert het Rights Management van LiveCycles en documentbeveiliging voor Adobe Experience Manager Forms. Het beschermt de dossiers van het Bureau en laat gemachtigde gebruikers toe om tot beleid-beschermde dossiers volgens gevestigde vertrouwelijkheidsmontages toegang te hebben.

## Hoe de Veiligheid van het Document intellectuele eigendom beschermt {#how-document-security-protects-intellectual-property}

Documentbeveiliging zorgt ervoor dat alleen de personen die u autoriseert, bestanden kunnen gebruiken die uw intellectuele eigendom bevatten. Met Documentbeveiliging kunt u bestanden beveiligen met vertrouwelijkheidsbeleid. A *beleid* is een inzameling van informatie die vertrouwelijkheidsmontages en een lijst van erkende gebruikers omvat. De montages u in een beleid specificeert bepalen hoe een ontvanger een dossier kan gebruiken waarop u het beleid toepast. U kunt bijvoorbeeld opgeven of ontvangers tekst kunnen afdrukken of kopiëren of wijzigingen kunnen opslaan.

Beveiliging van documenten en gebruikers maken beleid. Beheerders maken organisatiebeleid dat beschikbaar is voor alle gemachtigde gebruikers. De beheerders of de coördinatoren van de beleidsreeks kunnen groepen beleid tot stand brengen genoemd *beleidsreeksen* die aan een ondergroep van gebruikers beschikbaar zijn. Gebruikers kunnen hun eigen beleid maken, dat alleen zij kunnen gebruiken. Beheerders, beleidssetcoördinatoren en gebruikers maken beleid met behulp van de webpagina&#39;s voor documentbeveiliging.

Hoewel het beleid op de Veiligheid van het Document wordt opgeslagen, kunt u hen op dossiers door Word, Excel, of PowerPoint toepassen. Wanneer u een beleid op een dossier toepast, wordt de informatie die het dossier bevat beschermd door de vertrouwelijkheidsmontages die in het beleid worden gespecificeerd. Wanneer u het bestand distribueert dat met een beleid is beveiligd, hebben alleen geautoriseerde ontvangers toegang tot de inhoud van het bestand.

Het gebruiken van een beleid om een dossier te beschermen geeft u aan de gang zijnde controle over dat dossier, zelfs nadat u het verspreidt. U kunt gebeurtenissen controleren om te volgen wanneer en hoe de ontvangers uw dossier gebruiken. U kunt ook wijzigingen aanbrengen in het beleid, voorkomen dat gebruikers het bestand kunnen blijven openen en het beleid wijzigen dat aan het bestand is gekoppeld.

## Hoe beleid werkt {#how-policies-work}

Het beleid bevat informatie over de gemachtigde gebruikers en de vertrouwelijkheidsinstellingen die op intellectuele eigendom moeten worden toegepast. Documentbeveiliging herkent gebruikers die zijn opgenomen in een gekoppelde LDAP- of Active Directory-lijst. Gebruikers kunnen ook personen zijn die zijn uitgenodigd om zich te registreren bij Documentbeveiliging of voor wie de beheerder een account heeft gemaakt.

De vertrouwelijkheidsmontages in een beleid bepalen hoe de ontvangers dossiers kunnen gebruiken die door het beleid worden beschermd. Met beleid wordt bijvoorbeeld aangegeven of ontvangers bestanden kunnen afdrukken, inhoud naar andere bestanden kunnen kopiëren of wijzigingen in beveiligde bestanden kunnen opslaan. Het beleid kan verschillende vertrouwelijkheidsmontages voor diverse gebruikers ook specificeren.

Wanneer u een beleid op een dossier toepast, wordt de informatie die het dossier bevat beschermd door de vertrouwelijkheidsmontages die in het beleid worden gespecificeerd. Wanneer u het bestand verspreidt, worden de ontvangers die het bestand proberen te openen door Documentbeveiliging geverifieerd en wordt toegang toegestaan op basis van de bevoegdheden die in het beleid zijn opgegeven.

Nadat een beleid op een dossier wordt toegepast, kunnen de vertrouwelijkheidsmontages van het beleid op elk ogenblik worden veranderd. U kunt geautoriseerde gebruikers toevoegen of verwijderen of de rechten voor gebruikers wijzigen nadat ze het bestand hebben ontvangen. Het beleid dat op het bestand wordt toegepast, kan worden gewijzigd. De toegang tot het bestand kan worden ingetrokken, zodat iedereen met een kopie van het bestand het bestand niet meer kan openen.

Als het beleid offline toegang toestaat, kunnen de ontvangers beleid-beschermde dossiers (zonder actieve Internet of netwerkverbinding) voor de tijdspanne ook offline gebruiken die in het beleid wordt gespecificeerd.

## Hoe beleidsbeveiligde bestanden werken {#how-policy-protected-files-work}

Voor een gebruiker om beleid-beschermde Word, Excel, en de dossiers van PowerPoint te openen en te gebruiken, moet het beleid de gebruiker als ontvanger omvatten. Of, het moet anonieme toegang toestaan. En de gebruiker moet de Extensie van de Veiligheid van het Document voor Microsoft® Office hebben geïnstalleerd. Als u een bestand met documentbeveiliging wilt geven aan iemand die geen documentbeveiligingsextensie voor Microsoft® Office heeft, kunt u deze een kopie van de software geven. U kunt ze ook vertellen hoe u het bestand van uw website kunt downloaden. Als u niet het installatieprogramma hebt, kunt u het van de [&#x200B; downloadpagina &#x200B;](https://experienceleague.adobe.com/nl/docs/experience-manager-document-security/using/download-installer) downloaden.

Wanneer een gebruiker een bestand probeert te openen dat met een beleid is beveiligd, maakt de documentbeveiligingsextensie voor Microsoft® Office verbinding met Documentbeveiliging om de gebruiker te verifiëren. Als de Veiligheid van het Document aan controledossiergebruik wordt gevormd, ziet de gebruiker een bericht erop wijzend dat het dossiergebruik wordt gecontroleerd. Documentbeveiliging bepaalt welke bestandsmachtigingen de gebruiker kunnen krijgen en de gebruiker het bestand vervolgens kan gebruiken volgens de beleidsinstellingen, onder de volgende voorwaarden:

* Voor de geldigheidsperiode die in het beleid wordt gespecificeerd.
* Tot een beheerder of de persoon die het beleid toepaste, de toegang tot het bestand intrekt of het beleid wijzigt.

  Als de persoon die het beleid toepaste het beleid verandert of toegang tot het dossier terugtrekt, worden de toestemmingen van de gebruiker voor het dossier veranderd of verwijderd alhoewel de gebruiker reeds het dossier heeft. Als het bestand zelf is ingetrokken, ontvangt de gebruiker mogelijk een URL om een bijgewerkte kopie op te halen.

  Als het beleid offline toegang toestaat, kunnen de gebruikers beleid-beschermde dossiers zonder Internet of netwerkverbinding tijdens de gespecificeerde off-line huurperiode openen. Wanneer de offline leaseperiode afloopt, moet de gebruiker online gaan en synchroniseren met Documentbeveiliging, die een nieuwe leaseperiode start.

  Als het beleid offline toegang toestaat, kunnen de gebruikers beleid-beschermde dossiers zonder Internet of netwerkverbinding tijdens de gespecificeerde off-line huurperiode openen. Gebeurtenissen, zoals pogingen om het nieuwe bestand te openen, worden ook gecontroleerd en op dezelfde manier opgenomen als in het oorspronkelijke bestand.

## Documentbeveiliging gebruiken om uw bestanden te beveiligen {#using-document-security-to-protect-your-files}

U kunt beleid gebruiken om uw dossiers in diverse situaties te beschermen.

Een fabrikant accepteert bijvoorbeeld biedingen van leveranciers die onderdelen leveren voor een nieuw product. De fabrikant moet de inschrijvers specifieke informatie verstrekken om hun opmerkingen af te ronden. De fabrikant gebruikt Documentbeveiliging om de bestanden te beschermen met een beleid waarmee de bieders de bestanden kunnen openen en de informatie kunnen bekijken. Bieders kunnen de bestanden echter niet wijzigen, afdrukken of kopiëren en iedereen die geen machtiging heeft, kan de bestanden niet openen.

Nadat de fabrikant een bod heeft geaccepteerd, werkt hij het beleid bij om de succesvolle bieder toestemming te geven om wijzigingen lokaal af te drukken, te kopiëren en op te slaan. De fabrikant verwijdert ook de niet-succesvolle bieders en trekt hun toestemming om de bestanden te openen in.

Terwijl de technici van de fabrikant met de succesvolle bieder samenwerken, veranderen sommige ontwerpspecificaties in de bestanden. Om de nieuwe specificaties te publiceren, trekt de fabrikant de toegang tot sommige dossiers in en publiceert nieuwe versies. Wanneer engineers van de succesvolle bieder het bestand proberen te openen, zien ze een bericht dat de toegang tot het bestand is ingetrokken. Het bericht bevat een URL waar ze een nieuwe versie van het bestand kunnen downloaden.

## Aanvullende informatie {#additional-information}

De bronnen in deze tabel kunnen u helpen meer te weten te komen over AEM documentbeveiliging:

<table >
 <tbody>
  <tr>
   <th><p>Voor informatie over</p> </th>
   <th><p>Zie</p> </th>
  </tr>
  <tr>
   <td><p>Help bij AEM</p> </td>
   <td><p><a href="https://experienceleague.adobe.com/nl/docs/experience-manager-65/content/forms/administrator-help/get-started/configure-general-aem-forms-settings"> Hulp van de Beheerder </a> of, op de het beleidspagina's van de Veiligheid van het Document, klik de verbinding van de Hulp in de hoger-juiste hoek van een pagina.</p> </td>
  </tr>
  <tr>
   <td><p>Reparatie-updates, technische notities en aanvullende informatie over deze productversie</p> </td>
   <td><p><a href="https://experienceleague.adobe.com/nl?support-solution=General&support-tab=home#support">Technische ondersteuning Experience Cloud</a></p> </td>
  </tr>
 </tbody>
</table>
