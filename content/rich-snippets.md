# Rich Snippets

Česky také struktrované úryvky. Prostě graficky zajímavý obsah, který se zobrazuje ve výsledcích vyhledávání Google.

A zároveň samozřejmě jeden z nejsilnějších nástrojů z pohledu HTML kódu jednotlivých stránek pro získávání konkurenční výhody ve vyhledávači.

![Rich Snippets dostupné na českém Google](dist/images/original/rich-snippets.jpg)

Jak je z obrázku patrné, v době psaní článku máte [na českém Google](https://www.facebook.com/media/set/?set=a.384585593913.164660.250810683913&type=1) šanci nechat zobrazovat recenze, recepty, události a třeba informaci zda je produkt na skladě.
[Podle Google](https://support.google.com/webmasters/answer/99170?hl=cs) pak teoreticky ještě lidi, produkty, firmy a organizace, hudbu.

## Microdata a další způsoby značení

Jsou tři možnosti jak Google poprosit o zobrazování vašeho obsahu v úryvcích. Pro nekódery je tu klikací [Zvýrazňovač dat](https://support.google.com/webmasters/answer/2692911) a někde na půl cesty mezi klikáním a kódem pak [Pomocník](https://www.google.com/webmasters/markup-helper/), který zároveň umí vygenerovat strukturované úryvky pro e-mailové klienty (asi jen Gmail).

Protože jsme ale na kodérském webu, ukážeme si jak lze strukturované úryvky vyznačit přímo v kódu. Google doporučuje použít technologii [mikrodata](http://www.w3.org/TR/microdata/) ve struktuře vlastní specifikace [Schema.org](http://schema.org).

## Příklad – událost

Pojďme si zápis demonstrovat na schématu [Event](http://schema.org/Event), které může označovat sportovní nebo kulturní události. Nebo taky [školení](http://www.vzhurudolu.cz/kurzy):

<pre><code class="language-html">
&lt;div <strong>itemscope itemtype=&quot;http://schema.org/Event&quot;</strong>&gt;
	&lt;h3 <strong>itemprop=&quot;name&quot;</strong>&gt;
		&lt;a href=&quot;/kurzy/webovy-frontend&quot; <strong>itemprop=&quot;url&quot;</strong>&gt;
      		Dne&scaron;n&iacute; webov&yacute; frontend
    	&lt;/a&gt;
	&lt;/h3&gt;
	&lt;p <strong>itemprop=&quot;description&quot;</strong>&gt;
		&bdquo;Frontend update&rdquo; kurz, kter&yacute; citliv&#x11b; mixuje novinky a osv&#x11b;d&#x10d;en&eacute; postupy webov&eacute;ho frontendu. Ty nejd&#x16f;le&#x17e;it&#x11b;j&scaron;&iacute; &#x10d;&aacute;sti si sami&amp;nbsp;vyzkou&scaron;&iacute;te.
	&lt;/p&gt;
	&lt;p <strong>itemprop=&quot;startDate&quot; content=&quot;2015-01-22T10:00&quot;</strong>&gt;
		22. 1.
	&lt;/p&gt;
	&lt;p <strong>itemprop=&quot;location&quot; itemscope itemtype=&quot;http://schema.org/Place&quot;</strong>&gt;
		KC Greenpoint, Praha
	&lt;/p&gt;
	&lt;p <strong>itemscope itemtype=&quot;http://schema.org/Offer&quot;</strong>&gt;
		&lt;span <strong>itemprop=&quot;price&quot; content=&quot;3900.00&quot;</strong>&gt;
			3 900 K&#x10d;
			<strong>&lt;meta itemprop=&quot;priceCurrency&quot; content=&quot;CZK&quot;&gt;</strong>
		&lt;/span&gt;
	&lt;/p&gt;
&lt;/div&gt;
</code></pre>

Mikrodata jsou v ukázce zvýrazněna. Všimněte si několika věcí:

* `startDate` a jakékoliv datumy je potřeba stroji poskytnout v ISO formátu.
* Schémata je do sebe možné zanořovat – viz zde vložené typy obsahu `Place` a `Offer`.
* Pro vypisování informací, které nejsou v uživatelském obsahu vidět, Google doporučuje používat `<meta>` značku – viz `priceCurrency`.

## Otestování a zobrazování v Google

Velmi vám pomůže [Nástroj pro testování strukturovaných dat](http://www.google.com/webmasters/tools/richsnippets).

I tak je ovšem zobrazování na Google dost ve hvězdách. Kdy a zda se Rich Snippets začnou zobrazovat nemůžete nikomu garantovat, protože Google to nijak negarantuje vám. Někdy se zobrazí za pár dní, někdy to trvá měsíce, někdy se vůbec nedočkáte.

Přesto ale doporučuji úryvky připravovat. Za zkoušku dáte jen pár desítek minut svého času a efekt může být výrazný.

