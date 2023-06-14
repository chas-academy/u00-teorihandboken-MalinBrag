# Teorihandboken - Programmeringsmetodik (PG)
Studerande: Malin Bragazzi

## PG 1.1 Versionshantering (Git)
Vad? Versionshantering är ett sätt att uppdatera kod, tillägga, ta bort eller ändra sin kod i ett projekt (repository). Det är ett bra sätt att jobba i grupp på samma projekt. 
Branches använder man för att jobba på olika versioner/delar av samma projekt samtidigt, vilket är nödvändigt om man jobbar i grupp, så man inte stör någon annans arbete. Man arbetar på sin egen bransch lokalt på sin egen dator.
Man sparar sitt arbete i commits (som är ansluten till databasen) när man avslutat en task, skriver vad som gjorts i committen, och sedan pushar man den till repositoryt så att den blir sparad inte bara lokalt, utan även på t ex Github online. Då kan alla andra i samma projekt göra en pull och få den senaste versionen av det gemensamma repot.
Genom en merge så kan man sammanslå två olika branches till en och samma.
Hur?
Man pushar sin kod till till exempel Github, ser till att den inte ger konflikter med existerande, redan godkänd kod, och sedan accepterar den. Det går att spåra vem som gjorde vad och när i projektet, om man skulle behöva återgå till en tidigare version av någon anledning så går den också att spåra.
Det ger en bra struktur och översikt över kodning helt enkelt.
Varför?
Man behåller historiken av projektet, alla ändringar och utvecklingar, och det ger ett bra arbetsflöde för både stora och små projekt. Man kan spåra ändringar, hantera konflikter och återgå till tidigare versioner av projektet med denna metod.

## PG 1.2 Benchmarking
Vad? Benchmarking är ett sätt att utvärdera sitt arbete i jämförelse med konkurrenter (eller standarder som finns på marknaden). 
Hur? Först måste du veta varför du vill göra en benchmarking. Är det en funktion i din app som behöver förbättras eller är det hastigheten eller övergripande? Eller något helt annat? Ha ett tydligt mål med benchmarkingprocessen. Då kan du lättare välja ut företag eller program att jämföra med.
Sedan får du välja på vilket sätt du ska jämföra, är det med t ex ramverk och bibliotek som ofta tillhandahåller kod för hur algoritmer och vanliga kodsekvenser ska skrivas. Då kan du se hur du kan förbättra ditt eget arbete. Det finns även profileringsverktyg som på liknande sätt kan analysera din kod och identifiera vart det finns förbättringsområden.
Utöver detta så finns det renodlade benchmarkingtjänster och tredjepartsverktyg som hjälper till med tester och andra metoder för att mäta prestandan. Samla in data om konkurrenter och genomför själva processen.
Vad du ska välja för din egen benchmarkingprocess är helt beroende på vad du har för mål, vilka dina konkurrenter är som du ska jämföra mot, och vad du använder för språk och plattform.
Analysera resultaten och dokumentera svagheter och styrkor och bestäm vad du vill göra för förändringar.
Genomför sedan förändringarna och övervaka dessa för att se om du uppnådde ditt önskade resultat.
Varför?
Eftersom att denna bransch utvecklas snabbt och ofta så är det en bra ide att jobba kontinuerligt med benchmarking. Detta för att du ska vara konkurrenskraftig på marknaden.

## PG 1.3 Testdriven utveckling
Vad?
Testdriven utveckling (TDD för test-driven development) är en metod som går ut på att man skriver tester innan man implementerar ”den riktiga koden”. Den baseras på att man först skriver testerna och utifrån resultaten skriver man koden för själva mjukvaran. Detta istället för att först göra klart programmet och sedan utföra tester och eventuellt behöva ändra i efterhand.
Hur?
Om du ska lägga till en ny funktion i ditt program så skriver du först test, det är t ex test för användare och rena kodtest, samt hur de integreras med redan existerande kod. Det gör det lätt att specificera nödvändiga krav innan den nya t ex funktionen skrivs.
Det första testet som skrivs är det som bevisar att den existerande koden behöver ändras, alltså, det första testet kommer att misslyckas med flit. Efter det skriver man tester för att utveckla koden åt rätt håll, och fortsätter att köra tester, och så kör man på tills att testerna lyckas och då har man koden att implementera i sin programkod.
Detta görs för varje ny ändring som ska göras och bidrar till en tydligare utvecklingsprocess.

