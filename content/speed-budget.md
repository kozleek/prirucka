# Rychlostní limity. A proč nedělat „optimalizace“?

Rychlostní limit je metrika, která říká, jaké maximální hodnoty parametrů rychlosti mají mít vaše vstupní stránky. V anglických textech se mluví o „Speed Budgetu“ nebo „Performance Budgetu“.


## Jak na nastavení rychlostních limitů? 

Rychlostní limity si vložte do tabulky. Kolegům nebo externímu dodavateli pak dejte za úkol jejich dosažení.

### 1) Vyberte důležité vstupní stránky

Rychlost je zásadní hlavně u stránek, na které lidé chodí z marketingových kanálů. U e-shopů to bude šablona detailu produktu a jejich seznam. Možná homepage. Málo důležité stránky řešit nemusíte.

### 2) Vyberte, jaké parametry budete hodnotit

WebpageTest.org. Testoval bych na něm. Nejdůležitější hodnota je *Speed Index*. Další pak *Load Time*, *First Byte*. V textu o nástrojích se dozvíte více.

### 3) Otestujte parametry nejbližších konkurentů 
  
Seznam konkurentů už nejspíš máte. Ale pokud ne, rychle to napravte. Uložte si je do tabulky i s hodnotami u konkurentů a nastavte si cílové metriky tak, aby byly alespoň o 20 % lepší než u nejrychlejšího webu konkurence. O sestavování Speed Budgetu pěkně píše Daniel Mall v článku „How To Make A Performance Budget“. [vrdl.in/perfbudget](http://danielmall.com/articles/how-to-make-a-performance-budget/)

Pak už to vše stačí jen zrealizovat, že? 



## Optimalizace vs. kultura rychlosti

Nemám rád slovo „optimalizace“. Abyste totiž něco mohli „optimalizovat“, musíte to předtím pokazit. 

Pokud na rychlost nemyslíte už v úvodních fázích práce na projektu, bude „optimalizace“ náročná. Když ji má projekt v DNA, je to ve výsledku jednodušší.

Stanovení rychlostních limitů velmi pomůže. Všechny nové vlastnosti, které různí členové týmu běžně do projektů přidávají, se zvažují i pod úhlem limitů. 

> Klient: „Že bychom na houmpejdž dali automaticky pouštěné videjko přes celou stránku?“ 
> Designér: „OK, ale překročí vám to rychlostní limit. Šestnáctkrát.“  

Je důležité, aby vývojáři byli přítomní už v oné přípravné fázi projektu. Alespoň pro konzultace, ale ideálně i s možností zůčastnit se přípravy prototypů. Webový projekt je stejně technický jako designérský. Designéři a marketéři obvykle neznají technická specifika komponent zvažovaných k implementaci. Vývojáři jim rádi připraví testy. 

Kontrola dodržování rychlostních limitů by se měla provádět nejen během práce na webu, ale také po každé větší aktualizaci. Dá se to naštěstí zautomatizovat. Buď nějakým vlastním nástrojem, který vytáhne data z analyzátorů, o nichž mluvím v dalším textu, nebo třeba pomocí specializované nástroje Speed Curve. [speedcurve.com](https://speedcurve.com/)

Pojďme si teď ukázat nástroje pro analýzu rychlosti.

