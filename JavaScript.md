# Teorihandboken - JavaScript (JS)
Studerande: Malin Bragazzi
## JS 1.1 JavaScript / ECMAScript
Vad?
JavaScript är ett språk inom programmering. Det skapades som ett sätt att lägga till funktioner på webbsidor i Netscape, men nu för tiden så används det av alla större webbläsare och det används till att skriva hela webbsidor och spel. Det kan lägga in funktioner i både klienter och servrar, det vill säga både frontend och backend.
När fler och fler började använda JavaScript så krävdes det en standardisering av språket, och det är vad ECMAScript är. Ett språk som också är en standard för JavaScript. Det beskriver syntax, funktioner bl a.
Hur?
För att kunna få igång funktionerna så måste vi köra/exekvera koden. Det kan köras i en webbläsare eller med Node. 
JavaScript kan ändra HTML-element, hantera händelser så som klick, inmatning, skapa animationer osv. Det skrivs som en <script>-tag. Man kan skriva sin JavaScript direkt i HTML-dokumentet men det är god kutym att ha det i en separat JavaScript-fil som man länkar till. Det gör att sidan laddas fortare, bland annat.
Koden läses uppifrån och ner, så det spelar absolut roll vilken ordning man skriver koden i.
Det finns olika sätt att kommentera inom JavaScript, och det är enradskommentar som är // och det är block-kommentar som är */ …… /*.
Varför?
JavaScript är relativt lätt och bra för nybörjare att använda, samtidigt som det är ett flexibelt språk. Det är bra för att göra dynamiska webbsidor som anpassas efter t ex bilder och användar-input. Det går även att använda JavaScript för mobilappar (med hjälp av ramverk), samt för IoT-enheter. JavaScript har dessutom stöd för många tredjepartsbibliotek och ramverk.

## JS 1.2 JavaScript-ramverk och -bibliotek
Vad? Hur?
Både ramverk och bibliotek är verktyg som används för att underlätta utvecklingen av applikationer och program. De erbjuder färdiga lösningar, strukturer och komponenter för språket i fråga.
React är ett ramverk som används inom JavaScript. Det är ett gränssnitt som använder sig av komponenter som delas upp och kan återanvändas på olika ställen i projektet. React tillhandahåller också en så kallad virtual DOM så att man kan hantera webbsidan och ändra vid behov.
Angular är också ett ramverk för JavaScript. Det har utvecklats av Google. Det är också en strukturerad modell att bygga i, också komponentbaserad, och erbjuder funktioner som routing, formulärhantering osv.
Vue.js är också ett ramverk, det har likheter med både React och Angular men är mer lättanvänt och lättviktigt.
Ett populärt bibliotek för JavaScript är jQuery. Det gör det lätt att manipulera DOM och hantera händelser så som klick och inmatning. Det erbjuder också metoder för att bl a genomföra animationer.
Axios är ett HTTP-bibliotek men används för att göra HTTP-förfrågningar från JavaScript-applikationer. Det har ett enkelt gränssnitt för att skicka och ta emot data från server och stöjder funktioner som autentisering, hantering av fel samt asynkrona förfrågningar.
Varför?
Det underlättar arbetets gång och strukturerar upp projekt så de blir lättöverskådliga när man lärt sig använda ett ramverk eller bibliotek. Nackdelen är att det kan vara svårt att lära sig och i början resultera i att enklare projekt blir komplicerade. Det är som alltid bäst att välja arbetssätt baserat på projektet i fråga.

## JS 1.3 Promises
Vad?
Promises är en del av JavaScript och finns inbyggt i moderna webbläsare och Node.
En promise är ett löfte om att svarskod kommer levereras vid ett eller annat tillfälle, oavsett resultat.
Det är en inbyggd mekanism i JavaScript som hanterar asynkrona operation. En asynkron operation är en funktion som inte behöver slutföras innan nästa rad på koden läses in, utan den ligger asynkront i bakgrunden och gör en ”callback” vid ex en inmatning. Renodlade callbacks har använts för att hantera dessa asynkrona operationer, men promises har uppkommit som en bättre lösning. 

