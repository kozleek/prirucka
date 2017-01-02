# 4 principy návrhu responzivního rozhraní

My, dnešní webdesignéři, musíme předpokládat, že: 

* všechna zařízení mohou být dotyková,
* jeden člověk se na naše weby dívá z různých zařízení a
* nejčastěji je ovládá tím nejtlustším prstem – palcem.

Už brzy si vše rozebereme do hloubky a ukážeme dobré i špatné příklady. Ochráním vás před desktopovými zlozvyky a pokusím se zabránit častým chybám v mobilním rozhraní. Doufám.

Co se týká návrhu rozhraní, budu se zabývat hlavně jevy novými pro éru responzivního designu. Pojďme už na ty čtyři principy. Během let navrhování a implementace responzivních webů se u mě ustálily následující: 

## 1) Konzistence

Uživatelé se na naše weby dívají přes různá zařízení. Pokud to není nutné, nenuťme je učit se ovládání webu na každém zařízení znova. Rozhraní musí být co nejvíce konzistentní napříč všemi zařízeními.

## 2) Tupost

Uživatelé umějí klikat a sahat palcem, posunovat stránku a mačkat tlačítko Zpět. Nic dalšího nepředpokládám. Proto se pokud možno snažím vyhnout složitějším ovládacím prvkům jako jsou karusely, delší formuláře nebo modální okna.

Přemýšlíte, jestli vaše babička umí posouvat stránku? Čtěte například „UX Myth: People don’t scroll“ nebo „Do people actually use browser’s back button?“ na Quoře. [vrdl.in/hu8b9](http://uxmyths.com/post/654047943/myth-people-dont-scroll) [vrdl.in/slvtq](https://www.quora.com/Do-people-actually-use-browsers-back-button)

## 3) Přirozený proud

To co je na stránce nahoře je důležité, co uprostřed málo důležité a ke konci stránky zase důležitost roste. Nejpřirozenější směr konzumace informací je zleva doprava a shora dolů. Proto se vyhýbám prvkům, které uživatele nutí vracet se proti přirozenému proudu: například záložkovým navigacím uprostřed stránky. Ještě se k nim vrátím.

## 4) Očividnost

Co oči nevidí, srdce nepálí. Jenže co oči uživatele nevidí, srdce designéra pálit může. Lidé prostě schované prvky neotevírají. Proto je lepší zobrazit alespoň pár položek hlavní navigace, nebudovat závislost rozhraní na ikonách a na důležitých místech uživatelského rozhraní se vyhýbat vysouvacím nabídkám. Luke Wroblewski to hezky shrnul do anglického „Obvious Always Wins“. [vrdl.in/t93f2](http://www.lukew.com/ff/entry.asp?1945)

Tak. A teď si pojďme říct, na jakých základě jsem své čtyři principy vystavěl.