---
title: Beveiliging-extensie AEM document gebruiken voor Microsoft&reg; Office
description: U kunt controleren hoe de ontvangers uw beleid-beschermde dossiers gebruiken, ongeacht hoe wijd u hen verspreidt. In dit document wordt uitgelegd hoe u bestanden kunt beschermen en hoe u met beveiligde bestanden kunt werken.
uuid: db4abbc8-eb21-4f4a-9950-224ada95ce66
content-type: reference
topic-tags: using
discoiquuid: f4c2460c-174f-4e4d-b804-1eb051d2781e
exl-id: 667a9718-b865-4911-96c2-7c08f75e0732
source-git-commit: 6cf19ed9439e5be5a4c2e2fa2458879f37c25b96
workflow-type: tm+mt
source-wordcount: '6136'
ht-degree: 0%

---

# AEM Document Security Extension gebruiken voor Microsoft® Office{#using-aem-document-security-extension-for-microsoft-office}

## Protect-bestanden met AEM Document Security Extension {#usingaemdocumentsecurityextensiontoprotectfiles}

U kunt controleren hoe de ontvangers uw beleid-beschermde dossiers gebruiken, ongeacht hoe wijd u hen verspreidt.

Met de Document Security Extension for Microsoft® Office kunt u de volgende taken uitvoeren:

* Verbinding met documentbeveiliging configureren
* Een beleid toepassen op een bestand
* Open de Web-pagina&#39;s van de Veiligheid van het Document om gebruikersbeleid tot stand te brengen en te beheren
* Beleidsbescherming uit een bestand verwijderen
* Het beleid wijzigen dat wordt toegepast op een bestand
* Open de Web-pagina&#39;s van de Veiligheid van het Document om toegang tot dossiers in te trekken of het beleid voor het dossier te veranderen
* Open de Web-pagina&#39;s van de Veiligheid van het Document om de de controlegeschiedenis van het dossier te bekijken

### Verbinding maken met een documentbeveiligingsserver {#connect-to-a-document-security-server}

Als u beleid wilt toepassen op bestanden, moet u de verbindingsinstellingen configureren voor Documentbeveiliging. Afhankelijk van de manier waarop Extensie Documentbeveiliging voor Microsoft® Office is geïnstalleerd, hebt u mogelijk al standaardverbindingsinstellingen. U kunt verbindingsinstellingen toevoegen voor een of meer instanties van Documentbeveiliging. U kunt serverinformatie opvragen bij de documentbeveiligingsbeheerder.

Stel de server in die u wilt gebruiken om bestanden te beveiligen of om uw beveiligde bestanden te beheren als de standaardserver. Wanneer u een beleid toepast op een nieuw dossier of de Web-pagina&#39;s van de Veiligheid van het Document opent, verbindt de Uitbreiding van de Veiligheid van het Document voor Microsoft® Office met de standaardserver. Als u bestanden beveiligt met meerdere instanties van Documentbeveiliging, moet u de standaardinstelling voor de server wijzigen wanneer u overschakelt tussen servers. U kunt bestanden openen die zijn beveiligd door elke instantie van Documentbeveiliging, zolang u over de machtiging beschikt om het bestand te openen.

Als op de documentbeveiligingsserver verificatie op basis van certificaten wordt toegepast, moet u het certificaat installeren dat u op uw lokale computer hebt ontvangen. U moet een certificaatverificatie kiezen en het certificaat opgeven dat u wilt gebruiken voor verificatie.

Nadat u de verbindingsmontages voor een geval van de Veiligheid van het Document in één toepassing van Microsoft® Office vormde, wordt het gevormd voor elk van Word, Excel, en PowerPoint.

#### Het clientcertificaat installeren {#install-the-client-side-certificate}

Als u toegang moet krijgen tot de webpagina&#39;s voor documentbeveiliging via certificaatverificatie of tweerichtingsverificatie, ontvangt u het certificaat dat u op uw lokale computer moet installeren. U ontvangt een certificaatbestand (.PFX- of .P12-bestand) en het bijbehorende wachtwoord.

1. Sla het certificaatbestand op uw lokale computer op.
1. Dubbelklik het certificaatdossier om de Tovenaar van de Invoer van het Certificaat te openen en **daarna** te klikken.
1. Klik **daarna** als het certificaatdossier in filename vakje vermeld is. Klik **doorbladeren** als u van een ander certificaat wilt de plaats bepalen.
1. Ga het wachtwoord in dat u hebt ontvangen en klik **daarna**.
1. Voor de dialoog van de Opslag van het Certificaat, uitgezochte Plaats Alle Certificaten in de volgende Opslag, en klik **doorbladeren**.
1. In de Uitgezochte dialoog van de Opslag van het Certificaat, uitgezochte Persoonlijk, klik **O.K.**, klik **daarna**, en klik dan **Afwerking**.

#### Verbindingsinstellingen configureren {#configure-connection-settings}

1. In de Uitbreiding van de Veiligheid van het Document voor Microsoft® Office 2010 en Bureau 2013, op het **lusje van de Veiligheid van het 0} Document, uitgezocht** kies Server **.**
1. Of klik **Nieuw** om verbindingsmontages tot stand te brengen, of een bestaande verbinding te selecteren en **te klikken geeft** uit.
1. Typ een naam voor de verbinding in het **vakje van de Naam**. U kunt elke gewenste naam gebruiken.
1. Typ het adres van de server in het **vakje van het Adres van de Server**.
1. Typ de serverhaven in de **doos van de Haven**.
1. (Optioneel) Als u uw gebruikersnaam en wachtwoord wilt onthouden, selecteert u **Wachtwoord onthouden op deze computer** en typt u uw gebruikersnaam en wachtwoord in de juiste vakken. Het wordt aanbevolen deze optie niet in te schakelen als andere personen toegang hebben tot de computer.
1. Klik **verbinden met deze server**. Documentbeveiligingsextensie voor Microsoft® Office probeert verbinding te maken met de server die u hebt opgegeven. Voer afhankelijk van het opgegeven verificatietype een van de volgende handelingen uit:

   **Gebruikersnaam en Wachtwoord**

   Voer de gebruikersnaam en het wachtwoord in die u van de documentbeveiligingsbeheerder hebt ontvangen.

   **Authentificatie van het Certificaat**

   Kies deze optie om het certificaat te selecteren dat u hebt ontvangen en in uw persoonlijke certificaatarchief hebt geïnstalleerd.

   Als er slechts één verificatietype is geconfigureerd in Documentbeveiliging, wordt alleen die optie weergegeven.

>[!NOTE]
>
>Als u geen verbinding kunt maken met de server, opent u de webpagina&#39;s voor documentbeveiliging in Internet Explorer. Als u geen verbinding met de server kunt maken via Internet Explorer of als een dialoogvenster een waarschuwing over het servercertificaat weergeeft, kan de Document Security Extension for Microsoft® Office geen verbinding met de server maken. Neem contact op met de serverbeheerder voor hulp.

>[!NOTE]
>
>Als u geen verbinding kunt maken met Documentbeveiliging, wordt een bericht weergegeven met de melding dat de gebruikersnaam en het wachtwoord onjuist zijn. Controleer de configuratie-instellingen en probeer het opnieuw. Dit bericht wordt mogelijk weergegeven als u om een andere reden geen verbinding kunt maken. Als u voor het eerst verbinding maakte met de server, controleert u of u de servernaam en poort correct hebt ingesteld.

#### De standaardserver opgeven {#specify-the-default-server}

1. Ga als volgt te werk:

   * In de Uitbreiding van de Veiligheid van het Document voor Microsoft® Office 2010 en Bureau 2013 op het **lusje van de Veiligheid van het 0} Document, uitgezocht** kies Server **.**

