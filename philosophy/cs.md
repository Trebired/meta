---
title: Filozofie
updated: 2026-10-13
---

## Proč je všechno veřejné

### Jsme postradatelní

Nikdo v téhle organizaci není vzácný. Stavět software je naučená dovednost, kterou umí velké množství lidí, a každého z nás může nahradit někdo, kdo to udělá stejně dobře nebo líp. S organizací je to stejné. Trebired existuje proto, že několik rozhodnutí dopadlo takhle a ne jinak, a stejným způsobem jednou existovat přestane.

Říkáme to přímo, protože opačné přesvědčení je jediná věc, na které stavět odmítáme. Organizace, která bere vlastní trvání jako smysl své existence, se začne chránit. Drží kód zavřený, aby odchod něco stál, váže software na službu, kterou umí provozovat jen ona, a z lidí, kteří ji potřebují, dělá lidi závislé na tom, jestli přežije. Je to rozumný způsob, jak zůstat naživu. Taky to znamená, že v den, kdy organizace skončí, skončí s ní všechno, co udělala.

### Práce nás může přežít

Zdrojový kód je jedna z mála věcí, které člověk udělá a které nemají přirozený konec. Neopotřebuje se, kopírovat ho nic nestojí a kdokoli, kdo na něj narazí, ho může číst, opravit i rozšířit, za rok i za sto let. Zveřejněný je nezávislý na tom, kdo ho napsal. Zavřený má přesně takovou životnost jako organizace, která drží heslo.

Proto zveřejňujeme všechno. Každý produkt, každý balíček i každý nástroj, který jsme na jejich stavbu napsali, pod AGPL nebo MIT, ve veřejných repozitářích, bez zadrženého jádra a bez placené verze, která odemyká to, co jsme si nechali. Když Trebired zítra skončí, nebude se tu nic zachraňovat, protože nic nikdy nebylo zamčené. Licence práva uděluje už teď a kód už teď leží na discích jiných lidí.

### Pro lidi, které nikdy nepotkáme

Není to velkorysost ani marketingová pozice. Plyne to z předchozích dvou částí. Jestli jsme postradatelní my a práce ne, pak jediné poctivé, co se s tou prací dá udělat, je dát ji tam, kam naše zmizení nedosáhne.

Co s ní kdo udělá potom, není na nás. Může ji provozovat, forknout, učit se z ní nebo ji vzít někam, kde nás to nenapadlo, aniž by se nás ptal a aniž by nám cokoli dlužil. O to přesně jde. Radši po sobě necháme něco, co je dál k užitku, než organizaci, která si dávala pozor, aby zůstala potřebná.

## Pro jaké stroje stavíme

### Operační systém má být nudný

Operační systém dělá tu nejzákladnější práci v celé výpočetní technice. Nastartuje stroj, přenáší data mezi programy a pak jde z cesty. Nic na téhle práci nevyžaduje tajemství a nic na ní nestojí za to, aby kvůli ní firma sledovala miliardu lidí.

Windows si tajemství přesto drží. Nikdo mimo firmu, která je prodává, si nemůže přečíst, co dělají, opravit, co dělají špatně, ani ověřit jediné tvrzení, které o nich zazní. K tomu hlásí, co jejich uživatelé dělají, zpátky té samé firmě, za podmínek, které uživatel nepsal a nemůže si je prohlédnout. Není to chyba jinak dobrého systému. Je to to, k čemu ten systém slouží.

### Takže pro ně nestavíme

Software pro počítače z téhle organizace běží na Linuxu. Windows na seznamu nejsou a nepřibydou, stejně jako macOS. Není to o námaze ani o tom, kolik lidí je používá. Dodávat software na zavřenou platformu by znamenalo přijmout její podmínky za každého, kdo naši práci používá, a pak svůj vlastní kód nazývat otevřeným.

Cokoli, co stavíme pro prohlížeč, funguje všude, kde je prohlížeč, tedy i na Windows a na Macu. Čára vede u softwaru, který píšeme přímo pro stroj, protože tam má platforma právo mluvit do toho, čemu je uživatel vystavený.

### Čekáme, že skončí

Windows běží skoro všude a právě tohle nám přijde upřímně smutné. Jsou tam kvůli předinstalacím, nákupním smlouvám a zvyku, ne proto, že by je někdo porovnal s alternativami a vybral si je.

