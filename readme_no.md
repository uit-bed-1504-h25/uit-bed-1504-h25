
{% include navbar.html %}{% include top-box.html %}
<br><br><br>
<div align="right">
	<a href="readme_en.html"><img src="https://uit-econ.github.io/images/Norway.png"></a>
</div>


										   
# Hvordan lage en kursside
Om du trenger en innføring i git, [finner du en her (inkluderer innføring i python)](https://espensirnes.github.io/notebooks/html/0%20-%20installasjon%20og%20tips.html)

## 1. Lage en organisasjon

Det første vi må gjøre er å lage en "organisasjon", som skal eie kurssiden. Du kan gjøre dette som følger:

1. Logg in på github.com
2. Gå til [https://github.com/organizations/plan](https://github.com/organizations/plan){:target="blank" rel="noopener"}
3. Velg "Create organization"
4. Velg "Create a free organization" <br><br> ![image](https://uit-econ.github.io/images/createfreeorg.png)<br><br>
5. Bruk følgende oppsett:
	1. Gi navn etter følgende navnekonvensjon<br><br> 
	`uit-<kurskode>-<semester><år>`.<br><br>`<kurskode>` kan for eksempel være SOK-1006.<br>`<semester>` kan være enten "h" or "v" (Norsk) or "f" or "s" (Engelsk).<br>Bruk de siste to sifferne i `<year>`.<br><br>
	For eksempel kan navnet være `uit-sok-1006-v23`.<br><br>
	3. Skriv in e-posten din
	4. Velg "A business or institution"
	5. Skriv inn "UiT The Arctic University of Norway" som navn på institusjonen.<br><br>
	6. Aksepter betingelesene og klikk "Next"<br><br> ![image](https://uit-econ.github.io/images/setup.png)<br><br>
6. Legg til kollegger som er med på kurset og klikk "Complete setup"<br><br> ![image](https://uit-econ.github.io/images/addcolleagues.png)
7. Om nødvendig, skriv inn githubpassordet <br><br> ![image](https://uit-econ.github.io/images/password.png)
8. Klikk på brukerikonet i øverste høyre hjørne, og klikk på "Your organizations"<br><br> ![image](https://uit-econ.github.io/images/selectorganizations.png)<br><br>
9. Klikk på organisasjonen du akkurat har skapt<br><br>
		
## 2. Lage kursets repositorie (repo)

1. Gå til dette repositoriet: [https://github.com/uit-econ/coursepage_template](https://github.com/uit-econ/coursepage_template){:target="blank"}
2. Klikk på "Use this template" og "Create new repository" ![image](https://uit-econ.github.io/images/createnewrepo.png)
4. **VIKTIG!** Endre "Owner" til organisasjonen du akkurat har skapt.<br> ![image](https://uit-econ.github.io/images/reposettings.png)
3. Gi repoen akkurat samme navn som organisasjonen, men legg til ".github.io" på slutten av navnet.<br>
	For eksempel, om organisasjonsnavnet var "uit-sok-1006-v23", blir reponavnet "uit-sok-1006-v23.github.io".<br>
	Hensikten med denne navngivingen er at denne repoen automatisk skal bli startsiden til organisasjonen.  
4. Velg "Public" og klikk "Create repository" 
		
## 3. Åpne og se repoens hjemmeside
1. Finn "github-pages" nede til høyre i repositoriet og klikk på den.<br><br>
	![image](https://uit-econ.github.io/images/githubpages.png)<br><br>
3. Klikk på "View deployment" på siden du kommer til, og du vil se hjemmesiden til kurset (det kan ta noen minutter før det er ferdig, så du må kanskje oppdatere nettleseren noen ganger)
4. Om du ikke kan se "github-pages"-lenken, selv etter å ha ventet noen minutter, kan du aktivere nettsiden i "Settings" i repomenyen. Velg "Pages" i venstremenyen og "main" i nedtrekksmenyen "Branch". Klikk så på "Save".<br><br>
			
## 4. Rediger repoen
1. Rediger repoinnstillingene i "\_config.yml" ved å trykke på filen og så pennikonet oppe mot høyre. <br><br>Du trenger kun redigere de tre første linjene (om du ikke vil endre avanserte innstillinger). De første tre linjene er:

	* **name: Sok-xxxx Emnetittel**: <br>
	Nødvendig. Må endres til gjeldende kurskode.<br><br>
	* **semester: Høst/Vår 20xx**:<br>
	Nødvendig. Må endres til gjeldende semester.<br><br>
	* **image: tema.jpg**:<br>
	Valgfri. Du kan laste opp et nytt bilde med "Add file"-knappen. Om navet ikke er "tema.jpg", må du endre navnet over. Du kan imidlertid også bare slette "tema.jpg" og laste opp en ny fil med samme navn. ![image](https://uit-econ.github.io/images/editconfig0.png)<br><br>

2. Rediger venstremenyen til hjemmesiden ved å redigere "navbar.html". Begynn med å fjerne lenke til disse dokumentene ("Hvordan sette opp en kursside"). 
	Du kan redigere eksisterende lenker ved å endre på lenkeadressen og lenketeksten. Om du trenger flere lenker, så bare kopier én av lenkene og endre denne. <br><br>
	**MERK!** Markupfiler konverteres automatisk til html-filer. Om du ønsker å lenke til en markdown \*.md-fil, må du derfor endre filendelsen fra ".md" til ".html". <br><br> ![image](https://uit-econ.github.io/images/editnavigate.png)

3. Det er allerede maler for startsiden ("index.md"), forelesningsplan ("forelesningsplan.md"),
	seminarer ("seminarplan.md") and innleveringer ("innleveringer.md"). Du kan se av disse eksemplene hvordan du lager lenker og tabeller. <br><br>
	**VIKTIG!** Om du lager en ny markdownfil (.md), legg alltid inn **\{\% include navbar.html \%\}\{\% include top-box.html \%\}** i toppen av dokumentet. Dette sørger for at venstremenyen og topp-boksen lastes med siden.<br><br>


## 5. Redigere hovedsiden for *Samfunnsøkonomi med datavitenskap*
For å gjøre kurssiden tilgjengelig for studentene fra [hovedsiden](https://uit-econ.github.io/), må du redigere emnet der. 

1. Gå til  `\_portfolio`-mappen i `uit-econ.github.io`-repoen under hovedside-organisasjonen `uit-econ` her: [uit-econ/uit-econ.github.io/\_portfolio/](https://github.com/uit-econ/uit-econ.github.io/tree/main/_portfolio)<br><br>![image](https://uit-econ.github.io/images/editmainpage.png)<br><br>
2. Klikk på kurset du er ansvarlig for, og rediger det (klikk på penn-symbolet oppe til høyre).<br><br>![image](https://uit-econ.github.io/images/editmainpage2.png)<br><br>
3. Dokumentet du nettopp åpnet kan inneholde en kursbeskrivelse, eller ikke. Uansett, skal siden se slik ut nå:  <br>
	<div style="background-color:#f6f8fa;font-family:Courier; padding-left:160">
			<br>
			---<br>
			title: Sok-xxxx &lt;Navn på kurs&gt;     <br>
			subtitle: 10 STP  <br>
			image: https://raw.githubusercontent.com/uit-econ/hovedside/main/assets/img/Sok-xxxx.jpg   <br>
			category: semesterX   <br><br>
			caption:  <br>
			&emsp; title: Sok-xxxx  <br>
			&emsp; subtitle: &lt;Navn på kurs&gt;  <br>
			&emsp; thumbnail: https://raw.githubusercontent.com/uit-econ/hovedside/main/assets/img/Sok-xxxx.jpg  <br>
			---  <br>
			&#123;% include nettsideApnerTop.html %&#125;   <br>
			window.open('https://uit-sok-xxxx-&lt;semester&gt;&lt;år&gt;.github.io/');   <br><br>
			&#123;% include nettsideApnerMid.html %&#125;   <br>
			observer.observe(document.getElementById("Sok-xxxx").children[0], { attributes: true } );    <br><br>
			&#123;% include nettsideApnerBunn.html %&#125;   <br>
	</div>
	<br><br>
	* Om det lå en kursbeskrivelse, kan du eventuelt kopiere den og lime innholdet inn i "index.md" i kursets github repositorie. 
	* Dersom siden ikke ser ut som ovenfor, så 
		* sletter du all tekst som er der
		* limer inn teksten ovenfor
		* bytter sok-xxxx med kurskoden alle steder
		* bytter ut 'https://uit-sok-xxxx-&lt;semester&gt;&lt;år&gt;.github.io/' med lenken til kursets githubside. Vær obs på at github automatisk legger til kode når du limer inn lenken slik at den kan bli seende ut som `[https://uit-sok-1006-v23.github.io/](https://uit-sok-1006-v23.github.io/)'`. Du skal imidlertid kun lime inn selve adressen på formen  `https://uit-sok-1006-v23.github.io/`. Husk anførselstegn. 
		* bytter ut de to stedene det står &lt;Navn på kurs&gt; med navn på kurset
		* Bytt ut X i semesterX med semesteret som kurset skal gå
	
4. Når du lagrer (commit) vil du få opp spørsmål om å lage en "pull request", om du ikke har skriverettigheter. Trykk på knappen og be kollega med skriverettigheter om å akseptere din "pull request"

## 6. Bygg kurset inn i hjemmesiden på canvas
Slik bygger du kursets hjemmeside inn i Canvas:
1. Gå til [Canvas](https://uit.instructure.com/) og velg kurset som du er ansvarlig for <br><br>![image](https://uit-econ.github.io/images/canvasorig.png)<br><br>
2. Klikk "Rediger"-knappen oppe til høyre, og klikk så "< >" symbolet (rediger html) nede til høyre <br><br>![image](https://uit-econ.github.io/images/canvashtmledit.png)<br><br>
3. Slett alt html-innhold og lim inn<br><br>
	<div style="background-color:#f6f8fa;font-family:Courier; padding-left:80"><br>
		&lt;p&gt;&lt;iframe style="overflow: hidden;"<br>
		src="bytt ut med lenken til din kursside"<br>
		width="1500" height="3000"&gt;&lt;/iframe&gt;&lt;/p&gt;<br>
		<br>
	</div><br><br>![image](https://uit-econ.github.io/images/canvashtmlnew.png)<br><br>
4. Slett `bytt ut med lenken til din kursside` og lim istedet inn lenken til kurssiden<br><br>
			
		
	
**DU ER I MÅL!!!!**
		