Hur?
När du skapar en promise så är den pending, det vill säga resultatet inväntas fortfarande.
Du använder metoder som .then() och .catch() för att berätta vad som händer när svaret inkommit och nästa operation ska utföras. 
Den kan vara fulfilled och det blir den när operationen är lyckad och slutförd. Då kan man köra vidare kod som inväntat ett svar.
En promise kan också vara rejected och det är om den blir avvisad, och då bör ett felmeddelande genereras. Det är det som är ”catch”. Att koden fångar upp att operationen inte är lyckad, och istället genererar ett felmeddelande.
Varför?
En promise är ett mer strukturerat sätt att hantera asynkrona operationer och det gör de lättare att hantera än vanliga callbacks. Det är lättare att följa koden och det underlättar om det är flera operationer som behöver vara asynkrona samtidigt. Man kan dessutom skapa en kedja av asynkrona operationer med hjälp av then-metoden.
Då promise använder catch-metoden så blir det lättare att hantera fel.

## JS 1.4 OOP i JavaScript
Vad?
OOP står för objektorienterad programmering, och det fokuserar på att organisera koden i form av objekt. OOP används för att beskriva data och funktionalitet som är relaterade. Man delar upp koden i mindre enheter som blir mer hanterbara.
Hur?
Genom objekt i koden så har vi kapslat in funktionalitet och data, och på så sätt gör det lättare att komma åt den funktionalitet vi behöver.
Man använder sig av inkapsling, abstraktion, arv och polymorfism. De är de 4 grundpelarna inom OOP.
Inkapsling för att ha data och funktioner kopplade till en entitet, och bara visa de egenskaper som är aktuella att interagera med. 
Abstraktion för att fokusera på dom viktigaste egenskaperna och beteendena hos ett objekt, man skapar en enkel modell av något som är mer komplext. Detaljerna döljs.
I arv så bygger man klasser baserat på andra klasser och behöver inte upprepa kod som ska finnas i flera olika. Subklasser ärver av sina föräldrar.
 Med polymorfism så menar man en enhetlig behandling olika typer av objekt i en hierarki. Alltså att man kan ge olika klasser en enhetlig behandling genom att sätta en överklass som är gemensam för dom, så att dom ärver från den. Men även implementera sina egna varianter av metoden/funktionen.
Klasser är alltså en mall för ett objekt.
När vi anropar .this i en funktion eller metod så hänvisar .this till objektet som funktionen /metoden anropas på.
Varför?
För att man vill undvika att data och funktioner ligger utspridda. Man vill gruppera dessa och ha en struktur på arbetet. Det går dessutom att återanvända kod på ett enklare sätt utan att repetera den om den ligger i objekt.

## JS 1.5 DOM-manipulation
Vad?
DOM står för document object model. DOM-manipulation är sättet att ändra och manipulera ett HTML-dokument dynamisk med hjälp av JavaScript. När du laddar en webbsida så skapar din browser en DOM av sidan. Varje element, attribut och nod på sidan är ett objekt i DOM. 
Det är alltså ett gränssnitt för webbdokument.
Hur?
När man manipulerar DOM men hjälp av JavaScript så ändrar man innehåll, utseende och beteende i realtid. Det är så man skapar dynamiska och interaktiva webbsidor som reagerar på t ex bilder, och inmatning.
JavaScript pratar alltså med webbläsaren och vi kan ändra HTML-element och -attribut. Vi kan även lägga till eller ta bort existerande element och attribut. Det är dessutom möjligt att ändra CSS-styling på sidan och skapa events, det vill säga att något ska ske i webbläsaren och eventet blir utlöst av en händelse, så som musklick, laddning av sidan, inmating etc. Så ett event kan vara att t ex ordet ”Tack” dyker upp efter att ett formulär har skickats in på en webbsida.
Man hämtar en referens till det element som ska manipuleras. Till det finns metoder som getElementById, getElementByClassName, querySelector osv. Sedan ändrar man det som ska ändras. Och efter det kan man binda en händelsehanterare till elementet, t ex klick, laddning av sidan, hover eller inmatning från tangentbordet.
Man kan binda ett enstaka element, eller så kan man binda alla element med samma attribut (t ex ID) och då sparas dom i ett arrayformat.

Varför?
Man kan skapa webbsidor som anpassar sig efter användarens beteende och det skapar en rikare användarupplevelse.

