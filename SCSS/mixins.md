# Mixins

Mixins er en af de mest anvendte funktionaliteter fra Sass sproget. De er nøglen til genbrugelighed og DRY komponenter. Og af en god grund: mixins tillader forfattere at definere styles der kan genbruges igennem stylesheetet.

De kan indeholde hele CSS-regler og faktisk alt hvad der er tilladt overalt i et Sass dokument. De kan endda tage argumenter, præcis som funktioner. 

Mixins er også fordelagtige når vi snakker vendor prefiks.

### SCSS

```scss
@mixin transform($property) {
  -webkit-transform: $property;
  -ms-transform: $property;
  transform: $property;
}
.box { @include transform(rotate(30deg)); }
```
For at lave en mixin skal du bruge `@mixin` og give det et navn. I ovenstående eksempel er der brugt navnet `transform`. 

Der er også brugt variablen `$property` i paranteserne og her kan du så sætte den variable værdi, som du vil bruge til transormationen. (*30 deg*)

Når du har lavet dit mixin, kan du efterfølgende anvende den som en CSS-deklaration, der begynder med `@include` efterfulgt af navnet på mixin.

*Eksempel:*
```scss
.box { @include transform(rotate(30deg)); }
```