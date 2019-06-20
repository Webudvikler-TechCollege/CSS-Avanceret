# Variabler

Variabler er en metode du kan bruge til at gemme en værdi, som du så kan genbruge i dit stylesheet. Du kan gemme værdier som farvekoder, skrifttyper og størrelser eller enhver anden relevant CSS-værdi, som skal genbruges i dit system. 

Sass bruger `$` symbolet til at gøre noget til en variabel. 

*Eksempel (SASS):*

```scss
$font-stack:    Helvetica, sans-serif;
$primary-color: #333;

body {
  font: 100% $font-stack;
  color: $primary-color;
}
```
Når din sass kode bliver kompileret, tager den de definerede variabler for `$font-stack` og `$primary-color` og genererer almindelig CSS med vores variabel værdier. Dette er effektivt når du arbejder med farver der skal være konsekvente på hele websitet.

*CSS Resultat af ovenstående*
```css
body {
  font: 100% Helvetica, sans-serif;
  color: #333;
}
```