## JS 1.6 HTTP-requests
Vad? Hur?
HTTP-requests är en viktig del av kommunikationen mellan klient och server. En klient är t ex en webbläsare eller en applikation, och med server så menar jag en webbserver. HTTP står för hypertext transfer protocol och är ett protokoll som används för att överföra data på internet.
När webbläsaren skickar en HTTP-förfrågan till servern så vill den ha ett svar tillbaka. Det finns olika förfrågningar för olika ändamål. 
GET används för att hämta data, som till exempel en webbsida, bilder, filer.
POST används för att skicka data för att till exempel spara inmatad information. Det används när du skickar in ett formulär på en sida.
PUT används för att ändra, alltså ersätta data på servern.
PATCH som vill ändra specifika delar istället för att ersätta allt det gamla, som PUT gör.
DELETE används för att radera data.
Servern i sin tur bearbetar förfrågan och skickar ett HTTP-respons till klienten. Detta innehåller bl a en statuskod på 3 siffor såsom 200 (lyckad förfrågan), 404 (not found) och 500 (interal sever error).
HTTP-requests i JavaScript innebär att man kan göra såna förfrågningar direkt i koden. I JavaScript så finns det inbyggda funktioner och APIer som kan skicka både förfrågan och ta emot svar.
XMLHttpReqest är en äldre metod för detta och med den kan man skicka asynkrona förfrågningar.
Fetch API är mer modern än den via XML. Fetch API används tillsammans med en promise i koden, och omvandlas gärna till json och skrivs ut i konsollen, under utvecklingsskedet.
Ajax är en teknik som används för detta, där kan man uppdatera delar av webbsidan dynamiskt, och behöver därmed inte vänta på en hel sidomladdning, t ex vid chattmeddelanden eller nyhetsflöden.
Varför?
Det är för att interagera med webbtjänster. Det gör det möjligt att skicka information och få svar tillbaka.

## JS 1.7 Lexical scope
Hur? Vad?
Lexical scope är en princip som avgör hur variabler är tillgängliga inom ett projekt. Det defineras av den hierariska strukturen.
Scope definierar vilken del av koden som funktionen eller variabeln kan anropas i.
När till exempel variabler deklareras i en funktion så är de tillgängliga för det scopet (den funktionen) och alla scope som bildas inuti det. Varje block, funktion etc som bildas skapar ett nytt scope. Om variabeln som JavaScript söker efter, inte finns i det aktuella scopet, så kommer JavaScript att söka uppåt i hierarkin. Om variabeln inte hittas uppåt så får man ett felmeddelande.
Variabeln är alltså synlig där den deklarerats och i  inre funktioner, men inte utanför dom.
Varför?
Det underlättar funktionell programmering och modulär kodstruktur där olika delar av koden inte påverkar varandra. Det underlättar vid ändringar att det slipper bli för riskabelt för hela projektet.
Koden blir mer förutsägbar vid hantering av variabler och funktioner. Det gör koden lättare att förstå, det undviker namnkrockar samtidigt som modulär kod kan återanvänds om de importeras på rätt sätt.
Det är ett tydligt sätt att separera koden på ett strukturerat och hierarkiskt sätt.
Ett par nackdelar kan vara svårigheter att felsöka om det är många nivåer av inbäddade funktioner. Och när det är många nivåer av scope så kan det bli en fördröjning i prestandan eftersom programmet måste gå igenom scope chain vid varje åtkomst. Det är dock vanligtvis en mycket liten fördröjning.

## JS 1.8 Event handling
Vad?
Ett event kan vara till exempel att en webbsida laddat klart, att det skett en inmatning i ett formulär eller ett knapptryck på mus eller tangentbord.
Event handling är hur vi får JavaScript att reagera på dessa events. Det handlar om att lyssna på händelser så som till exempel en klick med musen, inmatning via tangentbord, muspekarens rörelse, laddning av webbsidan,  om man hovrar med musen över ett föremål på webbsidan.
Hur?
En event handler är ett kodblock som körs när eventet skett. Skillnaden på event handlers och event listeners är att handlers tar hand om de event som listeners väntar på ska ske.
Det finns olika sätt att hantera en händelse i JavaScript. Till exempel har vi Inline-eventhantering. <button onclick="handleClick()">Klicka här</button> När nu användaren klickar på knappen så körs funktionen handleClick. 
Det finns även metodreferens, där anger man eventhandlers genom att sätta ut dom på olika ställen i koden. Du hämtar elementet i fråga och lägger till t ex metoden addEventlistner. Då ser det it såhär: document.getElementById("myButton").addEventListener("click", handleClick) 
Det finns även anonyma funktioner, dom kallar man bara function() utan att de har ett namn.
När händelsen inträffar så kan man göra olika events, så som att manipulera DOM-element, uppdatera data på sidan, men du kan också stoppa händelsen genom att använda funtionen preventDefault.
Varför?
Det skapar en interaktiv webbsida som kan reagera på användarens aktioner i realtid.
Om man har för många event handlers på sin sida så kan det dock skapas flaskhalsar och det påverkar prestandan.