Drží je jediná věc a není to kvalita. Je to kompatibilita: programy, které lidé potřebují, vznikly pro Windows, protože Windows jim někdo prodal, a lidé u Windows zůstávají, protože tam ty programy jsou. Odložte ten kruh stranou, podívejte se na ten systém samotný a zbyde toho k obhajobě velmi málo. Všechno pod ním, jádro, souborové systémy, sítě i stroje, na kterých internet opravdu běží, je dávno udělané otevřeně, víc lidmi a na světle. Zbývá spotřebitelský zvyk s připojenou telemetrií, a zvyk je nahraditelný.

Myslíme si proto, že by přežít neměly, a nemyslíme si, že přežijí. Linux dávno běží na serverech, v sítích i v telefonech, které lidé nosí v kapse; stolní počítač je poslední místo, které nezabral, a každý rok je blíž. Stavíme pro ten stolní počítač schválně, a ne pro ten, o kterém čekáme, že zmizí.

## V čem to píšeme

### Nejdřív to má přečíst překladač

Každý program se čte dvakrát: jednou ho čte stroj, který ho spustí, a jednou člověk, který ho za rok bude měnit. Čistý JavaScript nechává práci toho stroje na tom člověku. V souboru nestojí, co která hodnota je, co funkce potřebuje ani co vrací, takže jediný způsob, jak to zjistit, je spustit to a dívat se. Na něco malého to stačí. Udržet tím něco naživu nejde.

Všechno proto píšeme v TypeScriptu a typ bereme jako větu, kterou další čtenář dostane zadarmo. Je to jediná dokumentace, která nemůže potichu zestárnout, protože ve chvíli, kdy začne lhát, se program přestane překládat. Překladač si celou věc přečte dřív než kdokoli jiný a odmítne ji v jediném okamžiku, kdy je odmítnutí levné.

Tohle je obecný případ a platí pro většinu toho, co software dělá: čeká na disk, na síť nebo na člověka, a tam rozhoduje srozumitelnost, ne rychlost. Po něčem jiném saháme jen tam, kde je limitem sám stroj.

### Rust tam, kde je limitem stroj

Některá práce nečeká na nic. Mezi člověkem a výsledkem nestojí nic než to, kolik toho musí procesor udělat a kolik si u toho musí držet v paměti. Vykreslování, tisk, zpracování velkých souborů, horké místo uvnitř dlouho běžící služby: tam přestává být jazyk otázkou vkusu.

Tyhle části píšeme v Rustu. Ne kvůli módě a ne proto, že by si ho zasloužil každý program, ale protože je to jediná volba, která dává rychlost C bez té rodiny chyb, kvůli kterým bylo C nebezpečné. Uvolněná paměť se znovu přečíst nedá a souběh, kterého si autor nevšiml, je většinou chyba při překladu, a ne hlášení od zákazníka za půl roku.

Pravidlo, které na sebe klademe, je úzké. Rust tam, kde se vyplatí, v částech, které jsme změřili a nestačily, a všude jinde ten jednodušší jazyk. Vybrat si těžší jazyk na práci, která ho nepotřebuje, není důslednost, ale ozdoba.

### Go tam, kde program musí přistát na cizím stroji

Malá část toho, co děláme, musí běžet tam, kam nevidíme: runner na buildovacím stroji, pomocný program vedle služby. Užitečná otázka tam není, jak je jazyk výmluvný. Je to otázka, co musí člověk na druhé straně nainstalovat, než se náš program vůbec spustí.

Na to odpovídá Go líp než cokoli jiného, co používáme. Jedna statická binárka, žádné běhové prostředí, které musí být na stroji první, žádná verze, na které je potřeba se shodnout. Zkopíruje se a běží. Používáme ho přesně na tohle a na nic jiného.

### Rozhraní je udělané z času někoho jiného

Obrazovka je místo, kde se naše rozhodnutí mění v něčí odpoledne. Každý ovládací prvek, který lže o tom, co udělá, každé okno, které vyskočí bez důvodu, i každá vteřina čekání se berou člověku, který s tím nesouhlasil.

Na linuxovém počítači stavíme v Qt a QML, v sadě nástrojů, ze které je udělané celé to prostředí. Aplikace, která používá ovládání, klávesové zkratky a dialogy systému, po uživateli nechce, aby se učil cokoli nového: chová se jako všechno ostatní na tom stroji. Na webu používáme React, protože prohlížeč má model, který už udržují miliony lidí a my nemáme co lepšího nabídnout, a vrstvu nad ním si držíme vlastní, aby to naše zůstalo naše.

## Co smí software stát

### Program je na stroji host