Varför?
Det gör det lätt att specificera nödvändiga krav innan den nya t ex funktionen skrivs och det gör det lättare att göra större förändringar i programkoden. Detta innebär lägre kostnader på sikt om man sällan behöver göra ändringar i sitt program.
Det förebygger även buggar och att redan existerande kods funktionalitet slås ut.
Det bidrar också till snabbare felsökning eftersom alla tester som skrivs dokumenteras.

## PG 1.4 Deploy och staging
Vad?
Deploy och staging används för att hantera testning av applikationer innan produktion.
Att göra en deploy är att ta ett färdigutvecklat program och göra den tillgänglig för användare. Att deploya kan bl a annat vara att distribuera programmet till server eller molntjänst.
Hur?
Man kan göra antingen manuell eller automatiserad deploy. Automatiserad gör att processen är mer konsekvent. Man kan använda sig av verktyg som bl a Continuous Integration/Continuous Deployment (CI/CD).
Under processen så gör man även databaskopplingar och andra konfigurationer så att applikationen kan köras på rätt sätt.
Staging är en testmiljö, eller som man kanske kan räkna ut av namnet, en stagead version av produktionsmiljön. Det är med riktiga data och scenarier som applikationen testas under staging, detta för att upptäcka fel och problem som kan uppstå.
Man kan utföra flera olika tester, t ex inom belastning, funktioner, säkerhet och integration.
Stagingmiljön är fysisk eller virtuell, men dock isolerad från produktionsmiljön. Detta för att man ska kunna testa och felsöka utan att påverka sin verksamhetet eller sina användare. Det minimerar också risken för att ofärdig kod kommer ut i produktion.
Varför?
Man gör deploy och staging för att se om programmer fungerar felfritt, som man väntat sig, eller för att se om prestandan är som man väntat sig. Och det ger tillfälle att upptäcka ev buggar. Detta för att när programmet väl sätts i produktion så ska det vara i felfritt, i den mån det går.

## PG 1.5 Debugging
Vad?
En bugg är fel eller problem i ett program. Det kan vara ett error-meddelande, en krasch, felaktig utdata eller annat oönskat. Debugging är processen att identifiera, analysera och korrigera dessa fel.
Hur?
Först måste felet identifieras. Det kan uppkomma på flera olika sätt, förhoppningsvis innan produktion, men t ex feedback från användare, rapporter från arbetsteamet etc.
För att hitta felet så läser man loggar med vad som gjorts när felet uppstod, felmeddelanden eller tester. På detta sätt kan man identifiera vad som lett upp till felet, vilka funktioner eller parametrar som skapar det, och därmed isolera det från resterande kod som faktiskt fungerar.
Under debugging-processen så spårar man koden i realtid och försöker identifiera orsaken till problemet. Man lägger ut breakpoints, det vill säga brytpunkten där koden stannar av så man kan analysera det som precis skett och vad kommande steg kommer att bli. Dessa kan läggas vid t ex radnummer eller funktioner. Man inspekterar värden på variabler, och kontrollerar stacktracet, det vill säga, en lista över anropade funktioner och i vilken ordning dom kommer, även om dom är inbäddade.
Man kan lättare övervaka och hitta fel om man avgränsar koden i breakpoints och sedan kör steg för steg, rad för rad. 
Efter att felet hittats, så åtgärdas det, dokumenteras och följs upp, som det mesta bör göras.
Varför?
Debugging och debugging-verktyg används för att snabbt och effektivt lösa problem. Det är speciellt användbart vid komplexa fel som är svåra att hitta, eller om programmet har ett oväntat beteende.