1. Selecteer een server om als gebrek te specificeren en **te klikken plaats Gebrek**. Er wordt een sterretje weergegeven naast de standaardserver.

### Het gebruiken van de leveranciers van de authentificatie van de Derden {#using-third-party-authentication-providers}

U kunt externe verificatieproviders gebruiken met AEM Forms Document Security. Met deze verificatieproviders kunt u een extra toegangslaag toevoegen aan de beveiligde documenten. AEM Forms Document Security ondersteunt de volgende uitgebreide verificatieworkflows:

* Uitgebreide verificatie met de standaard AEM Forms URL
* Uitgebreide verificatie met een aangepaste URL
* Standaard uitgebreide verificatieworkflow met externe identiteitsproviders geconfigureerd op AEM Forms op JEE-server
* Aangepaste uitgebreide verificatieworkflow met externe identiteitsproviders geconfigureerd op AEM Forms op JEE-server
* Uitgebreide verificatie met behulp van een aangepaste pagina voor SAML-verificaties

#### Uitgebreide verificatie met standaard AEM Forms URL {#extended-authentication-using-default-aem-forms-url}

U kunt de standaard AEM Forms-URL gebruiken voor uitgebreide verificatie. De standaardlandingspagina bevat branding voor Adoben. Bovendien worden standaard AEM Forms-instellingen gebruikt voor het gebruik van de standaard AEM Forms-URL voor uitgebreide verificatie.

Voer de volgende stappen uit om uitgebreide verificatie in te schakelen met de standaard bestemmings-URL voor Adoben:

1. Open de gebruikersinterface voor AEM Forms Admin.
1. Ga naar Services > Documentbeveiliging > Configuratie > Serverconfiguratie.
1. Schakel de optie Uitgebreide verificatie toestaan in.
1. Geef de standaard URL voor het porteren van URL voor uitgebreide verificatie op. De standaard-URL is http://localhost:8080/edc/extendedauthentication/welcome.jsp.

   Klik **[!UICONTROL sparen]**.

   >[!NOTE]
   >
   >Gebruik een volledig gekwalificeerde hostnaam in de URL. Adobe raadt u aan het HTTPS-protocol te gebruiken.

   Nu is AEM Forms Document Security geconfigureerd voor uitgebreide verificatie met de standaard AEM Forms-landings-URL.

   ![](assets/third-party-authentication.png)

#### Uitgebreide verificatie met een aangepaste bestemmings-URL {#extended-authentication-with-a-custom-landing-url}

U kunt een aangepaste URL voor uitgebreide verificatie gebruiken. Het biedt de flexibiliteit om een aangepaste verificatiepagina met aangepaste branding weer te geven. Bijvoorbeeld branding voor uw organisatie.

U kunt de aangepaste verificatiepagina in een oorlogsbestand verpakken en het oorlogsbestand op AEM Forms Server implementeren. Het oorlogsdossier bevat volledige logica om gebruikersgeloofsbrieven goed te keuren en tegen de Server van AEM Forms voor authentiek te verklaren. AEM Forms Document Security heeft de volgende vereisten voor de aangepaste verificatiepagina:

* De verificatiepagina moet gebruikersnaam als j_username en wachtwoord verzenden als j_password. De pagina moet de parameters source_url en login_url ook als verborgen verzenden.
* Na geslaagde verificatie moet de pagina automatisch worden gesloten.

Uitgebreide verificatie inschakelen met een aangepaste bestemmings-URL:

