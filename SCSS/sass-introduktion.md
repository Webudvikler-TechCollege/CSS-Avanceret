# Introduktion til SASS

SASS er en forkortelse af Synt

## Preprocessing (forbehandling)
CSS alene kan være sjovt, men i takt med at stylesheets bliver større og mere komplekse, kan en preprocessor være en god hjælp og her kan du med fordel bruge *Sass*. 

Sass lader dig bruge funktioner, der ikke findes i almindelig CSS, f.eks. *variabler*, *nesting*, *mixins*, *nedarvning* og andre, der gør det nemmere at skrive CSS.

Når du begynder at bruge Sass, skriver du din kode i en særlig sass arbejdsfil. Derefter skal denne fil kompileres til en css fil og det er denne fil du kan bruge på din hjemmeside.

Den mest direkte måde at få det til at ske sker i din terminal. Når Sass er installeret, kan du kompilere din Sass til CSS ved hjælp af sass-kommandoen. Du skal fortælle Sass hvilken fil der skal opbygges fra, og hvor skal CSS sendes til. For eksempel vil kørsel sass input.scss output.css fra din terminal tage en enkelt Sass-fil, input.scss og kompilere den fil til output.css.

Hvis du bruger VS Code er det ganske nemt at installere en udvidelse der automatisk kompilerer dine sass filer hver gang du gemmer dem. Her kan du f.eks. bruge *Live Sass Compiler*.