## PG 1.6 Dokumentation
Vad?
Hur?
Varför?
Dokumentation i kod kan vara olika saker. Det kan vara del kommentarer i koden för att beskriva funktioner och vad som är avsikten med den. Detta för att andra utvecklare ska kunna arbeta på samma projekt och inte behöva undersöka hela projektet för att förstå vad som ligger vart och varför. Det kan även vara bra för en själv att snabbt kunna se vad som gör vad i ens eget program om man behöver göra justeringar. Så slipper man gå igenom hela sidan.
Annan dokumentation som jag nämnt tidigare är vid ändringar av koden. Om man släpper nya versioner av sin applikation pga ändringar, så är det bra att dels berätta utåt för användare vad som är ändrat och dels internt där man noggrant kan dokumentera tidigare fel och buggar så man har det inför eventuella kommande fel.
Jag har även råkat på dokumentation när vi arbetat med APIer. Detta för att jag som användare ska kunna se hur deras struktur är utformad, så jag vet hur jag ska skriva koden som hämtar rätt parametrar. 
Dokumentation inom programmering är viktigt, och den bör vara anpassad efter målgruppen. Kunder, användare, andra programmerare etc.
Den bör vara tydlig så det inte uppstår frågetecken. Utöver att det skapar bra förutsättningar för samarbete programmerare emellan, så bidrar den även till att spara tid vid eventuella fel och till att kunna återanvända koden i andra sammanhang.
Dokumentation innebär också en bra README-fil så man vet vilket syfte projektet har, hur man använder det, och vilka funktioner som finns.