## JS 1.9 Prototype inheritance
Vad? Hur?
JavaScript är ett prototypbaserat språk. I JavaScript är en prototyp ett objekt som används som mall för att skapa andra objekt. När nya objekt skapas så ärver dom egenskaper och metoder från moderobjektet. Det innebär att  objektet kan kommer åt de egenskaper och metoder som finns i moderobjektet.
Så, när ett visst objekt försöker komma åt en ärvd egenskap eller metod, så letar JavaScript efter den på objektet i fråga. Om den inte finns där, så fortsätter JavaScript att leta uppåt i prototypkedjan tills den hittar deklarationen av egenskapen eller metoden, eller tills den når toppen av kedjan där Object.prototype finns, där vi ärver ifrån.
Ändringar finns dock kvar enbart på objektet ifråga som utförde ändringarna.
T ex så är array prototyp för alla array-objekt. Array-prototypen har egenskaper och metoder som t ex push(), pop(), forEach(). Dessa metoder ärvs av alla andra arrays.
Varför?
Genom att ärva egenskaper från prototyper så kan man återanvända kod utan behöva återupprepa den.
Om man gör ändringar i prototypen så ändras det i alla objekt som ligger i arvskedjan.
Det är enkelt att använda prototypbaserade arv, och det går snabbt att ändra i prototypen om man vill att ändra i samtliga objekt.
Det är ju dock också en nackdel om man inte är aktsam, det kan skapa oavsiktliga ändringar.

## JS 1.10 Higher-order functions
Vad?
En higher-order function är en funktion som kan ta en annan funktion som argument. Det är också en funktion som kan returnera en funktion som resultat.
Hur?
När man skickar in ett argument i en funktion så skriver man det innan för parentesen efter deklarationen av funktionen. Dit kan man skicka in objekt eller variabler, men i JavaScript kan man skicka in andra funktioner och använda den inuti sin egen logik. En high-order function kan också returnera en funktion som resultat. Det gör att man kan skapa funktioner dynamisk baserat på olika villkor och kriterier.
I JavaScript går att hantera funktioner som om de vore argument. Man kan alltså skicka in funktioner i en funktion. Då de kan bli hanterade som variabler så kan de även bli returnerade. Detta skapar funktionell programmering.
Några funktioner som är inbyggda i arrays låter oss använda higher order functions och det är foreach, map, filter och reduce.

Varför?
Det ger ökad flexibilitet och återanvändbarhet, att kunna generera funktionssvar inuti andra funktioner. Det ger kortare kod som är mer översiktligt om man inte behöver definiera villkor flera gånger utan istället skicka in en färdig funktion.
Det gör dock koden också mer komplex, och det kan vara svårt att vänja sig vid detta då det inte är vanligt i andra stora programmeringsspråk.
Som andra koder som involverar fler loopar, block och scopes så kan det leda till en liten förlust i prestandan när programmet måste gå in djupt i koden och leta.

## JS 1.11 Single-thread programming
Hur?
Programmet behandlar och utför instruktionerna en efter en ända tills den når slutet av programmet, eller tills den stöter på en instruktion som väntar på inläsning av data etc. Det är alltså bara en uppgift eller operation som utförs åt gången, och först när den är klar så kan nästa uppgift eller operation utföras.
Det är viktigt att göra koden effektiv, så att man förhindrar att det t ex inte skulle svara.
Det kan man göra genom att lägga in asynkron programmering, som ändå kommer att utföras samtidigt. Man kan också flytta kodblock, som är benägna att blockera, till bakgrundsprocesser eller trådar för att hålla huvudtråden fri att rulla på.
Vad?
Single-thread programming innebär att ett program körs en i enda tråd av exekvering. När programmet körs så börjar det uppifrån och arbetar sig nedåt.
Varför?
Det är lättare att hantera programmet, och man behöver inte handskas med trådar som stör varandra eller prestandaförlust som kan komma sig av delade resurser såsom minne. Endast en tråd gör också att det blir färre buggar vilket sparar tid vild utveckling och underhåll. Programmet blir nämligen mer förutsägbart och man kan undvika fel på ett lättare sätt.
Dock är single-thread programming inte så effektivt att utnyttja hårdvarans förutsättningar, så som flera processorkärnor. Det kan leda till långsamhet och försämrad prestanda trots att själva datorn har bra förutsättningar.
Det är alltså en bra ide att använda single-thread programming vid mindre applikationer men vid större program så kan det skapa problem med långsamhet.

