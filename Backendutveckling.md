# Teorihandboken - Backendutveckling (BE)
Studerande: Malin Bragazzi

## BE 1.1 PHP
Vad?
PHP betyder Hypertext Preprocessor och är ett skriptspråk som körs i backend, från server-sidan. Vid fullstack-projekt så körs det först, och sedan HTML/CSS och JavaScript. Med skriptspråk så menas det att PHP inte behöver kompileras innan körning, vilket gör det lätt att ändra. PHP är utformat för att skapa dynamiskt innehåll, det vill säga innehåll som kan ändras i realtid beroende på olika faktorer, bl a användarens input i tex formulär, användarens platstjänster, databas-data etc.
PHP har funnits sedan 1994 och har därmed en stor mängd dokumentation.
Hur?
För att använda PHP så behövs en öppningstagg och en stängningstagg <?php …  ?>. Det går att använda med andra språk (JavaScript och HTML) i samma fil. Då behöver filändelsen vara .php, men du kan lägga till script- och HTML-taggar och blanda språken, bara öppnings- och stängningstaggarna ligger korrekt.
Det finns 3 olika kommentar-taggar, det finns boolean för sant eller falskt, det finns integers för nummer som är heltal, floats för nummer som har decimaler, samt strings för fritext som skrivs inom citattecken (enkla eller dubbla). 
Det finns också flera operatorer som används för att förändra variabler eller räkna ut något, som t ex jämföre- och logiska operatorer. Och PHP innehåller även datatyper så som arrays, objects och callables.
PHP är alltså väldigt likt bl a C-språk.
Varför?
PHP har många olika bibliotek och dessutom många inbyggda funktioner för vanligt förekommande uppgifter inom programmering, t ex databasåtkomst, kryptering, filhantering. Det går också att köra på flera olika operativsystem.

## BE 1.2 OOP i PHP
Vad?
OOP står för objektorienterad programmering. Det betyder att man arbetar med objekt istället för procedurer. Vid större projekt så ger OOP i PHP en bra struktur, och vi slipper upprepa kod, då det fokuserar på att man ska kunna återanvända data.
Hur?
Ett objekt är en instans av en klass. En ”bil” kan vara ett objekt. Den har egenskaper så som (märke, färg, modell). Den har metoder så som (starta, bromsa, stanna).
En klass är en mall för hur ”bilen” skapas, och definerar egenskaperna och metoderna.
Egenskaperna kallas också för attirbut, och metoder kallas också för funktioner. Metoderna utför uppgifter beroende på vad man vill ha gjort (bromsa, stanna).
Det finns inkapsling, det innebär att man ”gömmer” egenskaper och metoder så de bara finns tillgängliga inom objektet i fråga.
Med arv så kan en klass ärva egenskaper från en annan klass. Polymorfism innebär att man kan sätta överklasser, och sedan ge  kommandon som gäller flera av de ”vanliga” klasserna. T ex så skulle ”fordon” kunna vara en överklass till bil.
Varför?
OOP är ett strukturerat sätt att koda. Man delar upp koden i klasser och objekt och det gör koden mer översiktlig och återanvändbar.
Genom att man kan använda sig av arv, inkapsling och polymorfism, så blir koden väldigt flexibel också.
Genom dess tydliga struktur så underlättar det arbete i team.