1. Implementeer het WAR-bestand voor aangepaste verificatie naar AEM Forms Server.
1. Open de gebruikersinterface voor AEM Forms Admin.
1. Ga naar Services > Documentbeveiliging > Configuratie > Serverconfiguratie.
1. Schakel de optie Uitgebreide verificatie toestaan in en geef een aangepaste URL voor het parseren van de uitgebreide verificatie op.
1. Voeg de volgende ingangen aan het `config.xml` dossier onder de knoop SSO na ingang *&lt;node name=&quot;AllowedUrls&quot;>* toe:

   >[!NOTE]
   >
   >&lt;entry key=&quot;sso-l&quot; value=&quot;/ sample_/login.jsp&quot;/> `!!discoiqbr!!` &lt;entry key=&quot;sso-s&quot; value=&quot;/ sample_/welcome.jsp&quot;> `!!discoiqbr!!` &lt;entry key=&quot;sso-o&quot; value=&quot;/ sample_/logout.jsp&quot;/> `!!discoiqbr!!`

   Voor geleidelijke informatie bij het bijwerken van het config.xml- dossier, zie [ manueel het uitgeven van het dossier van de documentveiligheidsconfiguratie ](https://experienceleague.adobe.com/en/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions#manually_editing_the_document_security_configuration_file).

   Nu is de beveiliging van AEM Forms-documenten geconfigureerd voor uitgebreide verificatie met een aangepaste bestemmings-URL

#### Standaard uitgebreide verificatieworkflow met externe identiteitsproviders geconfigureerd op AEM Forms Server {#default-extended-authentication-workflow-with-third-party-identity-providers-configured-on-aem-forms-server}

Voor uitgebreide verificatie kunnen verschillende typen verificatie worden gebruikt die beschikbaar zijn op AEM Forms Server. Bijvoorbeeld, SAML, [ wat zijn meer voorbeelden ].

Opmerking: als SAML-providers zijn geconfigureerd op AEM Forms Server, wordt een pagina met alle identiteitsproviders weergegeven die zijn geconfigureerd voor SAML-verificatie, voordat de bestemmings-URL wordt weergegeven.

Het volgende scherm wordt weergegeven wanneer een beveiligd document wordt geopend in Acrobat.

#### Aangepaste uitgebreide verificatieworkflow wanneer SAML-providers zijn geconfigureerd op AEM Forms Server {#custom-extended-authentication-workflow-when-saml-providers-are-configured-on-aem-forms-server}

Als de leveranciers van SAML op de Server van AEM Forms worden gevormd, dan alvorens het landen URL te tonen, wordt een pagina getoond die alle identiteitsleveranciers bevat die voor de authentificatie van SAML worden gevormd.

De voorwaarden om een douane uitgebreide authentificatiewerkschema te vormen wanneer de leveranciers van SAML op de Server van AEM Forms worden gevormd zijn:

* SAML-verificatie is geconfigureerd op AEM Forms Server
* De oorlog van de douane, die een pagina van de douaneauthentificatie en volledige logica bevat om gebruikersgeloofsbrieven goed te keuren en tegen de Server van AEM Forms voor authentiek te verklaren, wordt opgesteld aan de Server van AEM Forms.

#### Aangepaste pagina gebruiken voor SAML-verificatie {#using-custom-page-for-listing-saml-authentications}

U kunt ook een aangepaste pagina weergeven met alle verificatieproviders die op AEM Forms Server zijn geconfigureerd. Zo&#39;n pagina maken:

1. Verpak de pagina van de douaneauthentificatie in een oorlogsdossier en stel het oorlogsdossier aan de Server van AEM Forms op. Het oorlogsdossier bevat volledige logica om gebruikersgeloofsbrieven goed te keuren en tegen de Server van AEM Forms voor authentiek te verklaren.
1. Open AEM Forms Admin UI en navigeer aan **[!UICONTROL Montages]** > **[!UICONTROL Gebruikersbeheer]** > **[!UICONTROL Configuratie]** > **[!UICONTROL de Montages van de Dienstverlener van SAML]**.
1. Voeg het volgende aan het gebied van Eigenschappen van de Douane toe en klik **[!UICONTROL sparen]**.

   *saml.sp.discRecovery.url=/demoJSP/saml_discovery.jsp*

   Nu, wordt de Veiligheid van het Document van AEM Forms gevormd om een douanepagina te tonen die alle gevormde authentificatieleveranciers bevat.

### Een gebruikersaccount aanvragen {#obtaining-a-user-account}

Als u nog geen account voor documentbeveiliging hebt, kan Documentbeveiliging het registratieproces starten wanneer deze gebeurtenissen zich voordoen:

* Een gebruiker van de Veiligheid van het Document die u een beleid-beschermd dossier wil verzenden voegt u aan een beleid toe.
* De beheerder van de Veiligheid van het Document leidt tot een rekening voor u.

Nadat u zich hebt geregistreerd en uw account hebt geactiveerd, kunt u met beleid beveiligde bestanden gebruiken waarvoor u toestemming hebt gekregen om deze te gebruiken.

>[!NOTE]
>
>Als u een bestand ontvangt dat met een beleid is beveiligd en geen account voor documentbeveiliging hebt, neemt u contact op met de persoon die u het bestand voor hulp heeft gestuurd. Als u een uitnodiging tot registratie ontvangt, neemt u ook contact op met de afzender.

Als u een e-mailuitnodiging voor registratie ontvangt van Documentbeveiliging, kunt u zich registreren met de URL in de e-mail om de online registratiepagina te openen. Na je inschrijving ontvang je een tweede bericht over het activeren van je account.

#### Een externe gebruikersaccount verkrijgen {#obtain-an-external-user-account}

1. Open de registratie-e-mail voor documentbeveiliging. De URL die het bericht bevat, is een koppeling naar de pagina Registratie van externe gebruikers van documentbeveiliging. Als u geen registratiebericht ontvangt, contacteer de persoon die u het dossier voor hulp verzond.
1. Klik op de URL of kopieer deze en plak deze in uw browser.
1. Typ uw naam, organisatie en wachtwoord in de desbetreffende vakken. Uw wachtwoord kan elke combinatie van acht tekens zijn.

   >[!NOTE]
   >
   >Zorg ervoor dat u een wachtwoord kiest dat u gemakkelijk kunt onthouden; er is geen methode beschikbaar voor het zoeken naar vergeten wachtwoorden.

1. Klik **Register**. Er wordt een bericht weergegeven waarin u wordt gevraagd uw e-mail te controleren op een activeringsbericht.
1. Open het bevestigingsbericht voor documentbeveiliging.
1. Klik op de URL die in het bericht wordt weergegeven.
1. Klik op de koppeling naar de aanmeldpagina.
1. In het **vakje van de Gebruikersnaam**, typ het e-mailadres u onder de Veiligheid van het Document wordt geregistreerd. Dit e-mailadres is uw standaardgebruikersnaam voor documentbeveiliging.
1. In het **vakje van het Wachtwoord**, typ het wachtwoord u creeerde toen u registreerde.
1. Klik **Login**.

### Beleid maken en beheren {#creating-and-managing-policies}

Als u toestemming van de beheerder van de Veiligheid van het Document hebt, kunt u beleid tot stand brengen om op uw eigen dossiers op de pagina van het Beleid van de Web-pagina&#39;s van de Veiligheid van het Document van toepassing te zijn.

Sommige beleidsinstellingen die beschikbaar zijn voor het maken van beleid op de webpagina&#39;s Documentbeveiliging, worden niet ondersteund voor Word-, Excel- en PowerPoint-bestanden. In de volgende tabellen wordt beschreven hoe de beleidsmachtigingen worden toegewezen aan Word, Excel en PowerPoint-functies.

<table>
 <thead>
  <tr>
   <th><p>Machtigingen</p></th>
   <th><p>Word-, Excel- en PowerPoint-ondersteuning</p></th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td><p>Afdrukken &gt; Niet toegestaan</p></td>
   <td><p>Afdrukken van het bestand is niet toegestaan.</p></td>
  </tr>
  <tr>
   <td><p>Afdrukken &gt; Toegestaan</p></td>
   <td><p>U mag het bestand afdrukken.</p><p><strong> Nota </strong>: <i> als een beleid de toestemming van het Exemplaar maar niet de toestemming van de Druk geeft, kan de inhoud die aan een ander dossier wordt gekopieerd worden gedrukt.</i></p></td>
  </tr>
  <tr>
   <td><p>Afdrukken &gt; Lage resolutie. Alleen</p></td>
   <td><p>Niet van toepassing.</p></td>
  </tr>
  <tr>
   <td><p>Wijzigen &gt; Alles</p></td>
   <td><p>Het bestand kan worden gewijzigd.</p><p>Als deze machtiging niet is gegeven, kunt u beveiligde Word- en Excel-bestanden niet wijzigen. U kunt PowerPoint-bestanden wijzigen, maar u kunt de wijzigingen of presentaties voor gewijzigde bestanden niet opslaan.</p></td>
  </tr>
  <tr>
   <td><p>Wijzigen &gt; Niet toegestaan</p></td>
   <td><p>Gebruikers kunnen beveiligde bestanden niet wijzigen.</p></td>
  </tr>
  <tr>
   <td><p>Wijzigen &gt; Pagina's wijzigen</p></td>
   <td><p>Niet van toepassing.</p><p>Dit omvat het invoegen, verwijderen en roteren van pagina's.</p></td>
  </tr>
  <tr>
   <td><p>Wijzigen &gt; Fill &amp; Sign</p></td>
   <td><p>Niet van toepassing.</p></td>
  </tr>
  <tr>
   <td><p>Off line</p></td>
   <td><p>Het bestand kan offline worden geopend.</p></td>
  </tr>
  <tr>
   <td><p>Kopiëren</p></td>
   <td><p>Bestandsinhoud kan naar andere bestanden worden gekopieerd.</p></td>
  </tr>
  <tr>
   <td><p>Reader scherm </p></td>
   <td><p>Schermlezers (apparaten voor gebruikers met een visuele handicap) kunnen de bestandsinhoud lezen.</p></td>
  </tr>
  <tr>
   <td><p>Geldigheid machtiging</p></td>
   <td><p>Ondersteund.</p></td>
  </tr>
 </tbody>
</table>

<table>
 <thead>
  <tr>
   <th><p>Algemene instellingen</p></th>
   <th><p>Word-, Excel- en PowerPoint-ondersteuning</p></th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td><p>Geldigheidsperiode</p></td>
   <td><p>Ondersteund.</p></td>
  </tr>
  <tr>
   <td><p>Controledocument</p></td>
   <td><p>Ondersteund.</p></td>
  </tr>
  <tr>
   <td><p>Automatische offline leaseperiode</p></td>
   <td><p>Ondersteund.</p></td>
  </tr>
  <tr>
   <td><p>Externe machtigingsproviders</p></td>
   <td><p>Ondersteund.</p></td>
  </tr>
 </tbody>
</table>

<table>
 <thead>
  <tr>
   <th><p>Geavanceerde instellingen</p></th>
   <th><p>Word-, Excel- en PowerPoint-ondersteuning</p></th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td><p>Dynamische watermerken</p></td>
   <td><p>Ondersteund.</p></td>
  </tr>
  <tr>
   <td><p>Certificatie-plug-ins</p></td>
   <td><p>Niet van toepassing.</p></td>
  </tr>
  <tr>
   <td><p>Versleutelingsalgoritme en sleutellengte </p></td>
   <td><p>Alle opties worden ondersteund.</p></td>
  </tr>
  <tr>
   <td><p>Documentbeperking</p></td>
   <td><p>Alle bestandsinhoud wordt altijd versleuteld, ongeacht de instelling in het beleid.</p></td>
  </tr>
  <tr>
   <td><p>Foutbericht Toegang geweigerd</p></td>
   <td><p>Ondersteund.</p></td>
  </tr>
 </tbody>
</table>

Voor meer informatie over het creëren van en het leiden van beleid, zie [ Eind - de Hulp van de Gebruiker van de Veiligheid van het Document ](https://help.adobe.com/en_US/AEMForms/6.1/RMHelp/).

### Beleid toepassen {#applying-policies}

U kunt om het even welk beschikbaar beleid op een dossier, met inbegrip van beleid toepassen dat u creeerde en beleid dat deel van beleidsreeksen uitmaakt die u toegang tot hebt. Voordat u een beleid toepast, moet u het bestand opslaan.

Nadat u een beleid toepaste, wordt het toegevoegd aan de Recent Gebruikte lijst op het menu van de Veiligheid van het Document van het AEM om het voor u gemakkelijker te maken om uw het vaakst gebruikte beleid toe te passen. In de lijst Onlangs gebruikt wordt alleen beleid weergegeven voor de server waarmee u bent verbonden of voor uw standaardserver als u zich niet hebt aangemeld bij een andere instantie Documentbeveiliging.

>[!NOTE]
>
>Het beleid kan slechts op Word (.doc, .docx, .docm), Excel (.xls, .xlsx, .xlsm), en de dossiers van PowerPoint (.ppt, .pptx, .pptm) in Microsoft® Office 2010 en 2013 worden toegepast. U kunt geen beleid op de malplaatjedossiers van Word (.dot), de malplaatjedossiers van Excel (.xlt), en de dossiers van het het ontwerpmalplaatje van PowerPoint (.pot) toepassen.

#### Een beleid toepassen {#apply-a-policy}

1. In de Uitbreiding van de Veiligheid van het Document voor Microsoft® Office 2010 en 2013 op het **lusje van de Veiligheid van het 0} Document, uitgezochte** Veilig > kiest Beleid **.**

   Als u gebruikersnaam en wachtwoord hebt gekozen als verificatiemethode op de server en nog geen aanmeldingsgegevens voor Documentbeveiliging hebt opgegeven, wordt u in een dialoogvenster gevraagd om uw gebruikersnaam en wachtwoord.

1. Selecteer een beleid van de lijst en klik **toepassen**.
1. Sla het bestand op.

#### Pas een onlangs gebruikt beleid toe {#apply-a-recently-used-policy}

1. In de Uitbreiding van de Veiligheid van het Document voor Microsoft® Office 2010 en 2013, op het **lusje van de Veiligheid van het 0} Document, uitgezochte** Veilig **> *[Naam van het Beleid]*.**
1. Sla het bestand op.