## JS 1.12 OAuth från frontend
Hur? Vad? Varför?
OAtuh är ett standardprotokoll för autentisering och auktorisering, och innebär att man kan använda sin inloggning hos en tredje part för att logga in på en viss hemsida. Exempel på tredje parten är facebook och google. Användaren behöver alltså inte dela mig sig av sina uppgifter, utan inloggningen helt helt hos tredje part.
När detta sker i frontend så används ofta OAuth-bibliotek eller ramverk som har funktioner och API-anrop för att underlätta flödet.
Passport.js är ett populärt sådant ramverk för Node-applikationer. Auth0 är en molnbaserat autentiseringstjänst. Firebase Authentication är googles egna plattform för utvecklare, och erbjuder bl a OAuth-protokollet.
OAuth 2.0 Implicit Grant är variant inom autentiseringsflödet som används för att autentisera på klientens webbläsarsida. Den används ofta när klientappen är single page eller när en mobilapp inte har en säker servermiljö. Så klientappen skickar en förfrågan till tredjeparten genom att omdirigera användaren dit. Användaren loggar in, och direkt då skickas en åtkomsttoken till klientappen. Dock har detta sätt vissa säkerhetsrisker efter användaren kan se åtkomsttoken.
OAuth Authorization code grant with proof key for code exchange (PKCE) är en förbättrad och mer säker version än den förra. Den här metoden genererar en code challenge baserat på en slumpmässig verifier som genrerats innan autentiseringsprocessen påbörjats, och ska användas innan token skickas. Token skickas bara om verifiern och code challenge matchar varandra. 
Fördelar med dessa ramverk är att de är utvecklade specifikt för att hålla hög säkerhet. De kan vara svåra att lära sig, men det finns en hel del exempelkoder och dokumentation samt aktiva supportforum.
Det kan dock vara onödiga stora bibliotek eller ramverk för små applikationer, så det är bäst att välja utifrån appen du ska tillverka.

## JS 1.13 Websockets
Vad?
Websockets är en standard inom kommunikationsprotokoll, och det tillåter en permanent kommunikation mellan en klient och en server. Det gör det möjligt att skicka data ofta utan att behöva upprätta en anslutning varje gång. Det är en tvåvägskommunikation, så det är bara mellan server och klient.
Det minskar onödig nätverkstrafik då data kan flöda åt båda hållen genom en anslutning.
Hur?
Vanligtvis används HTTP-protokollet vid kommunikation mellan server och klient, men när det krävs kommunikation i realtid så är det bättre med websockets. Det är t ex vid chattapplikationer, realtidsövervakning (så som trafik, temperatur, ekonomi osv), spelapplikationer eller appar där flera jobbar samtidigt, t ex google docs.
Med websockets kan alltså webbsidor och applikationer uppdateras direkt när ny information finns på servern, utan att behöva vänta in ett svar.
Websockets kan användas på olika enheter, bl a både webbläsare och mobilappar.
Vi upprättar kontakt med en server och lyssnar sedan på event. Det finns 4 olika events:
Open, connection established
Message, data recieved
Error, websocket error
Close, connection closed
Dessa händelser är viktiga att lyssna på och ge lämpliga åtgärder om det behövs. En anslutning kan annars vara öppen i flera timmar, eller till och med dagar om servern, nätverket och webbläsaren tillåter det. Och det kan ge ökad belastning på servern och nätverket.
Varför?
Det möjliggör realtidskommunikation, att data skickas och tas emot omedelbart. Prestandan förbättras när det inte behöver upprättas anslutning och avsluta anslutning för varje förfrågan och svar som skickas.
Websockets behöver stöd från både webbläsare och server, vilket gör att vissa äldre webbläsare kan sakna stödet.

