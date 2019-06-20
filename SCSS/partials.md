# Partials (Delefiler)

Du kan oprette delbare Sass-filer, der indeholder små bidder af CSS, som du kan inkludere i andre Sass-filer. Dette er en effektiv måde at strukturere din CSS på og gør det lettere og mere overskueligt at vedligeholde dine stylesheets. 

Du kan isolere dine partials filer ved at sætte en underscore i starten af deres filnavn som f.eks. `_partial.scss`. Så genererer Sass ikke en css fil af denne fil når den kompilerer.

Sass partials bruges sammen med @import direktivet.

*Eksempel:*

```scss
@import '_partials.scss';
```