## BE 1.3 Säkerhet i PHP
Vad?
OWASP (open web application securuty project) är en organisation som arbetar för säkerhet inom mjukvara, och de har listat de 10 vanligaste sårbarheterna. Dessa är 
1 Injicering, där det skickas med kommandon i SQL-queries som skadar programmet.
2 Bruten autentisering, där man skadar autentiseringen och användaruppgifter läcker.
3 Känslig data, när APIer inte skyddar känslig data som t ex användaruppgifter.
4 XXE, en tolknigsmotor för XML inte har tillräcklig säkerhetskontroll. Då kan angripare kunna läsa filer på interna servern eller köra skadlig kod på den.
5 Bruten auktorisering, där en vanlig användare kan råka få tillgång till andra användares uppgifter, eller admin rättigheter. 
6 Felaktig säkerhetskonfiguration, så ett system (exempelvis) inte har korrekt konfiguration för sitt användningsområde.
7 Cross-site scripting, när ett program inte validerar datan den tar in, så angripare kan köra script i programmet, och t ex dirigera om användare till skadliga webbplatser, som kanske till och med ser likadana ut som den webbplatsen dom försöker efterlikna.
8 Osäker deserialisering, det vill säga processen att konvertera tillbaks serialiserade data till sina ursprungliga objekt. Då kan angripare infoga skadlig kod i programmet.
9 Användade av komponenter med kända säkerhetsbrister.
10 Otillräcklig loggning och övervakning. I snitt tar det 200 dagar att upptäcka ett intrång.
Hur?
Uppdatera PHP löpande. Man kan använda hash även i databasfälten i databasen, så användaruppgifter krypteras. Man kan använda Salt, som är en slumpmässig string som läggs till lösenordet och sedan hashas allt tillsammans. Så även om angriparna skulle kunna lista ut lösenord med Rainbow-table så blir det alldeles för långt för att kunna lista ut det med Salt.
Man kan kräva att lösenord ska vara utformade på vissa sätt.
Varför?
Genom att vara medveten om sårbarheter i våra program, så kan vi minska risken för att de ska bli hackade.

## BE 1.4 MVC
Vad?
MVC står för Model View Controller. Det är ett sätt att strukturera mjukvara.
Model står för appens data och logik. Den kommunicerar med databaser eller liknande för att hämta och lagra information. Den innehåller också beräkningar som är specifika för appen. Modellen kan ha metoder för att hämta data och uppdatera den.
View presenterar data för användaren. Den tar emot data av modellen och formaterar om den till t ex HTML, JSON eller liknande. View kan innehålla mallar (templates) av dessa språk som den presenterar med. Vid interaktion med användare så skickar view tillbaka data till controllern.
Controllern hanterar interaktion med användaren. Den tar emot förfrågningarna som den får från view och vidtar åtgärder för att svara på dom.
Controllern bestämmer vilken model som ska hämta/uppdatera data. 
Hur?
Ett ramverk som använder detta är Laravel. Där är ett tydligt exempel på hur MVC hänger ihop med routes. Routern skickar förfrågan till den lämpligaste controllern.
Varför?
Återigen blir koden mer återanvändningsbar om man bryter ner den i mindre moduler och importerar dit man vill använda den. Det underlättar testning och underhåll på sikt.
Det negativa är att det är ganska komplext och kräver mer omfattande konfiguration för att fungera korrekt. Det behövs tid för att lära sig hur det används på bästa sätt. Så det beror egentligen på projektets storlek, vilken arkitektur som blir bäst.

## BE 1.5 Wordpress
Vad?
Wordpress är ett CMS (content management system) och står faktiskt för 43% av alla sidor på nätet.
Hur?
Wordpress är open source-kod som bygger på PHP och databasen som används är MySQL. Det är enkel installation och det är lätt för nybörjare att komma igång med sina webbplatser via Wordpress. Temat man väljer styr design och layout, men man kan välja tillägg för att få använda t ex sökmotoroptimering, integration med sociala medier osv. Då det från början var avsett att användas för att blogga, så är det lätt att organisera inlägg i kategorier och taggar. I dagsläget kan man dock bygga nästan vad som helst, inklusive forum, butiker, bildgallerier osv.
I Wordpress kan både kodare och icke-kodare arbeta tillsammans, då kodare kan stå för funktionaliteten och icke-kodare kan lägga till poster, sidor och liknande.
Varför?
Wordpress är populärt för att det har utvecklats under 20 års tid, och har därmed tusentals teman att välja med mellan. Det är open source-kod så man kan modifiera sin sida själv väldigt enkelt. Det är relativt säkert och fungerar bra tillsammans med sökmotorer. Då det har ca 13 miljoner nedladdningar så finns det stor dokumentation, såsom forum, videos etc för användandet av wordpress,
Om man ska påvisa några svagheter med Wordpress så är det att det är ett attraktivt mål för hackare, eftersom det är så utbrett.
Man är beroende av tredjepartsleverantörer för vissa funktioner och tillägg, och det kan vara en osäkerhet om man vill det.
Och för större webbplatser så kan prestandan minska om den har många besökare.

