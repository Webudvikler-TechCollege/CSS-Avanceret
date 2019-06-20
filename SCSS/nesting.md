# Nesting (Indlejring)

Når du skriver HTML, har du sikkert bemærket, at det har et klart indlejret og visuelt hierarki. Det er  CSS tværtimod ikke.

Med Sass kan du indlejre dine CSS-selectors sådan at de følger den samme indentering som eksisterer i din HTML. 

*Eksempel (SASS)*

```scss
nav {
  ul {
    margin: 0;
    padding: 0;
    list-style: none;
  }

  li { display: inline-block; }

  a {
    display: block;
    padding: 6px 12px;
    text-decoration: none;
  }
}
```
*CSS Resultat*
```css
nav ul {
  margin: 0;
  padding: 0;
  list-style: none;
}
nav li {
  display: inline-block;
}
nav a {
  display: block;
  padding: 6px 12px;
  text-decoration: none;
}
```