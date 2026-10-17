---
title: Příručka
updated: 2026-10-17
---

## Tři tvary a nic jiného

Jsou tu tři druhy repozitáře a nic jiného. Aplikace drží backend, frontend, kód, který oba sdílejí, své spustitelné soubory a typy. Balíček drží svůj zdrojový kód, spustitelné ověřovací skripty a bránu, která proběhne před zveřejněním. Textový repozitář drží dokumenty, na kterých se musí shodnout víc repozitářů, jednu složku na dokument a jeden soubor na jazyk, bez vlastního buildu.

Každý druh má jedno rozvržení a to rozvržení je v každém repozitáři toho druhu stejné. Text, který čte jen jeden repozitář, v něm zůstává; textový repozitář vzniká ve chvíli, kdy dva potřebují stejná slova.

## Napsané člověkem, nebo postavené buildem

Zdrojový kód drží kód a text, který napsal člověk. Cokoli, co build stáhne, odvodí nebo vykreslí, je artefakt: snímek vzdáleného rozhraní, soubor s kurzy, předrenderovaná stránka. Artefakty se při každém běhu zapisují do výstupu buildu a nikdy se necommitují.

Repozitář, který drží generovaný soubor ve zdrojovém kódu, je vadný, a je vadný i tehdy, když je ten soubor malý, když se mění jednou za rok a když by s ním byl build rychlejší. Aplikace čte generovaná data stejně jako kterýkoli jiný vstup buildu, nikdy jako import ze zdrojového stromu.

## Jak se čte commit a vydání

Zpráva u commitu je předmět a většinou nic víc: rozkazovací způsob, bez koncové tečky, do dvaasedmdesáti znaků, popisuje chování, které se změnilo, ne soubory, kterých se to dotklo. Žádné prefixy typu, žádné rozsahy. Commit, který potřebuje dvakrát slovo „a“, jsou dva commity.

Zvýšení verze je vlastní commit, jeho předmět pojmenuje vydání a co se v něm změnilo, a anotovaný tag nese tutéž větu. Nejdřív se pushne commit a až potom tag, protože tag, který dorazí první, neukazuje na nic. Zveřejněný tag se nikdy nepřesouvá ani nemaže; chyba se opravuje další verzí.

## Čí jméno na tom stojí

Každý commit, tag, vydání i zveřejněný balíček nese jméno člověka, který tu práci udělal. AI se používá tak, jako se používá překladač nebo editor, jako nástroj v rukou někoho, kdo za výsledek dál odpovídá, a nikdy nevystupuje jako autor, protože model nemůže za nic odpovídat.

Nepředává se nic, co vývojář nepřečetl, nepochopil a není připravený obhájit. To je celé pravidlo a právě proto jméno u commitu něco znamená.