## BE 1.6 Heirarkiska databaser
Vad?
Hierarkiska databaser organiserar data i hierarkisk struktur, som det hörs på namnet. Det är en så kallad trädstruktur där objekten/posterna kallas noder. Noderna kan ha flera barnnoder men bara en föräldernod. De kan vara bra att använda i specialiserade situationer som t ex Windows Registry, telekommunikationssystem samt vissa banktillämpningar.
Hur?
Om man ska hämta data från en specifik plats i hierarkin, så är det väldigt lätt att använda sig av hierarkiska databaser då, eftersom man vet vart datan finns, då det är en tydlig under- och överordnad relation sinsemellan noderna. Det är en enkel och intuitiv struktur som gör det lätt att förstå och hantera.
Dessa databaser är dock väldigt oflexibla, så om datan är mer komplex och inte passar in i den hierarkiska strukturen så blir det svårt att representera den på ett bra sätt.
Vid ändringar då man t ex behöver ta bort en nod så krävs det även ibland att vissa barnnoder uppdateras, och det kan vara krångligt och riskfyllt om det inte görs på ett beräknat sätt. Att söka fritext i hierarkiska databaser eller generera rapporter kan vara svårt om det involverar flera noder eller relationer. 
Varför?
Databasen har snabb access till noder, dvs, kan snabbt ta bort eller lägga till en post. Dock är fri sökning väldigt långsam i hierarkiska databaser, och språken som finns är inte lika smidiga som SQL.
Denna typ av databaser skapades på 60-talet och har mer och mer fasats ut och ersatts av andra sorters databaser, som relationsdatabaser och nätversdatabaser.

## BE 1.7 Relationsdatabaser, SQL och ER-modellering
Hur? Vad? Varför?
Relationsdatabaser använder tabeller för att lagra data. De ska ha ett schema där det beskrivs vad det är för data som finns däri. De ska inte upprepa data, samt de ska vara konsistenta, dvs inte innehålla motsägelser.
Strukturen som används för databasmodellen är vad datan i tabellerna har för inbördes relation till varandra Man kopplar ihop kolumnvärdena och och kallar dessa sammanhörande kolumner för nycklar. Primärnycklar används i en databas, och främmande nycklar är för att koppla ihop mot en annan databas primärnycklar.
ER står för entity relationship och den metoden används för att påvisa strukturerna i en databas med hjälp av entitet och relation. I ett ER-diagram är entiterna är objekten och relationerna visas genom pilar eller linjer mellan entitetna. Det finns också olika sambandstyper, så kallade kardinalitetsförhållanden. Se bild nedan för fullständigt diagram.

![Alternativ text](/ER.png)

Med hjälp av ett ER-diagrammet får man en grundläggande plan för hur objekten relaterar till varandra och kan konvertera det till ett programmatiskt schema. 
SQL står för Structured Query Language och är ett språk som används inom hanteringen av relationsdatabaser. Det är erkänt som det främsta språket för sitt syfte. Men hjälp av SQL-kommandon kan man bl a skapa och ändra tabeller, infoga, uppdatera data, samt söka efter information.
Delen i SQL som heter DDL (data definition language) handlar om hur man lagrar sin data. Där finns kommandon som Create, Alter, Drop. Delen som heter DML (data modelling language) handlar om manipuleringen, dvs kommandon som Select, Insert, Update, Merge. Såhär ser språket ut:

![Alternativ text](/SQL.png)