## Werken met de beleidsbeveiligde bestanden {#usingaemdocumentsecurityextensionpolicyprotectedfiles}

De uitgever van het dossier bezit het intellectuele bezit in beleid-beschermde dossiers, die de Veiligheid van het Document beschermt.

U kunt met beleid beveiligde bestanden gebruiken, ongeacht of dit interne of externe bestanden zijn van de organisatie van de uitgever van het bestand. Documentbeveiliging moet u herkennen om met beleid beveiligde bestanden te openen. Dit moet gebeuren via LDAP/Active Directory. Of dit moet gebeuren als lokale gebruiker van LiveCycle/AEM formulieren op JEE of door zich te registreren na een uitnodiging.

Als u een bestand ontvangt dat met een beleid is beveiligd en geen account voor documentbeveiliging hebt, neemt u contact op met de afzender voor hulp. Als u een uitnodiging tot registratie ontvangt, neemt u ook contact op met de afzender.

### Werken met bestanden die met een beleid zijn beveiligd in Microsoft® Office {#working-with-policy-protected-files-in-microsoft-office}

De uitbreiding van de Veiligheid van het Document voor Microsoft® Office beperkt bepaalde Word, Excel, en functionaliteit PowerPoint om het intellectuele bezit van de dossieruitgever te beschermen. Als u geen toestemming hebt om het bestand te wijzigen, kunt u er geen wijzigingen in opslaan.

Als u met een bestand werkt dat met een beleid is beveiligd, zijn bepaalde productfuncties mogelijk niet beschikbaar of werken deze mogelijk niet zoals gewoonlijk. Als een niet-beveiligd bestand geopend is, zijn de meeste functies ingeschakeld, behalve de functies waarmee u inhoud uit een met een beleid beveiligd bestand kunt importeren of kopiëren zonder dat u kopieer- of exportmachtigingen hebt.

>[!NOTE]
>
>Als u de Extensie-gesteunde toepassingen van het Bureau van de Veiligheid van het Document gebruikt, adviseert men dat u het plaatsen van Vensters DEP onbruikbaar maakt. Schakel de optie Buffer Overflow Protection uit in de McAfee VirusScan-console om ervoor te zorgen dat Office-toepassingen probleemloos kunnen worden gestart op een computer met Documentbeveiliging en McAfee VirusScan-scan met On-Access Scan ingeschakeld. Deze aanpassing helpt potentiële conflicten te voorkomen.

Als een functie niet beschikbaar is, zijn de opdrachtnaam in het menu en de bijbehorende werkbalkknop niet beschikbaar. Als u de muisaanwijzer boven de opdracht of knop houdt in de Documentbeveiligingsextensie voor Microsoft® Office, geeft knopinfo aan dat de opdracht niet beschikbaar is in Documentbeveiliging.

### Beleidsbeveiligde bestanden openen {#opening-policy-protected-files}

U kunt met beleid beveiligde bestanden openen met dezelfde methoden als voor het openen van andere bestanden. Als u zich nog niet hebt aangemeld bij Documentbeveiliging, wordt u gevraagd dit te doen. Dat wil zeggen dat als u niet bent verbonden met internet en u het bestand offline kunt openen. Als u het aanmeldingsproces annuleert, wordt de toegang geweigerd.

Als u geen toestemming had om het dossier te openen, wordt u geïnformeerd dat de toegang wordt ontkend. Als de toegangsrechten voor het bestand zijn ingetrokken, kunt u ook naar een bijgewerkte versie van het bestand worden geleid als er een beschikbaar is. Neem contact op met de bestandsuitgever als u geen bestand met een bestandsbeveiliging kunt openen dat is beveiligd met een beleid.

Wanneer een beveiligd bestand is geopend, wordt in de titelbalk die volgt op de bestandsnaam, aangegeven dat het bestand is beveiligd door AEM Documentbeveiliging.

Wanneer u een beveiligd document opent in Documentbeveiligingsextensie voor Microsoft® Office vanaf SharePoint Server, moet u ervoor zorgen dat het Office-programma dat is gekoppeld aan het bestandstype, zoals Word, Excel of PowerPoint, is geopend. Als u het bestand probeert te openen zonder de bijbehorende toepassing te openen, wordt het document mogelijk niet geopend en wordt een foutbericht weergegeven dat u de toepasselijke plug-in moet installeren. Naast het openen van de vereiste toepassing, raadt de Adobe u aan de cachemap te wissen. Doe dit voordat u een beveiligd document opent in Documentbeveiligingsextensie voor Office vanaf SharePoint Server. Wanneer u een beveiligd document opent vanaf SharePoint Server, worden bovendien alle machtigingen voor het document uitgeschakeld, ongeacht het beleid dat is toegepast.

Afhankelijk van de verificatiemethode die is geïmplementeerd op Documentbeveiliging, wordt u mogelijk gevraagd om de verificatiemethode te kiezen wanneer u een beveiligd document opent. Als Documentbeveiliging meerdere verificatiemethoden ondersteunt, worden de verificatieopties aan u getoond. Als een Document Security-server bijvoorbeeld zowel gebruikersnaam/wachtwoord als certificaatverificatie biedt, kunt u de juiste verificatiemethode kiezen. Als op certificaat-gebaseerde authentificatie wordt toegelaten, werd u ertoe aangezet om het certificaat te gebruiken dat u hebt ontvangen en geïnstalleerd.

