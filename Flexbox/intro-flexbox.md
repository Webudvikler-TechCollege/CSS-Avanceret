# Introduktion til Flexbox

Flexbox (*flexible box module*) er et sæt af CSS-egenskaber som kan hjælpe dig med at skabe et fleksibelt layout, distribuere ekstra plads og justere indholds-elementer i en given container. 

Flexbox gør det nemt at:
- arrangere elementer i enhver retning, fra venstre til højre, fra højre til venstre, fra top til bund eller fra bund til top
- omdanne eller omarrangere rækkefølgen for et sæt elementer
- placere elementer på en linie uden at wrappe  eller at tvinge dem til at wrappe, når der ikke er plads nok
- strække og justere elementer i forhold til deres parent element

# Flexbox Basics

Flexbox handler i bund og grund om relationen mellem et parent element og child elementer i første niveau.

```html
<div class="flex-container">
    <div class="flex-item"></div>
    <div class="flex-item"></div>
    <div class="flex-item"></div>
</div>
```

Parent elementet kaldes for *flex container* og de direkte child elementer kaldes for *flex items*.

Det horisontale flow på flex items kaldes for *main axis* og løber som standard fra venstre til højre.

Starten på det horisontale flow begynder ved den første linie på vores flex-container og kaldes for *main start*. Disse løber til *main end* som ligger på den modsatte linie af vores flex-container.

Længden fra *main start* til *main end* kaldes *main size*.

Flex containerens *cross axis* løber vertikalt fra top til bund. Og ligesom main axis har cross axis en *main start* og en *main end* på containerens øverste og nederste linie.

## Flex container

For at få et element til at opføre sig som en flex-container kan vi give den følgende css egenskab:

```css
.flex-container {
    display: flex;
}
```

## Links 
- []

