---
marp: true
author: Ibra barry
theme: default
class: invert

---

 #  Sass

By:Ibra Barry

---

# Variabili
Le variabili vengono inizializzate utilizzando il simbolo del dollaro ($) prima del nome della variabile, sono uno strumento utile per memorizzare e riutilizzare valori specifici all'interno dei fogli di stile.

``` scss
$primary-color: #ff0000;

body {
  color: $primary-color;
}

```
---
# Variabili
Nell'esempio, è stata dichiarata una variabile chiamata $primary-color e le è stato assegnato il valore #ff0000, che rappresenta il colore rosso. Sucessivamente la variabile viene utilizzata  all'interno della regola CSS per l'elemento body
assegnando il valore della variabile alla proprietà **color**.

---
# At-Rules
 Sono direttive speciali che iniziano con il simbolo "@" e sono utilizzate per specificare comportamenti particolari nel preprocessore Sass. Queste direttive consentono di definire regole, importare file, creare mixin, condizionare il codice e altro ancora.
 Le direttive di sass sono le seguenti:

 ---
 
 ## @use
 Questa regola permette di caricare funzioni e variabili da altri fogli di stile Sass e combina CSS da più fogli di stile.
 
 ad esempio:
 ```scss
    $bg-color: red;
    $font-size-body:12px;
 ```
 ```scss
 @use 'variabels' as v;

 body{
    v.$bg-color: red;
    v.$font-size-body:12px;
 }
 ```
---
 ## @use
Nell'esempio, è stato utilizzato un file chiamato variables.scss che contiene le variabili:
$bg-color: red; $font-size-body:12px;

Nel file main.scss, viene utilizzato l'at-rule @use per importare il file variables.scss come modulo e gli viene assegnato l'alias v. Quindi, possiamo accedere alle variabili definite nel modulo utilizzando la sintassi v.$nome-variabile.

---

 