## BE 1.8 OAuth i backend
Vad?
OAuth står för Open Authorization och är en öppen säkerhetsprotokollstandard som används för att hantera autentisering mellan klienter och server. Det används för att låta användare få åtkomst till sina egna data inom appen genom en tredjepartstjänst så man inte delar sina inloggningsuppgifter direkt till appen i fråga. Till exempel är facebook eller google stora leverantörer inom denna tjänst. Det är ofta man stöter på ”logga in med google” eller ”fortsätt som facebook-användare” på andra webbsidor.
Hur?
Inom detta finns olika roller. Vi har Resource owner som är användaren. Denne ger godkänt att en applikation kan få tillgång till deras konto/info, dock bara scope, dvs läsa och skriva, inte få lösenord etc.
Det finns Resource och Authorization server (som också är APIet), resursservern som skyddar användarkontona, verifierar dom samt förser appen med access tokens.
Client är appen som vill komma åt användarens konto. Detta görs enbart om användaren auktoriserat detta och om APIet har validerat. 
Varför?
Genom att OAuth  gör det möjligt med säker autentisering så minskar risken med att lösenord avslöjas. Användaren kan också välja vad denne vill dela med sig av till appen, genom att begränsa behörigheten. Det ger en bättre användarupplevelse att slippa behöva skapa nya konton och hålla reda på användarnamn och lösenord för ytterligare en tjänst.  Det minskar tiden det tar att komma igång med nya tjänsten.
Det finns även några nackdelar. T ex så är applikationen ifråga beroende av en autentiseringsserver som inte är ens egen. Om den har problem så påverkar det applikationens förmåga att få åtkomst till dess egna användare.
Användare har också en viss oro över att ge åtkomst till sina uppgifter. Det är då viktigt att tydligt upplysa om hur användaruppgifterna kommer att användas.

## BE 1.9 HTTP-protokollet
Vad?
HTTP (hyper text transfer protocol) är ett protokoll för hur data skickas över internet. Det är en standard för hur man skickar förfrågan och svar mellan servrar och klienter.
Hur?
När klienten (t ex en webbläsare) skickar förfrågan till en server så skickas en HTTP-förfrågan. En HTTP-förfrågan innehåller olika delar:
Metod. Olika metoder är GET, POST, PUT och DELETE, beroende på vad man vill göra, vill man hämta data, skicka data, uppdatera eller radera data.
URI, en adress till den delen klienten vill interagera med. Det kan t ex vara en URL eller en sökväg.
Headers och body som innehåller t ex cookies, autentiseringsuppgifter, JSON-data etc.
Servern analyserar alltså den förfrågan den får, och behandlar den. T ex behandlar data i en databas eller gör olika valideringar.
Efteråt skickas ett HTTP-svar tillbaka till klienten. Det innehåller statuskod, som t ex 404 not found.
Även i svaret skickas header och body med.
När svaret når klienten så används det för att utföra åtgärder, t ex visa en hemsida, visa data, eller göra fler anrop.
Varför?
Det är enkelt och ett väl beprövat protokoll som fungerar på olika plattformar och operativsystem. Det går att kommunicera mellan klienter och servrar som är byggda på olika språk. Det gör det även lätt att fortsätta utvecklingen av applikationer som använder sig av HTTP-protokollet. Det kan vara enkla webbsidor till avancerade APIer.
HTTP är inte ett säkert sätt att överföra data, då det inte är krypterat. Det man istället använder heter HTTPS (HTTP secure) som är samma sak men har ett lager av säkerhet implementerat. 

## BE 1.10 cURL
Vad?
cURL är ett command line verktyg som används för att skicka och ta emot data via olika protokoll, t ex HTTP, HTTPS, IMAP, POP3, TELNET, GOPHER(S), SCP, TFTP, RTSP osv.
cURL betyder client for URLs och syftar till att det är en klientapplikation som används för att interagera med olika URLs (en standardiserad adress för t ex webbsidor, filer, API-endpoints osv). cURL kan förutom att hämta data, använda HTTP cookies, är open source och gratis och kan användas i flera olika operativsystem.
Hur?
Du ger anger den URL du vill använda till cURL. cURL upprättar en TCP/IP-anslutning till URLens server och skickar sedan iväg en (t ex) HTTP-förfrågan dit. Sedan skickar servern tillbaka ett svar till cURL i (t ex)  HTTP-format som presenteras för användaren.
Varför?
CURL går att använda på olika operativsystem och behöver ingen speciell installation eller konfiguration. Det kommer dessutom numera färdiginstallerat på MasOS och Windows.
cURL är mångsidig som erbjuder olika alternativ att anpassa förfrågningar och svar, och kan utföra många olika typer av operationer, t ex hämta webbsidor, interagera med APIer, felsökning. 
Den har också stöd för kryptering. 
cURL har däremot svårt att hantera annat än automatiserade uppgifter, som t ex autentisering. Dock kan man autentisera anropen med HTTP autentiseringsmetoder.
cURL stödjer dual-stack, den kan kommunicera med både IPv4 och IPv6, olika versioner av identifiering av enheter på internet.