De gebruikerservaring bij het openen van beveiligde bestanden is afhankelijk van de wederzijdse verificatieconfiguratie op de server. Als slechts één geldig clientcertificaat is geïnstalleerd, wordt er geen verificatiedialoogvenster weergegeven en worden de bestanden geopend. Als er echter meerdere clientcertificaten op een computer zijn geïnstalleerd, wordt er een dialoogvenster voor verificatie weergegeven. De gebruiker moet een geldig certificaat kiezen om het beveiligde bestand te openen.

### Beleidsbescherming uit een bestand verwijderen {#removing-policy-protection-from-a-file}

Als u hiervoor toestemming hebt gekregen, kunt u de beleidsbeveiliging verwijderen uit bestanden die u hebt beveiligd. Als u dit doet, wordt het bestand niet meer beveiligd door Documentbeveiliging.

1. In de Uitbreiding van de Veiligheid van het Document voor Microsoft® Office 2010 en 2013, op het **lusje van de Veiligheid van het 0} Document, uitgezochte** verwijdert **.**

   Als u nog geen aanmeldingsgegevens voor Documentbeveiliging hebt opgegeven, wordt u in een dialoogvenster gevraagd om uw gebruikersnaam en wachtwoord.

>[!NOTE]
>
>Als u geen beleid kunt verwijderen uit een bestand dat u hebt beveiligd, neemt u contact op met de beheerder van documentbeveiliging.

### Beveiligingsinstellingen weergeven {#viewing-security-settings}

U kunt de machtigingen weergeven die u hebt voor het huidige bestand voor afdrukken. U kunt ook machtigingen voor het huidige bestand weergeven wanneer u kopieert van, wijzigt en offline toegang zoekt tot het bestand, samen met de geldigheidsperiode van het bestand.

In Document Security Extension for Microsoft® Office 2010 geeft de groep Security Status op het tabblad Documentbeveiliging uw machtigingen voor het bestand weer.

Ga als volgt te werk:

* In de Uitbreiding van de Veiligheid van het Document voor Microsoft® Office 2010 en 2013, op het **lusje van de Veiligheid van het Document**, in de **3} groep van de Status van de Veiligheid, klik om het even welk punt.**

### Documenten opslaan wanneer Beleid automatisch toepassen is ingeschakeld {#saving-documents-when-auto-apply-policy-is-enabled}

Als de beheerder de functie voor automatisch toepassen heeft ingeschakeld, wordt elk document dat u maakt of bewerkt automatisch beveiligd wanneer u het document opslaat.

Als het beleid voor automatisch toepassen is ingeschakeld, wordt u bij Documentbeveiliging voor Microsoft® Office gevraagd u aan te melden bij de Document Security-server. Voer uw gebruikersnaam en wachtwoord in zodat de server u kan verifiëren. Als u de juiste aanmeldingsgegevens hebt opgegeven, wordt het document opgeslagen en beveiligd.

>[!NOTE]
>
>Als u zich niet kunt aanmelden bij Documentbeveiliging, wordt het document mogelijk wel of niet opgeslagen. Deze situatie hangt van af hoe uw Beheerder het Auto-apply beleid heeft gevormd. Vraag de beheerder hoe documenten in deze situatie worden verwerkt.

### Synchroniseren voor offline toegang {#synchronizing-for-offline-access}

Met beleidsregels kunt u bestanden openen terwijl u offline bent en geen verbinding hebt met Documentbeveiliging. U moet zich eerder bij de Veiligheid van het Document hebben aangemeld om uw geloofsbrieven met de server te vestigen alvorens u off-line kunt werken. Als u offline met bestanden wilt werken, raadt de Adobe u aan te synchroniseren met Documentbeveiliging. Doe dit voordat u de verbinding verbreekt om ervoor te zorgen dat de beleidsinstellingen voor uw bestanden zijn bijgewerkt met de server. Adobe raadt u ook aan het bestand één keer online te openen voordat u het offline opent. Als u het bestand niet één keer online opent of synchroniseert met de server, kunt u mogelijk nog steeds met een beleid beveiligde bestanden gebruiken terwijl u offline bent. De offline leaseperiode mag echter niet zijn verlopen en de beleidsinstellingen voor het bestand mogen niet zijn gewijzigd sinds u de laatste keer handmatig of automatisch met de server hebt gesynchroniseerd.

Ga als volgt te werk:

* In de Uitbreiding van de Veiligheid van het Document voor Microsoft® Office 2010 en 2013, op het **lusje van de Veiligheid van het 0} Document, uitgezocht** synchroniseer Off-line **.**

  ***nota **: Synchronize off-line knoop is beschikbaar alhoewel de gebruiker geen off-line toestemming voor het document heeft. Nochtans, doet het selecteren van de knoop niets.*

### Werken met dynamische watermerken {#working-with-dynamic-watermarks}

De Uitbreiding van de Veiligheid van het document voor Microsoft® Office steunt de opneming van dynamische tekst-gebaseerde watermerken in beleid-beschermde documenten. Een dynamisch watermerk kan informatie bevatten die kan worden gewijzigd, zoals de datum, de tijd, de gebruikersnaam of de naam van het beleid. Als een gebruiker een bestand afdrukt dat met een beleid is beveiligd en dat een dynamisch watermerk en de machtiging om af te drukken bevat, wordt het watermerk in de uitvoer weergegeven.

Documentbeveiligingsextensie ondersteunt geen uitgebreide watermerkfuncties. Veelzijdige watermerkfuncties zijn onder andere watermerken op basis van PDF, meerdere elementen in een watermerk en tekstopmaakopties. Deze omvatten ook het paginabereik.

U kunt een dynamisch watermerk maken met behulp van de webpagina&#39;s voor documentbeveiliging. Voor meer informatie, zie [ Eind - de Hulp van de Gebruiker van de Veiligheid van het Document ](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/forms/administrator-help/work-with-document-security/document-security).

Documentbeveiligingsextensie voor Microsoft® Office biedt ondersteuning voor de volgende watermerkfuncties:

<table>
 <thead>
  <tr>
   <th><p>Opties van het watermerk voor documentbeveiliging</p></th>
   <th><p>Word-, Excel- en PowerPoint-ondersteuning</p></th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td><p>Beleidsnaam</p></td>
   <td><p>Ondersteund.</p></td>
  </tr>
  <tr>
   <td><p>Watermerknaam</p></td>
   <td><p>Ondersteund.</p></td>
  </tr>
  <tr>
   <td><p>Als achtergrond gebruiken</p></td>
   <td><p>Het weergavegedrag van een dynamisch watermerk is hetzelfde, ongeacht of u de optie Als achtergrond gebruiken selecteert.</p><p>Voor Word 2010 en 2013 wordt het dynamische watermerk alleen weergegeven in de weergave Afdruklayout en Afdrukvoorbeeld. </p><p>Voor Excel 2010 en 2013 wordt deze ook weergegeven in de weergaven Afdrukvoorbeeld en Pagina-indeling.</p></td>
  </tr>
  <tr>
   <td><p>Verticale positie</p></td>
   <td><p>Ondersteund</p></td>
  </tr>
  <tr>
   <td><p>Horizontale positie</p></td>
   <td><p>Ondersteund</p><p>Voor Excel 2010 en 2013 werkt het horizontaal plaatsen van watermerken met punten niet.</p></td>
  </tr>
  <tr>
   <td><p>Schalen</p></td>
   <td><p>Ondersteund</p></td>
  </tr>
  <tr>
   <td><p>Positie</p></td>
   <td><p>Ondersteund</p></td>
  </tr>
  <tr>
   <td><p>Dekking</p></td>
   <td><p>Ondersteund</p></td>
  </tr>
 </tbody>
</table>

### Webpagina&#39;s voor documentbeveiliging openen {#opening-the-document-security-web-pages}

