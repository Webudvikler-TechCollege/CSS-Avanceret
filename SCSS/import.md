# Import

I CSS kan du bruge import til at opdele dit CSS i mindre dele. Den eneste ulempe er, at hver gang du bruger `@import` i CSS, skal du også lave en HTTP-request. 

I Sass kan du også bruge `@import`, men i stedet for at kræve en HTTP-request kombinerer Sass den importerede fil med den, du importerer til.

I nedenstående eksempel importeres _reset.scss til base.scss:

*_reset.scss_*

```scss
html,
body,
ul,
ol {
  margin:  0;
  padding: 0;
}
```

*base.scss:*

```scss
@import 'reset';
body {
  font: 100% Helvetica, sans-serif;
  background-color: #efefef;
}
```
*CSS Resultat:*

```css
html,
body,
ul,
ol {
  margin:  0;
  padding: 0;
}
body {
  font: 100% Helvetica, sans-serif;
  background-color: #efefef;
}
```

Læg mærke til at vi bruger `@import 'reset';` i base.scss filen. Når du importerer en fil, behøver du ikke at medtage filtypen .scss. Sass er smart nok til at finde ud af det for dig.