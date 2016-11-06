# Atomický design a Pattern Lab: návrat do budoucnosti návrhu uživatelských rozhraní

> We’re not designing pages, we’re designing systems of components. 
— Stephen Hay

[Pattern Lab](http://patternlab.io/) je nástroj pro návrh, testování a prezentaci atomických designových systémů. 

Používám jej na aktuálním projektu a mám takový pocit, že jinak už větší weby dělat nechci. V tomhle textu budu vysvětlovat proč.

Nejprve si ale musíme povědět něco o systémech designu. 


## Designové systémy

Myslím to, co asi znáte pod pojmy *style guide* nebo *pattern library*. Neznáte? Je to jako by jste si udělali pro větší projekt vlastní knihovnu odpovídající typu Bootstrap. Chcete lepší vysvětlení? Podívejte se na přednášku:

<p class="video">
Video: <a href="https://www.youtube.com/watch?v=FvTzAwebUjQ">Úvod do Style Guides</a> – Martin Staněk o „style guides“, dokumentacích k systémům designu.
</p>

Budu se tady odkazovat na svůj aktuální projekt – přípravu systému atomického designu pro nový [Webmium Eshop](http://www.webmium.cz/eshopy).

![Webmium - systém atomického designu](dist/images/original/atomicky-design-webmium.jpg)

Systémy jsou super:

- usnadňují dodržování jednotnosti designu
- zmenšují a zpřehledňují kód
- podporují iterativní vývoj po malých kouscích
- usnadní testování 
- díky dokumentaci i komunikaci v týmu a zaučení nových lidí 

Designové systémy prostě šetří čas a peníze.

Není těch názvů nějak moc? Style guides, systémy komponent, vlastní Bootstrapy, UI knihovny, knihovny návrhových vzorů, CSS frameworky… Ano, narážím na hlavní nevýhodu design systémů – zatím mají děsně moc názvů a variant. Já si je všechny vložil do kategorie *systémy webového designu*. 

Ať tomu budeme říkat jakkoliv, webdesign jde z mého pohledu jasně tímhle směrem. Podívejte se třeba na tenhle rozcestník: [styleguides.io](http://styleguides.io/).

No a tím se dostáváme k Atomic Designu, jednomu z nejnadějnějších myšlenkových frameworků pro tvorbu systémů pro webový design.

## Atomický design 

[Atomic Design](http://bradfrost.com/blog/post/atomic-web-design/). Proč zrovna do něj vkládám takovou naději? Protože za ním stojí chlapík jménem Brad Frost. Nic vám to neříká? [Jeho blog](http://bradfrost.com/blog/) jsme možná někdy viděli. 

Brad je velká hvězda dnešního frontend designu, která má díky úspěšným [přednáškám](http://bradfrost.com/speaking/) vliv. A teď navíc o atomickém designu [píše knížku](http://atomicdesign.bradfrost.com/). 

Já vím, sázet při výběru nástroje na jméno tvůrce není stoprocentně spolehlivé. Brad ale v tuhle chvíli nemá konkurenci a ta knížka to pojistí, uvidíte.

![Atomic Design](dist/images/original/atomic-design.jpg)

Skrze framework atomického designu Frost přišel s tříděním prvků na stránce do úrovní vycházejících celkem chytře z chemické terminologie. Vezměme to i s příklady z našeho eshopu:

1. Atomy (například tlačítko)
2. Molekuly (např. tlačítko s inputem spojené do vyhledávacího pole)
3. Organizmy (např. hlavička stránky)
4. Šablony (např. šablona detailu produktu)
5. Stránky (např. stránka konkrétního produktu)

### Není to zbytečně složité?

Neptáte se sami. Než jsem si atomickou organizaci zkusil na konkrétním projektu, všem okolo jsem říkal, že je to zbytečně složitá hierarchie a že běžné projekty si vystačí s jedno až dvouúrovňovou strukturou komponent. 

Než jsem si to zkusil na konkrétním projektu. 

Teď už mám vyzkoušeno a říkám, že je to kategorizace, která je pro obyčejné weby úplně dokonalá. Omlouvám se tedy všem atomům, molekulám, organizmům a své učitelce chemie na střední.

Hlavním důvodem pro zavedení designových systémů je — ušetření práce. 
Organizace komponent o méně úrovních, obvyklá na jiných mých projektech čas šetří, ale ne tak jako když z atomů skládáte molekuly a z molekul organizmy. Kód se pak opakuje výrazně méně a začne fungovat onen efekt skládání Lego kostek, tak hojně spojovaný se systémy webového designu.

Pokud by vám ale atomické dělení přestalo vyhovovat, kategorizaci si můžete sami změnit. Brad Frost k tomu vyloženě vybízí a ukazuje i příklady jiných organizací. Myslím, že to ale nebudete potřebovat.

<p class="video">
Video: <a href="https://www.youtube.com/watch?v=wgsHfAV-6Aw">Atomic Design v České televizi</a> – Zdeněk Lanc sdílí zkušenosti s předchozí verzí Pattern Labu při redesignu ČT24.
</p>

Tak, a teď si pojďme povídat o nástroji pro práci na atomických systémech.

## Pattern Lab: návrh, prezentace, ale hlavně testování atomického designu

Na začátek se musím přiznat, že [Pattern Lab](http://patternlab.io/) je pro mě zdrojem největšího nepochopení a frustrace — asi tak od doby co jsem se snažil ve Francii domluvit anglicky.

Pattern Lab totiž není:

- nástroj k prezentaci systému designu (jako [AtomicDocs](http://atomicdocs.io/)) 
- ani nástroj ke generování dokumentace k CSS (jako [KSS](http://warpspire.com/kss/) nebo [StyleDocco](https://jacobrask.github.io/styledocco/)). 

Je to nástroj pro *návrh*. Tedy spíše v kategorii Photoshop nebo Sketch. Jejda, to byla bolest, než jsem to pochopil. V obvyklých případech vás bude přidání Pattern Labu do vašeho designérského workflow stát určité úsilí. U mě to bylo snadné, protože asi víte, že jsem zblázněný do návrhu rozhraní [přímo v prohlížeči](http://www.vzhurudolu.cz/prednaska/design-webu-v-prohlizeci-149). 

Kromě návrhu ale dokáže *testovat*, ověřovat designérské hypotézy přímo v prohlížeči, v různých obsahových nebo uživatelských kontextech. To je, řekl bych, jeho hlavní silná stránka. Vy totiž dobře víte, že spíše turista z Francouze vytáhnete anglickou větu než vy ze svého Photoshopu či Sketche testovatelný prototyp. Tady je ta budoucnost, kterou zmiňuji v názvu textu.

Podobně jako výše uvedené nástroje pak Pattern Lab sice umí systém designu *prezentovat*, tedy ukazovat lidem mimo nejužší designérský tým. Neřekl bych, že tohle je ale jeho silná stránka. Protože je primárně testovací, má docela ošklivé výstupy. Nicméně má skvělou podporu pro generování jakékoliv dokumentace z materiálů co do něj nasázíte. Je to Markdown, Mustache šablony a nějaké CSS soubory. Udělat z toho cokoliv prezentovatelného v pohodě zvládnete.

<small markdown="1">
Užitečné odkazy k Pattern Lab:  
– [Ohromný článek na Smashing Magazine](https://www.smashingmagazine.com/2016/07/building-maintaining-atomic-design-systems-pattern-lab/).  
– [Demo Pattern Labu](http://demo.patternlab.io/). Zdrojáky jsou [na Githubu](https://github.com/pattern-lab/starterkit-mustache-demo).
</small>


### Testování na reálném obsahu

Nejdřív otázka pro designéry:

> Bylo dřív vejce nebo slepice? A obsah nebo design?

Asi budete souhlasit, že obsah a design spolu dost úzce souvisejí. Při práci na designu potřebujete obsah, to designéři vědí. Jenže ono je to někdy i naopak. Při testování designu potřebujete všechny varianty obsahu, včetně extrémních. To vědí zase frontend kodéři.

Pattern Lab nabízí úžasnou věc – vkládání reálného obsahu přímo do designu. Už ve fázi návrhu! Pokud obsah někde máte, necháte si ho nalít do JSON souboru a napojíte na něj Pattern Lab. Lusknutí prstem a v prohlížeči testujete víceméně reálný web. Nebo v našem případě více webů na jednom systému designu:

![Varianty Webmium](dist/images/original/atomicky-design-webmium-eshopy.jpg)


### Pseudošablony: testování variant obsahu

Další hezká věc a přitom žádná velká věda. Pattern Lab nabízí možnost vytvořit pseudošablony, varianty šablon s různým typem obsahu, různým rozložením atd. Prostě si všechny možnosti otestujete už přímo v design systému a ne až na běžícím webu.

### Pattern Lab není nutnost, ale…

Asi byste atomický systém dokázali implementovat bez Pattern Labu. Ale moc to nedoporučuji. Můžete ho navrhnout v Photoshopu, ale bude vám chybět možnost okamžitého otestování. Můžete ho zkusit napsat přímo v kódu, ale bude vám chybět nástroj pro snadný návrh a prezentaci.

Ale ani v případě mé práce pro Webmium není Pattern Lab jediný nástroj. Grafické materiály dostávám v běžných celostránkových souborech z Photoshopu. S grafikem máme docela soulad, takže můžu prohlásit, že i takhle může atomický systém vznikat. Jen musíte vědět, že to co poskládáte z atomického designu nebude perfektně sedět s pé-es-déčky. Nicméně doufám, že v pixel-perfect návrhy už dávno nevěříte.

## Zkusíte Pattern Lab a atomický design?

Určitě ho zkuste, pokud:

- děláte vlastní produkt nebo spravujete větší web: design systém dlouhodobě využijete a větší počáteční časová investice se vám vrátí;
- jste otevření změnám v pracovních postupech: designér i kodér musí velmi intenzivně spolupracovat a vyvíjet věci v malých iteracích.

Pattern Lab se naopak nehodí:

- do firem, kde rubete unikátní weby jako Baťa cvičky – obvykle agenturního typu;
- na malinké projekty – pokud si to nechcete vyloženě zkusit a víte, že to v budoucnu užijete (naopak skvěle se hodí na systémy pro vytváření malinkých webíků);
- do týmů, ve kterých chybí zkušený designér nebo kodér – spolupráce je tam dost důležitá (lze spojit do jedné osoby [frontend designéra](http://www.vzhurudolu.cz/blog/62-frontend-pozice#frontend-designer)).

## Návrat do budoucnosti?

Tím, že jsme si do projektů zavedli vodopádový systém, udělali jsme si z webdesignu dost složitý obor. Zeptejte se svého kodéra, když mu grafik předává složitá celostránková PSDéčka, jak moc času by ušetřil systematičtějšími a atomičtějšími podklady. 

Díky nástupu mobilních zařízení se zjednodušují uživatelská rozhraní, což je skvělé, ale nestačí to. Nástup designových systémů vnímám jako pročišťující proces. Proto *návrat*. Návrat do pravěku webdesignu, kdy fáze návrhu a implementace webu nebyla tak komplexní činností.

A proč návrat *do budoucnosti*? [Na WebExpo 2015](https://webexpo.cz/praha2015/prednaska/designovani-webu-v-prohlizeci/) jsem říkal, že nám chybí nástroje pro rozumný návrh rozhraní. A že v budoucnu určitě přijdou. Tušíte správně. Pattern Lab je pro mě jedním z nich. Do světa bez atomického designu, Pattern Labu nebo podobných nástrojů se už, milí čtenáři, vracet nechci. 
