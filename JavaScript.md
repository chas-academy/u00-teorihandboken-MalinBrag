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
Det är en inbyggd mekanism i JavaScript som hanterar asynkrona operation. En asynkron operation är en funktion som inte behöver slutföras innan nästa rad på koden läses in, utan den ligger asynkront i bakgrunden och gör en ”callback” vid ex en inmatning. 
Promises är en del av JavaScript och finns inbyggt i moderna webbläsare och Node.
Hur?
En promise kan vara pending, och det är den när den skapas. Resultatet är alltså inte klart ännu.
Den kan vara fulfilled och det blir den när operationen är lyckad och slutförd. Då kan man köra vidare kod som inväntat ett svar.
En promise kan också vara rejected och det är om den blir avvisad, och då bör ett felmeddelande genereras.
Varför?
En promise är ett mer strukturerat sätt att hantera asynkrona operationer och det gör de lättare att hantera än vanliga callbacks. Det är lättare att följa koden och det underlättar om det är flera operationer som behöver vara asynkrona samtidigt. Man kan dessutom skapa en kedja av asynkrona operationer med hjälp av then-metoden.
Då promise använder catch-metoden så blir det lättare att hantera fel.

## JS 1.4 OOP i JavaScript
Vad?
OOP står för objektorienterad programmering, och det fokuserar på att organisera koden i form av objekt. OOP används för att beskriva data och funktionalitet som är relaterade. Man delar upp koden i mindre enheter som blir mer hanterbara.
Hur?
Genom objekt i koden så har vi kapslat in funktionalitet och data, och på så sätt gör det lättare att komma åt den funktionalitet vi behöver.
Man använder sig av inkapsling, abstraktion, arv och polymorfism.
Inkapsling för att ha data och funktioner kopplade till en entitet. Abstraktion för att fokusera på dom viktigaste egenskaperna och beteendena.
I arv så bygger man klasser baserat på andra klasser och behöver inte upprepa kod som ska finnas i flera olika. Med polymorfism så menar man en enhetlig behandling av klasser i en hierarki. Alltså samma metoder för objekt i olika klasser.
Varför?
För att man vill undvika att data och funktioner ligger utspridda. Man vill gruppera dessa och ha en struktur på arbetet. Det går dessutom att återanvända kod på ett enklare sätt utan att repetera den om den ligger i objekt.

## JS 1.5 DOM-manipulation
Vad?
DOM står för document object model. DOM-manipulation är sättet att ändra och manipulera ett HTML-dokument dynamisk med hjälp av JavaScript. När du laddar en webbsida så skapar din browser en DOM av sidan. Varje element, attribut och nod på sidan är ett objekt i DOM. 
Det är alltså ett gränssnitt för webbdokument.
Hur?
När man manipulerar DOM men hjälp av JavaScript så ändrar man innehåll, utseende och beteende i realtid. Det är så man skapar dynamiska och interaktiva webbsidor som reagerar på t ex bilder, och inmatning.
JavaScript pratar alltså med webbläsaren och vi kan ändra HTML-element och -attribut. Vi kan även lägga till eller ta bort existerande element och attribut. Det är dessutom möjligt att ändra CSS-styling på sidan och skapa events. 
Man hämtar en referens till det element som ska manipuleras. Till det finns metoder som getElementById, getElementByClassName, querySelector osv. Sedan ändrar man det som ska ändras. Och efter det kan man binda en händelsehanterare till elementet, t ex klick, laddning av sidan, hover eller inmatning från tangentbordet.

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
En förfrågan innehåller även en URL till den begärda resursen på servern. Headers, som innehåller metainfo, accepterade språk och autentiseringsuppgifter, och body som innehåller annan eventuell data.
Servern i sin tur bearbetar förfrågan och skickar ett HTTP-respons till klienten. Detta innehåller bl a en statuskod på 3 siffor såsom 200 (lyckad förfrågan), 404 (not found) och 500 (interal sever error).
Varför?
Det är för att interagera med webbtjänster. Det gör det möjligt att skicka information och få svar tillbaka.

## JS 1.7 Lexical scope
Hur? Vad?
Lexical scope är en princip som avgör hur variabler är tillgängliga inom ett projekt. Det defineras av den hierariska strukturen, så variabler och funktioner är tillgängliga inom samma block som de definerats i, eller om de definerats i blocket utanför (om det är ovanför blocket ifråga) eller i globala omfattningen (också om det är ovanför blocket i fråga). Alltså bara om scopet är överordnat.
Så något som deklarerats utanför och nedanför blocket går inte att kalla på. Det är utanför ”the lexical scope”.
The lexical scope är alltså den delen av koden där en variabel eller funktion är aktiv och går att kalla på.

Varför?
Det underlättar funktionell programmering och modulär kodstruktur där olika delar av koden inte påverkar varandra. Det underlättar vid ändringar att det slipper bli för riskabelt för hela projektet.
Koden blir mer förutsägbar vid hantering av variabler och funktioner. Det gör koden lättare att förstå, det undviker namnkrockar samtidigt som modulär kod kan återanvänds om de importeras på rätt sätt.
Ett par nackdelar kan vara svårigheter att felsöka om det är många nivåer av inbäddade funktioner. Och när det är många nivåer av scope så kan det bli en fördröjning i prestandan eftersom programmet måste gå igenom scope chain vid varje åtkomst. Det är dock vanligtvis en mycket liten fördröjning.

## JS 1.8 Event handling
Vad?
Event handling är hur vi får JavaScript att reagera på saker som händer i webbläsaren. Det handlar om att lyssna på händelser så som till exempel en klick med musen, inmatning via tangentbord, muspekarens rörelse, laddning av webbsidan, eller om man hovrar med musen över ett föremål på webbsidan.
Hur?
Det finns olika sätt att hantera en händelse i JavaScript. Till exempel har vi Inline-eventhanering. <button onclick="handleClick()">Klicka här</button> När nu användaren klickar på knappen så körs funktionen handleClick. 
Det finns även metodreferens, där anger man eventhandlers genom att sätta ut dom på olika ställen i koden. Du hämtar elementet i fråga och lägger till t ex metoden addEventlistner. Då ser det it såhär: document.getElementById("myButton").addEventListener("click", handleClick) 
Det finns även anonyma funktioner, dom kallar man bara function() utan att de har ett namn.
När händelsen inträffar så kan man göra olika events, så som att manipulera DOM-element, uppdatera data på sidan, men du kan också stoppa händelsen genom att använda funtionen preventDefault.
Varför?
Det skapar en interaktiv webbsida som kan reagera på användarens aktioner i realtid.
Om man har för många event handlers på sin sida så kan det dock skapas flaskhalsar och det påverkar prestandan.

## JS 1.9 Prototype inheritance
Beskriv rubriken här

## JS 1.10 Higher-order functions
Beskriv rubriken här

## JS 1.11 Single-thread programming
Beskriv rubriken här

## JS 1.12 OAuth från frontend
Beskriv rubriken här

## JS 1.13 Websockets
Beskriv rubriken här

