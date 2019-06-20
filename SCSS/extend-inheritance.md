# Extend & Inherit (Udvid/Nedarv)

Dette er en af de mest nyttige funktioner i Sass. 

Ved hjælp af `@extend` kan du dele et sæt CSS-egenskaber fra en selector til en anden. Det hjælper med at holde din Sass meget enkel. 

I vores eksempel vil vi oprette en simpel serie af meddelelser for fejl, advarsler og succeser ved hjælp af en anden funktion, der går hånd i hånd med extend, placeholder klasser. 

En placeholder klasse er en speciel type klasse, der kun udskriver, når den forlænges, og kan hjælpe med at holde din kompilerede CSS ren og pæn.

```scss
/* Denne CSS vil give output da %message-shared er extended. */
%message-shared {
  border: 1px solid #ccc;
  padding: 10px;
  color: #333;
}

// Denne CSS vil ikke give output da %equal-heights ikke er extended.
%equal-heights {
  display: flex;
  flex-wrap: wrap;
}

.message {
  @extend %message-shared;
}

.success {
  @extend %message-shared;
  border-color: green;
}

.error {
  @extend %message-shared;
  border-color: red;
}

.warning {
  @extend %message-shared;
  border-color: yellow;
}
```

Ovenstående kode tildeler `.message`, `.success`, `.error` og `.warning` stilen fra `%message-shared`. 

Det betyder at overalt, hvor %message-shared vises, vil `.message`, `.success`, `.error`, og `.warning` også blive vist. Den magiske sker i den genererede CSS, hvor hver af disse klasser får de samme CSS egenskaber som `%message-shared`. Dette hjælper dig med at undgå at skulle skrive flere klassenavne på forskellige HTML-elementer.