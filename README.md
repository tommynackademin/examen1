#ReadMe

Innehållsförteckning.

1. Syfte

2. Förutsättningar

3. Instruktion för deploy via Azure

4. Konfiguration av Accessibility-Test.yml



1. Syfte
 
Detta repo syftar till att exemplifiera och beskriva processen för deploy av en webb
app samt tillhörande automatiserade tillgänglighetstest i enlighet med avtalat projektdirektiv.

2. Förutsättningar

För att ha möjlighet till att använda Repot så behöver användaren ha registrerade användare och tillgång till ett flertal verktyg. Dessa inlkluderar:
    - Installerat GIT med tillhörande Konfigurerad Git-användare
    - Installerad Kodredigerare med tillhörande Github extension
    - En Aktiverad Personal Access Tokens för github (https://Github.com)
    - Upprättat konto via Microsoft Azure (https://azure.microsoft.com)
    - Tillgång till en aktiv Wave api-nyckel med krediter (https://wave.webaim.org/)
    - Kodbas - repo med minst en Index.html fil i /public
    - Länkat Personal Access Token till en GitHub Secret för Repositoryn
   
3.Instruktion för deploy via Azure

Logga på på Azure och klicka på "Ny resurs". Välj Static Webb App, konfigurera server paket och plats efter behov. Under distributionsinformation,
välj källa "GitHub", akutellt GitHub konto samt Repository för kodbas. Under "Gren" Välj Root eller "/". Bekräfta att Index.html liiger i /public.
Klicka på "Skapa resurs". Webb-appen deployas nu samt GitHub repositoryn uppdateras med ett CI/CD workflow mot Azure.

4. Konfiguration av Accessibility-Test.yml

Rad 11, ändra "secrets.test1" till motsvarande registerad secret. Om secret heter t.ex. nyckel1 så ska det stå "secrets.nyckel".
Rad 16, ändra endpoint: Lägg in personlig Wave api-nyckel för "key="kopiera in nyckel här". Ändra URL till webb-resursens url given av Azure. "url="kopiera in webb appens url här"
Rad 21, ändra Acess token till motsvarande GitHub secret i repositoryn.
Rad 22, ändra Branch efter egen preferens, ändra absolut ej till main!!!




