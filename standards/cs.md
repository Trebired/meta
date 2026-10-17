---
title: Standardy
updated: 2026-10-17
---

## Čím musí projít každá změna

Typy sedí bez chyby, nástroj na kázeň schválí tvar kódu, proběhnou ověřovací skripty a celek se sestaví. Změna, která některou z těch věcí neprojde, se nemerguje a nevydá. Ta brána je program, ne recenzent v dobré náladě.

Nástroj na kázeň vynucuje to, v čem je revize slabá: délku souborů, délku funkcí, délku řádků, mrtvé komentáře, cesty importů a to, kam co smí patřit. Odmítne commit, místo aby nepořádek nechal na potom.

## Jaký ten software musí být

Open source, pod MIT nebo AGPL, bez zadrženého jádra. Software pro počítače běží na Linuxu. Cokoli stavěného pro prohlížeč funguje všude, kde je prohlížeč.

Aplikace běží pod tvrdým stropem 500 MB obsazené paměti a míří na 200 MB, měřeno při skutečném používání, ne po čerstvém startu naprázdno. Jediná výjimka je grafika a i ta uvádí vlastní číslo, místo aby byla zproštěná povinnosti nějaké mít.

## Na co má čtenář nárok

Každý web i každé rozhraní, které vydáme, drží WCAG 2.2 AA: ovladatelné jen klávesnicí, čitelné odečítačem obrazovky, použitelné při 200% velikosti textu a poctivé k omezenému pohybu. Stránka o přístupnosti říká, co to pokrývá a co ne.

Žádné sledování, žádná analytika, žádné profilování chování a žádná třetí strana, která by čtenáře pozorovala na čemkoli, co organizace provozuje.

## Co se stane, když to něco neprojde

Opraví se příčina. Hranice, která se posune pokaždé, když se to nehodí, nikdy žádná hranice nebyla, takže překročená paměť se řeší v příčině, ne zvednutím stropu, a pravidlo se nikdy nevypíná kvůli tomu, aby prošel commit.

Když se ukáže, že je standard špatně, mění se veřejně a písemně a všechno už vydané se k němu dotáhne. Je to pomalejší než výjimka a je to jediná verze, která vydrží.