## BE 1.11 REST
Vad?
REST står för representational state transfer. Det är en uppsättning principer för hur APIer ska utformas och fungera. Dessa är separation av klient och server, statelessness, svar som går att cachea, samt uniformt interface.
Hur?
Separation av klient och server betyder att frontend och backend API kan utvecklas oberoende av varandra. 
Statelessness betyder att servern inte lagrar någon information om klienten. Varje förfrågan innehåller enbart det som behövs för att kunna behandla den, oberoende av tidigare förfrågningar. Det betyder att klienten måste inkludera all nödvändig info i varje förfrågan, eftersom ingen historik sparas.
Svar ska gå att cashea, då servern kan utnyttja cashning för att effektivisera datatrafiken.
Uniformt interface innebär att APIerna ska vara enhetliga och konsistenta oavsett vad som görs. Det innefattar bl a användning av standardformat för att representera APIerna, så som JSON och XML. Det betyder också identifiering av resurser, samt manipulation av resurserna genom CRUD / GET, POST, PUT, DELETE. Även självbeskrivande meddelanden med inkluderat vilken åtgärd som kan vidtas för att korrigera ett felmeddelande, samt länka resurser med varandra.
Varför?
Majoriteten av APIer som skapas går efter detta. Det är återanvändbarhet eftersom all data är standardiserad. Enkler integration.

## BE 1.12 XML och andra dataformat
Vad? Hur? Varför?
XML är kort för extensible markup language och är ett dataformat som är textbaserat och har struktur som innehåller taggar (precis som HTML). Det är ett vanligt format för att utbyta och lagra data och används ofta tillsammans med t ex APIer. XML är plattformsoberoende.
I XML finns det en grundsyntax, deklaration, element, attribut, inkapsling etc som i de flesta andra språk. Syntaxen är ganska lik HTML.
CSV står för Comma-Separated Values och är också textbaserat. Datan är representerad i tabellform och används ofta för att exportera och importera data i t ex kalkylbladsprogram som har olika filformat.
Kolumnerna i tabellerna separeras av komma, tab, kolon, semikolon och lodstreck.
JSON är kort för JavaScript Object Notation och är baserat på text. Det anses som enklare än XML och har blivit populärt för att det är lätt att hantera tillsammans med JavaScript. JSON är en samling av namn/värde par (inom citattecken) och är en ordnad lista av värden. Värden kan vara string, tal. Objekt, array, boolean osv.
Dessa tre, XML, CSV och JSON är de vanligaste dataformaten inom applikationer och APIer.

## BE 1.13 Webbservrar
Vad?
En webbserver är programvara eller dator som över HTTP-protokollet tillhandahåller data till klienter. Den tar emot förfrågningar, behandlar dom och skickar tillbaka svar.
En fysisk webbserver är en dator som kan hantera och leverera webbinnehåll. Dom är konstruerade för att kunna hantera flera anslutningar samtidigt. Dom står ofta hos driftbolag och har snabb uppkoppling mot internet.
En webbserver-applikation är ett program som installeras och är ansvarig för att hantera anslutningar, tolka frågor och skicka tillbaka svar. Där har vi t ex Apache och Nginx.

Hur? Varför?
När man skriver en webbadress så försöker man nå en server i stora drag. Webbläsaren skickar en begäran som en DNS konverterar till en IP-adress som i sin tur leder till servern. När den är nådd så kan den presentera innehållet i webbläsaren. Alla enheter som är uppkopplade mot internet har en egen unik IP-adress för kommunikation. Den har dock begränsad funktionalitet och bör bara användas för att testa vissa funktioner i koden.
Idag är Apache den vanligaste webbservern, den hanterar ca 70% av alla webbplatser i dagsläget. Apache har öppen källkod.
Det finns en webbserver som är inbyggd i PHP och nås genom kommandot ”php -S localhost:80” i terminalen. 
Det finns också en typ av mindre webbservrar för företag som kallas intranät.

