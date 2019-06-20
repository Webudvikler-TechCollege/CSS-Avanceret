# Introduktion til BEM (Block Element Modifier)
BEM står for `Block ELement Modifier` og er en naming konvention, man kan bruge i forbindelse med CSS stylesheets.

Med BEM-tilgangen kan du sikre, at alle, der deltager i udviklingen af et websted, arbejder med en enkelt kodebase og taler det samme sprog. En ordentlig navngivning på dine CSS elementer giver et bedre overblik når der skal laves ændringer i designet af et website.

# Block
Block definerer et selvstændig, overordnet element, der i sig selv giver mening. Det kan eksempelvis være et header eller nav tag, men det kan også være et mere specifikt  indholdselement som f.eks. en spalte med nyheder eller lign. 

## Navngivning
Navnet på en block kan bestå af latinske bogstaver, cifre og bindestreger. 

### HTML

```html
<div class="block">...</div>
```
### CSS

```css
.block {
    color: #424242;
}
```
# Element
Et element er en del af en blok og har ingen selvstændig betydning. Ethvert element er semantisk bundet til dets blok:

## Navngivning
Navne på elementer kan bestå af latinske bogstaver, cifre, bindestreger og underscores. Elementernes CSS klasser skrives med bloknavn,to underscores og elementets navn: `.block__elem`

### HTML
```html
<div class="block">
	  ...
	  <span class="block__elem"></span>
</div>
```

### CSS:
Brug kun class selectors.
Brug aldrig tag names eller id's.
ELementer skal kun gælde for den blok de er en del af.

Rigtigt:
```css
.block__elem { color: #042; }
````

Forkert:
```css
.block .block__elem { color: #042; }
	div.block__elem { color: #042; }
```

# Modifier

Flag på blokke eller elementer. Brug dem til at ændre udseende, adfærd eller tilstand.

## Navngivning
Navne på modifiers kan bestå af latinske bogstaver, cifre, bindestreger og underscores. CSS klasser skrives som blok eller elementets navn plus to bindestreger: .block--modifier eller .block__element--modifier. Mellemrum i komplekse modifiers erstattes med bindestreg.

### HTML

En modifier er et ekstra klassenavn, som du tilføjer til en blok / element DOM node. Tilføj kun modifikatorklasser til blokke / elementer, de ændrer, og hold den oprindelige klasse:

Rigtigt:

```html
<div class="block block--mod">...</div>
	<div class="block block--size-big
		block--shadow-yes">...</div>
```

Forkert:

```html
<div class="block--mod">...</div>
```

### CSS
Brug modifier klassen som selector:

```css
.block--hidden { }
```
At ændre elementer baseret på en modifier på blok niveau:

```css
.block--mod .block__elem { }
```
Element modifier:

```css
.block__elem--mod { }
```

# Eksempel

Antag, at du har blokformular med modifier tema: "xmas" og `simpel:true` og med elementer `input` og `submit`, og element `submit` med sin egen modifier  `disabled:true` for ikke at sende formularen, når den ikke er udfyldt:

## HTML

```html
<form class="form form--theme-xmas form--simple">
  <input class="form__input" type="text" />
  <input
    class="form__submit form__submit--disabled"
    type="submit" />
</form>
```

## CSS

```css
.form { }
.form--theme-xmas { }
.form--simple { }
.form__input { }
.form__submit { }
.form__submit--disabled { }
```