U kunt de Web-pagina&#39;s van de Veiligheid van het Document openen om uw gebruikersbeleid tot stand te brengen en bij te werken en status en controleinformatie over uw beleid-beschermde dossiers te bekijken. U kunt de Web-pagina&#39;s van de Veiligheid van het Document ook gebruiken om beleid te veranderen of toegang voor een beleid-beschermd dossier in te trekken.

Om de Web-pagina&#39;s van de Veiligheid van het Document, in de Uitbreiding van de Veiligheid van het Document voor Microsoft® Office 2010 en 2013, op het **lusje van de Veiligheid van het 0} Document te openen,** creeer en beheer Beleid **.** Als u nog geen aanmeldingsgegevens hebt opgegeven, wordt de browser geopend op de aanmeldingspagina van de server.

### Beleid wijzigen {#changing-policies}

Als u machtigingen hebt, meestal als documentbeveiligingsbeheerder of de uitgever van het bestand, kunt u later een ander beleid toepassen op een bestand of de instellingen wijzigen van het beleid dat momenteel wordt toegepast.

Als u de instellingen voor een beleid wilt wijzigen, gebruikt u de webpagina&#39;s voor documentbeveiliging.

1. Ga als volgt te werk:

   * In de Uitbreiding van de Veiligheid van het Document voor Microsoft® Office 2010 of 2013, op het **lusje van de Veiligheid van het 0} Document, uitgezochte** Veilig > Veiligheid van de Verandering **.**

1. Selecteer een beleid van de lijst en klik **toepassen**.

### Toegangsrechten voor bestanden intrekken {#revoking-file-access-privileges}

U kunt de mogelijkheid intrekken om bestanden te openen die u hebt beveiligd. Wanneer u de bestandstoegang intrekt, kunt u een bericht opgeven wanneer gebruikers proberen het te openen en een URL naar een bijgewerkte versie opgeven als ze het vervangen door een gereviseerde kopie.

1. Ga als volgt te werk:

   * In de Uitbreiding van de Veiligheid van het Document voor Microsoft® Office 2010 en 2013, op het **lusje van de Veiligheid van het 0} Document, uitgezochte** trekt **terug.**

   De webpagina&#39;s voor documentbeveiliging worden geopend op de pagina Documenten intrekken.

1. Specificeer een bericht aan vertoning en, indien beschikbaar, een URL voor de bijgewerkte versie, en klik **O.K.**.

Voor meer informatie over het intrekken van de voorrechten van de dossiertoegang, zie [ Eind - de Hulp van de Gebruiker van de Veiligheid van het Document ](https://help.adobe.com/en_US/AEMForms/6.1/RMHelp/).

Toegangsrechten kunnen opnieuw worden ingesteld via de webpagina&#39;s voor documentbeveiliging.

### De auditgeschiedenis van het bestand weergeven {#viewing-the-file-audit-history}

Met Documentbeveiliging kunt u de auditgeschiedenis opslaan voor bestanden die met een beleid zijn beveiligd, zodat u de handelingen kunt controleren die gebruikers op uw bestanden uitvoeren.

De gecontroleerde gebeurtenissen voor Word, Excel, en de dossiers van PowerPoint omvatten het volgende:

**beveilig een Nieuw Document** Beleid dat op een dossier wordt toegepast

**Open Dossier van het Document van de Mening**

**dicht Gesloten Document** Dossier

**trekt de voorrechten van de Toegang van het Document** die voor dossier worden verwijderd

**trekt de voorrechten van de Toegang van het Document** terug die aan dossier zijn teruggekeerd

**wijzig het Dossier van het Document** veranderde en plaatselijk bewaarde

**Van de hoge Resolutie van de druk 1} Druk Afgedrukt Dossier**

**de bescherming van het Beleid van de Beveiliging van de Verandering die van dossier wordt verwijderd**

**Beleid van de Schakelaar op Document** Nieuw beleid dat op dossier van de Web-pagina&#39;s van de Veiligheid van het Document wordt toegepast

### De auditgeschiedenis van een bestand weergeven {#view-the-audit-history-for-a-file}

In de Uitbreiding van de Veiligheid van het Document voor Microsoft® Office 2010 en 2013, op het **lusje van de Veiligheid van het 0} Document, uitgezochte** Geschiedenis van de Controle **.**

De Web-pagina&#39;s van de Veiligheid van het Document openen aan de pagina van Gebeurtenissen, die gecontroleerde gebeurtenissen voor het huidige dossier toont.

### Beperkte functies in Microsoft® Office {#microsoft-office-restricted-features}

Om uw intellectuele eigendom te beschermen, zijn sommige functies van Microsoft® Office niet beschikbaar wanneer een bestand met beleidsbescherming is geopend. De lijst met niet-beschikbare functies is afhankelijk van de machtigingen die aan de huidige gebruiker zijn verleend. Sommige functies zijn alleen niet beschikbaar voor een beveiligd bestand en andere zijn niet beschikbaar voor alle bestanden wanneer u zich in een beveiligde sessie bevindt. Over het algemeen bevindt u zich in een beveiligde sessie vanaf het moment dat u een met een beleid beveiligd bestand opent tot u de toepassing sluit of de sessie verloopt.

De meeste beleidsregels verlenen volledige machtigingen aan de uitgever van het bestand. Andere gebruikers kunnen extra functiebeperkingen opmerken.

Als een opdracht niet beschikbaar is, worden de opdrachtnaam in het menu en de bijbehorende werkbalkknop grijs weergegeven.

>[!NOTE]
>
>Als u een beleid toepast op een bestand dat een koppeling naar een ingesloten bestand bevat, wordt het beleid niet toegepast op het gekoppelde bestand. Documentbeveiliging voor Microsoft® Office breidt de beveiliging niet uit tot gekoppelde bestanden.

* Word-, Excel- en PowerPoint-bestanden die met een beleid zijn beveiligd, kunnen niet worden geopend in een browservenster van Internet Explorer.
* Gebruikers die alleen de machtiging Wijzigen hebben gekregen, kunnen geen inhoud kopiëren naar een bestand vanuit een andere toepassing met behulp van het Windows-klembord. Gebruikers kunnen inhoud naar bestanden kopiëren door de optie Microsoft® Office Clipboard in te schakelen.
* Als u een bestand opent dat met een beleid is beveiligd in Microsoft® Office, is de toets Print Screen niet beschikbaar totdat u de toepassing sluit of de sessie verloopt.
* Documentbeveiliging voor Microsoft® Office ondersteunt WebDAV (Web-based Distributed Authoring and Versioning) niet. Gewoonlijk kunt u geen met beleid beveiligd bestand openen vanuit een WebDAV-map. Als u een bestand kunt openen dat met een beleid is beveiligd, hebt u geen machtigingen om het bestand op te slaan, af te drukken, te wijzigen of te kopiëren.

De algemene veiligheid die op beleid-beschermde dossiers van toepassing is omvat de volgende beperkingen:

Veel veelvoorkomende functies kunnen tijdens een beveiligde sessie worden beperkt in Word, Excel en PowerPoint.

Als een bestand dat met beleid is beveiligd en dat de gebruiker niet toestaat wijzigingen aan te brengen, is geopend, zijn opdrachten die het bestand op een of andere manier wijzigen, niet beschikbaar. Alleen de opdrachten waarmee u documenten opent of maakt en de voorkeuren van de toepassing wijzigt, zijn beschikbaar.

#### Beperkingen in Word 2010 en Word 2013 {#word-2010-and-word-2013-restrictions}

Als u een bestand opent dat met een beleid is beveiligd in Word, kunt u de gegevens voor automatisch herstel pas opslaan nadat u Word hebt gesloten en opnieuw hebt gestart. Bovendien zijn de hieronder vermelde kenmerken beperkt in de beschreven situaties:

**Dossier > Nieuw > Nieuw van Bestaand** Beschikbaar maar de dossiers die gebruikend dit bevel worden gecreeerd terwijl om het even welk beleid-beschermd dossier open is kunnen niet worden bewaard. Inhoud in het nieuwe bestand kan niet naar een ander bestand worden gekopieerd.

