# Příručka pro VzhůruDolů.cz

Texty o technikách a technologiích moderní webové kodéřiny.

## Autorství

Autorem Příručky je Martin Michálek: [vrdl.cz/martin]([http://www.vzhurudolu.cz/martin).

Opravy, bugreporty, změny jsou vítány: [github.com/machal/prirucka/issues](https://github.com/machal/prirucka/issues).

## Používáme Markdown Extra

- http://parsedown.org/extra/
- https://michelf.ca/projects/php-markdown/extra/

## Pravidla psaní

Texty zde vložené se čtou nebo mohou být čteny na různých místech:

1. V tomto veřejném repozitáři.
2. V Příručce na VzhůruDolů.cz: [vrdl.cz/prirucka/css3](http://www.vzhurudolu.cz/prirucka/css3).
3. V eboocích, nyní jen „Vzhůru do CSS3”: [vrdl.cz/ebook](http://www.vzhurudolu.cz/ebook)
4. V tištěných knihách, což je zatím jen v plánu.

Před každým zveřejněním na těchto místech prochází Markdown obsah určitými transformacemi a proto je potřeba držet se jednotného způsobu psaní. 

V prvé řadě je potřeba psát obecně ve stylu například „v době psaní tohoto textu“, nikoliv „v době psaní tohoto článku“.

### Formátování

Pro ebooku je lepší co nejjednodušší formátování, proto:

- Pro zvýrazňování slov v textu nepoužíváme tučný řez, ale kurzívu. Jedinou výjimkou jsou „nadpisy“ v `ul`/`ol` seznamech. Tučný řez rezervujeme pro nadpisy.
- `ul`/`ol` seznamy nepoužíváme pro texty delší než jedna věta. V eboocích se pak rozpadají na více řádek.

### Odkazy

V textu odkazujeme obecně jen interně - přímo na Markdown soubory, které jsou v eboocích, externí jako celé url. Aby to v ebooku bylo jasné. Na co lze klikat a co vede ven. A taky kvůli případnému tisku odkazy ven pomocí celých url.

- **Interní** v rámci stejného ebooku - uvnitř textu:  
```markdown
Lorem ipsum [odkaz](odkaz.md) lorem ipsum.
```
- **Důležité interní i externí** - nakonci odstavce ve zkrácené verzi - odkaz ale vede na plnou, abychom šetřili přesměrování:  
```markdown
Lorem ipsum lorem ipsum:
([vrdl.cz/p/grunt](http://www.vzhurudolu.cz/prirucka/grunt)).
```
- **Méně důležité** - bez odkazu (máme Google, že…)

### Video

Ideální je vložení pomocí HTML kódu. Markdown je tady nespolehlivý:

```html
<p class="video">
Video: <a href="https://www.youtube.com/watch?v=VN8CFG-YajE">BrowserStack</a> ~ Jak testovat web ve všech prohlížečích a nemuset řešit virtuály a emulátory.
</p>
```

### Podcast

Vložení opět pomocí HTML kódu. 

```html
<p class="podcast">
Podcast: <a href="https://soundcloud.com/vzhurudolu/s-robinem-pokornym-o-css-v-js" data-id="296642310">S Robinem Pokorným o CSS v JS</a>
</p>
```

### Zobrazení jen na webu

Prostě odstavec s třídou `.web-only`. V ebooku bude při předzpracování textu odstraněno.

```markdown
<p class="web-only" markdown="1">
  Čtete referenční příručku vlastností, které je možné přiřadit položkám 
  [flexboxu](css3-flexbox.md).
</p>
```

### Umístění reklamy na webu

Standardně po druhém odstavci. Lze změnit jednou nebo více kotvami `<!-- AdSnippet -->` v obsahu.