Počítač patří tomu, kdo ho používá. Paměť, kterou si náš software drží, je paměť, kterou nemůže mít jeho ostatní práce, a procesor zaměstnaný námi je procesor, který nedělá to, kvůli čemu si člověk sedl. Brát cizí stroj jako svůj a zaplnit ho je tichá neslušnost, do které se většina softwaru usadila.

Proto na to máme číslo. Aplikace z téhle organizace běží pod tvrdým stropem 500 MB obsazené paměti, míří na 200 MB a míň a měří se při skutečném používání, ne po čerstvém startu naprázdno. Jediná výjimka je grafika, a i ta uvádí vlastní číslo, místo aby byla zproštěná povinnosti nějaké mít.

Když to něco překročí, opravuje se příčina. Strop nezvedáme, protože strop není ten problém, a hranice, která se posune pokaždé, když se to nehodí, nikdy žádná hranice nebyla.

### Čekání je cena, kterou nikdo nezapíše

Nikdo softwaru nepoděkuje za to, že je rychlý, a přesně proto se obětuje jako první. Každý jednotlivý ústupek se dá obhájit, celek ne, a končí to strojem, který je mnohonásobně rychlejší než ten předchozí a běží na něm software, který působí pomaleji.

Rychlost a velikost proto bereme jako součást toho, jestli věc vůbec funguje, ne jako pozdější optimalizaci. Produkt, který je správný a nepoužitelný, není hotový.

## Proč si nástroje stavíme sami

### Závislost je slib, který drží někdo jiný

Všechno, na čem produkt stojí, je rozhodnutí, které může někdo jiný změnit, opustit, přejmenovat nebo prodat. Není to argument pro to psát si všechno sám, na čemž se malé organizace utopí. Je to argument pro to vědět přesně, které sliby vás drží, a mít ty důležité na dosah.

Vrstva přímo pod našimi produkty je proto naše: frontendový framework, bundler, logování, překlady i kázeň, která hlídá tvar kódu. Když je v téhle vrstvě něco špatně, opravíme to týž den, místo abychom založili hlášení a čekali. Když je dobře, vydáme to pod MIT nebo AGPL, aby naše nikdy neznamenalo zavřené.

### Pokaždé stejný tvar

Každý repozitář tady má stejné rozvržení, stejné nástroje a stejná pravidla, a hlídá to nástroj, ne něčí paměť. Délka souborů, mrtvé komentáře, cesty importů, kam co smí patřit: všechno se vynucuje, na každém projektu, i na těch, na které se nikdo nedívá.

Není to pořádek pro pořádek. Je to to, díky čemu může kdokoli otevřít kterýkoli repozitář téhle organizace a vědět, kam se dívat, a díky čemu práci přežijí i lidé, kteří u jejího vzniku nebyli. Kód, ve kterém se vyzná jenom jeho autor, je už napůl zavřený, ať má v licenci cokoli.

## Jak práce vzniká

### Stroj umí napsat řádek, odpovídat za něj neumí

AI používáme stejně jako překladač, editor nebo vyhledávač: jako nástroj v ruce člověka, který za výsledek odpovídá. Navrhuje, píše první verze, často se mýlí, a nic z toho neposouvá odpovědnost jinam. Odsud neodejde nic, co vývojář nepřečetl, nepochopil a není připravený obhájit.

Autorství se proto nehýbe. Commity, vydání i odevzdaná práce nesou jméno člověka, který je udělal, nikdy jméno modelu, protože jméno na práci je tvrzení o tom, kdo za ni ručí. Model neručí za nic. Napsat tam jeho jméno by byla lež přesně v té jediné věci, kvůli které se podpis píše.

### Žádný obrázek z AI, nikde

Nepoužíváme AI na věci, které předáváme. Žádná vygenerovaná loga, žádné vygenerované ilustrace, žádné vygenerované fotky, žádné vygenerované značky ani ikony. Obrázek z AI nenajdete nikde v téhle organizaci, ani na tomhle webu, ani v produktu, ani v práci odevzdané klientovi, a nenajdete ho tam ani později.

### Značka je rozhodnutí, ne průměr

Logo je rozhodnutí o tom, kdo někdo je, a obrázek je rozhodnutí o tom, co ukazuje světu. Model ani jedno rozhodnout nemůže, protože nemá komu skládat účty; zprůměruje, co nakreslili jiní, a vrátí něco, co se podobá všemu a nepatří ničemu.

Tak to kreslíme sami, pomaleji, a za každou čáru odpovídáme. Je to řemeslo a práce je hotová, když je správně, ne když je rychle.