**Dossier > sparen** Beperkt door de toestemming van de Verandering.

**Dossier > sparen als** Alle opties die door de toestemming van de Verandering worden beperkt.

**Dossier > Druk** Alle opties die door de toestemming van de Druk worden beperkt. Niet beschikbaar, tenzij het beleid afdrukken met hoge resolutie toestaat.

**Dossier > sparen &amp; verzend** Alle opties niet beschikbaar tijdens een beschermde zitting.

**Dossier > Info > het Document van Protect > Codeert met Wachtwoord, voegt Digitale Handtekening, Teken als Definitief, Beperk Toestemming door Mensen** niet beschikbaar tijdens een beschermde zitting.

**Dossier > de Werkschema&#39;s** niet beschikbaar tijdens een beschermde zitting.

***Nota **: Beginnend een werkschema in Word, Excel, en PowerPoint 2010 is slechts beschikbaar in de Beroeps van het Bureau plus 2010, de Onderneming 2010 van het Bureau, het Bureau Ultimate 2010, en stand-alone versies van 2010.*

**Blogpost > Publish** niet beschikbaar tijdens een beschermde zitting.

**Dossier > de Server > Menu van de Taken van de Server van het Dossier** niet beschikbaar tijdens een beschermde zitting.

**Huis > Klembord > Exemplaar** Beperkt door de toestemming van het Exemplaar. Als kopiëren niet is toegestaan, kan de gekopieerde inhoud niet in een ander dossier of aan het Klembord van het Bureau worden gekleefd. Inhoud kan binnen het beveiligde bestand worden gekopieerd als de gebruiker over wijzigingsmachtigingen beschikt.

**Huis > Klembord > Deeg** Beperkt door de toestemming van de Verandering.

**Huis > Klembord > Deeg Speciaal** Beperkt door de toestemming van de Verandering.

**Tussenvoegsel > Tekst > Voorwerp** niet beschikbaar tijdens een beschermde zitting. Met een beleid beveiligde bestanden kunnen op geen enkel moment worden ingevoegd.