## PG 1.7 Struktur av kod i projekt
Vad?
Struktur av kod i projekt är hur man organiserar hur koden skrivs. Vad skrivs i vilka filer, vad bör ligga i samma mapp, vad bör ligga i en annan mapp. Bör man dela upp funktioner och variabler och annat för sig, eller bör man följa programmets gång i koden.
Hur?
Det är bra att dela upp koden så att man kan återanvända den. Till exempel, om man har funktioner som går att använda på flera ställen så kan man extrahera den och importera till de ställen där de behövs. Det samma med till exempel design, då är sass väldigt bra att använda, då man förkortar processen att bygga saker som ska se likadana ut (t ex bakgrunder eller knappar).
Man bör även separera kod som gör olika saker. Frontend- och backend-kod bör finnas i olika mappar. Databaskoppling bör även finnas separerat från dom. Det är också viktigt att namnge filer och mappar så det går att förstå för utomstående vart man hittar de olika delarna. Mappstrukturen bör vara hierarkisk och enligt funktionsområden.
Moduler bör man även definiera och skriva separat och sedan importera till de filer de ska användas. 
Här har vi dokumentation igen, det är viktigt att kommentera sin kod och även skriva README så man vet vad projektets syfte är, vilken funktionalitet som finns, och hur man använder sig av applikationen.
Varför?
Strukturen beror på projektets storlek, men det ska oavsett vara enkelt att navigera i det. Det är viktigt att följa de standarder som finns, så programmet är översiktligt för andra programmerare, eller för att enkelt kunna åtgärda problem.
Det finns olika standarder, dels för olika språk (https://www.php-fig.org/psr/psr-12/) och dels för kvaliteter på mjukvara (ISO/IEC 9126: ISO/IEC 9126 ).

## PG 1.8 Automatisering av arbetsflöde
Vad?
Via byggverkyg kan man automatiskt bl a  kompilera källkod, och distribuera till testmiljö (typ deployment).
Man kan också använda sig av automatiserade tester och generera rapporter av testresultatet. Det sparar mycket tid än om man skulle felsöka efter t ex buggar på manuellt sätt. Den automatiserade testningen ser också vart exakt det blir fel i koden om det finns en bugg.
Man kan även automatisera genom att använda program som skapar genererad kod, speciellt nu när AI har börjat distribueras.
Man kan dessutom göra egna boilerplates eller filer, eller kodmönster att spara för att automatisera delar av kodskrivandet.
Även Git är ett automatiserat verktyg, på så sätt att det integrerar koden automatiskt och man kan använda sig av olika branches och forks.
Hur?
Genom att t ex använda byggverktyg som CI/CD, Continuous Integration /Continuous Deployment. Där automatiseras hanteringen av kod, på så sätt att koden som skrivs automatiskt integreras med projektet (gemensamma kodbasen), och när de nya ändringarna blivit automatiskt godkända så deployas de. På så sätt sker integration och testning kontinuerligt.
Varför?
För att effektivisera arbete och även minska risken för fel, så som stavfel och annat som orsakas av mänskliga faktorn. 
Dock finns det ju vissa arbetsflöden som är för komplexa för att kunna bli automatiserade. Dessutom behövs även automatiserade verktyg och koder övervakas och uppdateras. Plus att det behövs tid för att lära sig hantera dessa verktyg och kunna hantera dom, så investering av tid och pengar behövs initialt. Så det finns både bra och dåliga saker.

## PG 1.9 Virtualisering av utvecklingsmiljö
Hur?
Istället för att använda en fysisk dator som server, så kan man använda virtuella maskiner eller containrar som simulerar server för samma resultat.
Vad?
En virtuell maskin (VM) är en efterliknelse av en komplett dator. Den inkluderar simulering av bl a operativsystem (från flera distributörer) och hårdvara (inklusive processor, minne och andra enheter). Den körs på en fysisk dator och det går att köra flera VM samtidigt på en dator.
När man använder containrar så måste man definiera en konfigurationsfil, i Docker så kallas det för Dockerfil. Där bestäms vilka komponenter som ska finnas i containern. I den kan man köra sin applikation. Containerteknik är bra för att dom är oberoende av plattform, alltså blir det samma resultat oavsett vilken dator man sitter vid.
Varför?
Med virtuella maskiner så kan man efterlikna olika operativsystem och konfigurationer. Det gör att man kan arbeta på en dator men simulera att man jobbar på en helt annan.
I containrar så virtualiserar man applikationen istället för hela operativsystemet.
Genom att använda dessa metoder så kan t ex ett team på en arbetsplats jobba i exakt likadan miljö, oavsett dator. Det eliminerar risken för problem som kan uppstå pga olika plattformar.
Man kan dessutom byta utvecklingsmiljö snabbt efter behov. 
De ger dessutom bra portabilitet, de finns allt tillgängliga i datorn, enkelt samarbete då man kan dela utvecklingsmiljöer och resurserna effektiviseras på arbetsplatsen då flera virtuella maskiner kan finnas på en och samma dator.

## PG 1.10 Bundeling-verktyg
Vad?
Som man kanske hör på namnet, så är bundeling-verktyg de verktyg som används för att bunta ihop filer. Om du har flera olika moduler som var och en ska göra en nätverksförfrågan för att ladda din applikation, så buntas de istället ihop och skickar  en enda, eller åtminstone mycket färre. De minskar också i storlek då verktyget komprimerar och tar bort oanvänd kod. Det resulterar i slutändan i att applikationen laddar snabbare.
Eftersom filerna är mindre så minskar även överföringstiden och i slutändan blir det en bättre upplevelser för användaren.
Hur?
Man använder sig av verktyg, så som webpack. Man installerar webpack genom kommandot ’npm install webpack –save-dev’. Då genereras en konfigurationsfil, ’webpack.config.js’ och där får man specificera bl a filerna som ska matas in och matas ut. När man sen skriver webpack i terminalen så byggs applikationen och genererar filerna som man tidigare hänvisat.
Många verktyg vet redan på förhand vilka filer som ska importeras och exporteras och vet hur de är beroende av varandra.
Varför?
Då man som utvecklare kanske vill strukturera sin kod i olika filer för att göra det översiktligt, så kanske man vill ha flera olika filer och mappar med beskrivande titlar, så man vet vad som finns vart i projektet. Då är det bra att använda bundeling, så det inte tar lång tid att ladda och skickar flera nätverksförfrågningar och saktar ner applikationen avsevärt.

## PG 1.11 Terminalinterface
Vad?
Terminalinterfacet är terminalen vi arbetar med. Men då kärt barn har många namn så kallas den även command prompt och CLI (Command Line Interface). Det är ett sätt att interagera med datorn via korta kommandon. Man skriver in sitt kommando i terminalen och trycker enter för att köra/exekvera. Kommandotolken tolkar sedan och programmet utför aktionen. Det finns olika kommandotolkar, jag själv har PowerShell, git bash och developer command prompt for visual studio.
Hur?
Det finns många vanliga och oerhört nödvändiga kommandon. Man kan navigera i sitt eget projekts filsystem genom cd = change directory, och sedan skriva / och namn på fil eller mapp för att gå framåt, eller .. för att gå bakåt.
Om du vill lista alla filer i en mapp så skriver du ls, och om du vill visa även dolda filer så skriver du ls -a.
Varför?
Terminalen automatiserar uppgifter som att skapa och ändra i databas, skapa filer, programkörning, starta servrar, kompilera kod etc. Det sparar mycket tid för utvecklare. Man kan även använda Git genom terminalen, och därmed utföra många aktioner till sitt fjärr-repository.
Det är ett mycket effektivt verktyg i en utvecklingsmiljö.

