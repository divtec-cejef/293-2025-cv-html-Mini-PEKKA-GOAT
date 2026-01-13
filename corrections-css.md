## A) Corriger les listes HTML (balises mal imbriquées)

Actuellement vous avez un `<p>` à l’intérieur d’un `<ul>` avec des `<li>` :
```

<ul>
  <p>
    <li>...</li>
    <li>...</li>
  </p>
</ul>
```

À corriger :

* un `<ul>` ne contient que des `<li>`
* pas de `<p>` autour

Exemple correct :
```

<ul>
  <li>...</li>
  <li>...</li>
</ul>
```

---

## B) Centrer la page correctement (max-width sans centrage)

Vous avez :
```
body {
max-width: 800px;
}
```

Mais il manque le centrage horizontal.

À corriger :
```
body {
max-width: 800px;
margin: 0 auto;
}
```

💡 *`margin: 0 auto` centre un bloc quand une largeur/max-width est définie.*

---

## C) Tailles de texte : ajouter `px` et `em` (consigne)

Vous avez déjà du `rem` ✅
Il manque :

* une taille en `px`
* une taille en `em`

Exemple :
```
h1 {
font-size: 36px; /* px */
}

h2 {
font-size: 1.5em; /* em */
}
```

💡 *L’exercice demande les 3 unités pour comparer leurs comportements.*

> *`px` = fixe, `em` = relatif au parent, `rem` = relatif à la racine.*

---

## D) Image de fond : il faut une vraie image (pas seulement un dégradé)

Vous avez un dégradé :
```
background: linear-gradient(...);
```

Mais la consigne demande une **image de fond**.

À corriger (exemple) :
```
body {
background-image: url("../img/background.jpg");
background-size: cover;
background-position: center;
background-repeat: no-repeat;
}
```

---

## E) Police personnalisée : `@font-face` manquant + police non importée

Vous utilisez :
```
font-family: 'Luckiest Guy', cursive;
```

Mais :

* vous ne l’importez pas
* vous n’utilisez pas `@font-face` (consigne)

À corriger :

* ajouter une police en local dans `fonts/`
* la déclarer avec `@font-face`
* l’appliquer au body (ou titres)

Exemple :
```
@font-face {
font-family: "MaPolice";
src: url("../fonts/mapolice.woff2") format("woff2");
font-weight: 400;
font-style: normal;
}

body {
font-family: "MaPolice", Arial, sans-serif;
}
```

💡 *Déclarer une police avec `@font-face` vous apprend à gérer vos ressources localement.*

---

## F) Éviter `margin-left: 33%` sur les listes (mise en page fragile)

Actuellement :
```
ul {
margin-left: 33%;
margin-right: 33%;
}
```

Problème :

* ça casse facilement sur mobile
* ce n’est pas un vrai centrage

À corriger :

* centrer via un conteneur (`main`) et laisser les listes naturelles
* ou utiliser une largeur + auto

Exemple :
```
main {
max-width: 800px;
margin: 0 auto;
padding: 20px;
}

ul {
margin: 0 0 20px 0;
padding-left: 20px;
}
```

💡 *Les % sur marges donnent souvent des résultats imprévisibles.*

> *Un layout propre se fait avec un conteneur centré.*

---

## G) Footer : ajouter une vraie marge extérieure en CSS

Pour respecter clairement la consigne, ajoutez une marge au footer :

Exemple :
```
footer {
margin-top: 40px;
padding: 20px;
text-align: center;
}
```

💡 *La marge extérieure sépare visuellement le footer du contenu.*