**de Meeste opties op dit lusje van Maken 0} {zijn niet beschikbaar tijdens een beschermde zitting.**

**Overzicht > het Bewijzen > Onderzoek** Beperkt door de toestemming van het Exemplaar. Niet beschikbaar als kopiëren niet is toegestaan.

**Overzicht > het Bewijzen > Synoniemenlijst** Beperkt door de toestemming van het Exemplaar. Niet beschikbaar als kopiëren niet is toegestaan.

**Overzicht > Taal > Vertaal > Vertaal Document** Toegelaten met de toestemming van het Exemplaar.

**Overzicht > Taal > Vertaal > Vertaal Geselecteerde Tekst** Toegelaten met de toestemming van het Exemplaar.

**Overzicht > Taal > Vertaal > Mini Vertaler** Toegelaten met de toestemming van het Exemplaar.

**Overzicht > vergelijkt >** niet beschikbaar tijdens een beschermde zitting. Met een beleid beveiligde bestanden kunnen op geen enkel moment worden vergeleken.

**Overzicht > Protect > de Auteurs van het Blok** niet beschikbaar tijdens een beschermde zitting.

**Overzicht > Protect > Beperkt het Uitgeven** niet beschikbaar tijdens een beschermde zitting.

**Mening > Macro&#39;s** de toestemming van het Exemplaar beperkt sommige macro&#39;s, die hen onbeschikbaar maken tenzij het kopiëren wordt toegestaan.

**toe:voegen-ins** kan niet tijdens een beschermde zitting worden toegevoegd of worden verwijderd.

**Online Collaboration** niet beschikbaar tijdens een beschermde zitting.

**Primair en subdocuments** Primair documentenbeleid regeert subdocuments wanneer u hen binnen het primaire document opent. Als subdocumenten afzonderlijk worden geopend, kunnen deze niet worden afgedrukt, gekopieerd of gewijzigd.

**hervat** niet beschikbaar tijdens een beschermde zitting.

**Kaders (en alle verwante bevelen)** niet beschikbaar tijdens een beschermde zitting.

**het Comité van het Document** niet beschikbaar tijdens een beschermde zitting.

**Ontwikkelaar > het Malplaatje van het Document** niet beschikbaar tijdens een beschermde zitting. Selecteer Bestand > Opties > Aanpassen > Tabblad Ontwikkelaar > Sjablonen > Documentsjabloon om deze opdracht te openen.

**het Schetsen > Primair Document > leidt tot Subdocument, Subdocument van het Tussenvoegsel** niet beschikbaar tijdens een beschermde zitting.

#### Beperkingen in Excel 2010 en Excel 2013 {#excel-2010-and-excel-2013-restrictions}

De onderstaande functies zijn beperkt in de beschreven situaties:

**Dossier > Nieuw > Nieuw van Bestaand** Beschikbaar, maar de dossiers die gebruikend dit bevel tijdens een beschermde zitting worden gecreeerd kunnen niet worden bewaard. Inhoud in het nieuwe bestand kan niet naar een ander bestand worden gekopieerd.

**Dossier > sparen, sparen als** Beperkt door de toestemming van de Verandering.

**Dossier > sparen als > PDF** niet beschikbaar tijdens een beschermde zitting.

**Dossier > Druk** Beperkt door de toestemming van de Druk. Niet beschikbaar, tenzij het beleid afdrukken met hoge resolutie toestaat.

**Dossier > Info > het Document van Protect** niet beschikbaar tijdens een beschermde zitting.

**Dossier > Info > het Werkboek van Protect** niet beschikbaar tijdens een beschermde zitting.

**Dossier > sparen &amp; verzend** niet beschikbaar tijdens een beschermde zitting.

**Dossier > Opties > toe:voegen-ins** kan niet tijdens een beschermde zitting worden toegevoegd of worden verwijderd.

**Dossier > de Werkschema&#39;s** niet beschikbaar tijdens een beschermde zitting.

***Nota **: Beginnend een werkschema in Word, Excel, en PowerPoint 2010 is slechts beschikbaar in de Beroeps van het Bureau plus 2010, de Onderneming 2010 van het Bureau, het Bureau Ultimate 2010, en stand-alone versies van 2010.*

**Dossier > de Server > Menu van de Taken van de Server van het Dossier** niet beschikbaar tijdens een beschermde zitting.

**Huis > Klembord > Exemplaar** Beperkt door de toestemming van het Exemplaar. Als kopiëren niet is toegestaan, kan gekopieerde inhoud niet in een ander bestand of op het Microsoft® Office-klembord worden geplakt. Inhoud kan binnen het beveiligde bestand worden gekopieerd als de gebruiker over wijzigingsmachtigingen beschikt.

**Huis > Klembord > Deeg** Beperkt door de toestemming van de Verandering.

**Huis > Klembord > Deeg Speciaal** Beperkt door de toestemming van de Verandering.

**Huis > Cellen > Formaat > Beweging of het Blad van het Exemplaar** niet beschikbaar tijdens een beschermde zitting.

**Huis > Cellen > Tussenvoegsel > het Blad van het Tussenvoegsel** niet beschikbaar tijdens een beschermde zitting.

**Huis > Cellen > Schrapping > Schrappblad** niet beschikbaar tijdens een beschermde zitting.

**Huis > het Uitgeven > Vulling > over Werkblad** Beperkt door de toestemming van de Verandering.

**Tussenvoegsel > Lijsten > Lijst** Beperkt door de toestemming van de Verandering.

**het Tussenvoegsel > Lijsten >** beleid-beschermde dossiers draaitafel kan niet in de Tovenaar van de Aanmaak worden geselecteerd.

**Tussenvoegsel > Tekst > Voorwerp** niet beschikbaar tijdens een beschermde zitting. Met een beleid beveiligde bestanden kunnen op geen enkel moment worden ingevoegd.

**Tussenvoegsel > Tekst > Kopbal en Voettekst** Beperkt door de toestemming van de Verandering. Niet beschikbaar voor een document dat met een beleid is beveiligd.

**Gegevens > krijgen Externe Gegevens** De gegevens van beleid-beschermde dossiers kunnen niet worden ingevoerd.

**Gegevens > Overzicht > Subtotals** Beperkt door de toestemming van de Verandering.

**Gegevens > Hulpmiddelen van Gegevens > Bevestiging van Gegevens** die door de toestemming van de Verandering wordt beperkt.

**Overzicht > het Bewijzen > Onderzoek** Beperkt door de toestemming van het Exemplaar.

**Overzicht > het Bewijzen > Synoniemenlijst** Beperkt door de toestemming van het Exemplaar.

**Overzicht > Taal > Vertaal** Beperkt door de toestemming van het Exemplaar.

**Overzicht > Veranderingen > het Blad van Protect** niet beschikbaar tijdens een beschermde zitting.

**Overzicht > Veranderingen > het Werkboek van Protect** niet beschikbaar tijdens een beschermde zitting.

**Overzicht > Veranderingen > de Werkboek van het Aandeel** niet beschikbaar tijdens een beschermde zitting.

**Overzicht > Veranderingen > Protect en het Werkboek van het Aandeel** niet beschikbaar tijdens een beschermde zitting.

**Overzicht > Veranderingen > Toestaan Gebruikers om Wegen** uit te geven niet beschikbaar tijdens een beschermde zitting.

**Overzicht > Veranderingen > de Veranderingen van het Spoor > Veranderingen van het Hoogtepunt** niet beschikbaar voor een beleid-beschermd dossier dat een dynamisch watermerk bevat.

**Mening > Macro&#39;s** die door de toestemming van de Verandering wordt beperkt.

**Mening > sparen Workspace** Bevel werkt niet.

**Ontwikkelaar > XML > de Pakken van de Uitbreiding** de toestemming van het Exemplaar beperkt sommige macro&#39;s, die hen maken niet beschikbaar tenzij u het kopiëren toestaat.

**Formulas > de Controle van de Formule > het Controleren van de Fout** die door de toestemming van de Verandering wordt beperkt. Niet beschikbaar, tenzij wijzigen is toegestaan.

**Online Collaboration** niet beschikbaar tijdens een beschermde zitting.

**sparen AutoHerstelt Info** niet beschikbaar tijdens een beschermde zitting.

***Nota **: Als u probeert om een cel in een beleid-beschermd dossier zonder toestemming te veranderen, waarschuwt Excel verkeerd u om het Unprotect bevel van het Blad te gebruiken om de bescherming te verwijderen.*

#### Beperkingen van PowerPoint 2010 en PowerPoint 2013 {#powerpoint-2010-and-powerpoint-2013-restrictions}

De onderstaande functies zijn beperkt in de beschreven situaties:

**Dossier > Nieuw > Nieuw van Bestaand** Beschikbaar, maar de dossiers die gebruikend dit bevel tijdens een beschermde zitting worden gecreeerd kunnen niet worden bewaard. Inhoud in het nieuwe bestand kan niet naar een ander bestand worden gekopieerd.

**Dossier > sparen** Beperkt door de toestemming van de Verandering.

**Dossier > sparen als** Alle opties die door de toestemming van de Verandering worden beperkt.

**Dossier > Druk** Alle opties die door de toestemming van de Druk worden beperkt. Niet beschikbaar, tenzij het beleid afdrukken met hoge resolutie toestaat.

**Dossier > sparen &amp; verzend** niet beschikbaar tijdens een beschermde zitting.

**Dossier > Info > de Presentatie van Protect > codeert met Wachtwoord, voegt een Digitale Handtekening, Teken als Definitief, Beperk Toestemming door Mensen** niet beschikbaar tijdens een beschermde zitting.

**Dossier > de Opties van PowerPoint > sparen AutoHerstelInfo** niet beschikbaar tijdens een beschermde zitting.

**Dossier > de Server > Menu van de Taken van de Server van het Dossier** niet beschikbaar tijdens een beschermde zitting.

**Huis > Klembord > Exemplaar** Beperkt door de toestemming van het Exemplaar. Als kopiëren niet is toegestaan, kan gekopieerde inhoud niet worden geplakt in het document, in een ander bestand of op het Office-klembord. Inhoud kan binnen het beveiligde bestand worden gekopieerd als de gebruiker over wijzigingsmachtigingen beschikt.

**Huis > Klembord > Deeg** Beperkt door de toestemming van de Verandering. Als kopiëren niet is toegestaan, kan gekopieerde inhoud niet in het document worden geplakt.

**Huis > Klembord > Deeg Speciaal** Beperkt door de toestemming van de Verandering.

**Huis > Dia&#39;s > Nieuwe Dia&#39;s > Dia&#39;s van Overzicht, hergebruik Dia&#39;s** niet beschikbaar tijdens een beschermde zitting.

**Tussenvoegsel > Tekst > Voorwerp** niet beschikbaar tijdens een beschermde zitting. Met een beleid beveiligde bestanden kunnen op geen enkel moment worden ingevoegd.

**Ontwerp > Achtergrond > de Stijlen van de Achtergrond, de Grafiek van de Achtergrond van de Huid, Achtergrond van het Formaat** niet beschikbaar voor een beleid-beschermd dossier dat een dynamisch watermerk bevat.

**de Show van de Dia > Opstelling > de Show van de Dia van het Verslag** Beperkt door veranderingstoestemming.

**Overzicht > het Bewijzen > Synoniemenlijst** Beperkt door de toestemming van het Exemplaar.

**Overzicht > Taal > Vertaal** Beperkt door de toestemming van het Exemplaar.

**Overzicht > Taal > Vertaal > Mini Vertaler** Toegelaten met de toestemming van het Exemplaar.

**Mening > de Mening van de Presentatie > de Show van de Dia** die door de toestemming van de Verandering wordt beperkt. Als wijzigingen niet zijn toegestaan, kunnen presentaties niet worden weergegeven als het bestand is gewijzigd.

**Mening > Macro&#39;s** de toestemming van het Exemplaar beperkt sommige macro&#39;s, die hen onbeschikbaar maken tenzij het kopiëren wordt toegestaan.

**toe:voegen-ins** kan niet tijdens een beschermde zitting worden toegevoegd of worden verwijderd.

**Online Collaboration** niet beschikbaar tijdens een beschermde zitting.

## Andere verificatieproviders gebruiken {#use-third-party-authentication-providers}

U kunt externe verificatieproviders gebruiken met AEM Forms Document Security. Met deze verificatieproviders kunt u een extra toegangslaag toevoegen aan de beveiligde documenten. AEM Forms Document Security ondersteunt de volgende uitgebreide verificatieworkflows:

* Uitgebreide verificatie met de standaard AEM Forms URL
* Uitgebreide verificatie met een aangepaste URL
* Standaard uitgebreide verificatieworkflow met externe identiteitsproviders geconfigureerd op AEM Forms op JEE-server
* Aangepaste uitgebreide verificatieworkflow met externe identiteitsproviders geconfigureerd op AEM Forms op JEE-server
* Uitgebreide verificatie met behulp van een aangepaste pagina voor SAML-verificaties

## Verklarende woordenlijst {#glossary}

Voor informatie over LiveCycle en AEM vormen op de terminologie van JEE, zie [ Hoofdstuk 19: Verklarende woordenlijst ](https://helpx.adobe.com/content/dam/help/en/experience-manager/6-5/forms/pdf/using-designer.pdf).
