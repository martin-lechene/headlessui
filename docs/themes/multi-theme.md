# Système de multi-thème (welcome.blade.php)

## Fonctionnement

- Un sélecteur permet de choisir parmi plusieurs thèmes : `pro`, `light`, `dark`, `glass`, `forest`, `sea`, `summer`, `2D`.
- Le thème sélectionné est appliqué dynamiquement via une classe CSS sur `<body>`.
- Le choix est sauvegardé dans le `localStorage` du navigateur.
- La configuration des thèmes se trouve dans `resources/js/themes.js`.

## Ajouter ou modifier un thème

1. **Ajouter dans la config JS**
   - Ouvre `resources/js/themes.js`.
   - Ajoute/modifie un objet dans le tableau `themes` :
     ```js
     {
       key: 'nouveau',
       name: 'Mon Thème',
       class: 'theme-nouveau',
       colors: {
         primary: '#xxxxxx',
         background: '#xxxxxx',
         text: '#xxxxxx',
         accent: '#xxxxxx',
       },
     }
     ```
2. **Ajouter le style CSS**
   - Dans `welcome.blade.php`, ajoute une règle `.theme-nouveau { ... }` dans le bloc `<style>`.
   - Exemple :
     ```css
     .theme-nouveau { background-color: #f0f0f0; color: #222; }
     ```
3. **Ajouter dans le sélecteur**
   - Ajoute une `<option value="nouveau">Mon Thème</option>` dans le `<select id="theme-select">`.

## Utilisation dans les composants

- Tous les composants de la page héritent du thème via la classe sur `<body>`.
- Utilise les classes Tailwind ou des variables CSS pour adapter les couleurs selon le thème.

## Thème par défaut

- Le thème `pro` (FrappeUI) est appliqué par défaut si aucun choix n’est sauvegardé.

## Astuce

- Pour appliquer le thème dans d’autres pages, réutilise le même script et la même logique. 