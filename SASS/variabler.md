# Variabler

Variabler er en metode du kan bruge til at gemme en værdi, som du så kan genbruge i dit stylesheet. Du kan gemme værdier som farvekoder, skrifttyper og størrelser eller enhver anden relevant CSS-værdi, som skal genbruges i dit system. 

Sass bruger `$` symbolet til at gøre noget til en variabel. 

Her er et eksempel:

```sass
$font-stack:    Helvetica, sans-serif
$primary-color: #333

body
  font: 100% $font-stack
  color: $primary-color
```