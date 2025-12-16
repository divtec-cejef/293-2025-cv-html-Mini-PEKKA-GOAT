## A) Photo dans le header : lien cliquable + nouvel onglet + sécurité
- Votre image est dans le header, mais le lien pointe vers `#` (donc ça n’ouvre rien)
- Veuillez faire en sorte que le clic ouvre l’image dans un nouvel onglet
- Exemple :
```
<a href="./img/clash-royale-mini-pekka-counters.avif" target="_blank" rel="noopener noreferrer">
  <img class="avatar" src="./img/clash-royale-mini-pekka-counters.avif" alt="Avatar de Valentin Allimann">
</a>
```

## B) Corriger la structure HTML : mauvaise imbrication `<h2>` / `<section>`
- Vous avez écrit : `<h2><section ...>`
- Ce n’est pas valide : une `<section>` ne doit pas être ouverte dans un `<h2>`
- Veuillez structurer comme ceci :
```
<section id="competences">
  <h2>Mes compétences</h2>
  ...
</section>
```
- N’oubliez pas de fermer la balise `</section>`

## C) Ne pas utiliser `<nav>` pour du contenu (qualités / défauts)
- La balise `<nav>` est réservée à la navigation (menus, liens)
- Veuillez remplacer ce bloc par une `<section>` :
```
<section id="qualites">
  <h2>Mes qualités et mes défauts</h2>
  ...
</section>
```

## D) Footer : ajouter l’e-mail (conforme à l’exercice)
- Le footer doit contenir `&copy;2025` + votre e-mail cliquable
- Exemple :
```
<footer>
  &copy;2025 Valentin Allimann —
  <a href="mailto:vava.allimann@gmail.com">vava.allimann@gmail.com</a>
</footer>
```

## Autres
- Ajouter description
