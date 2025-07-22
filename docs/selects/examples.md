# Exemples de selects avancés

Voici comment utiliser le composant `@select` pour différents cas d'usage avancés. Les exemples montrent la configuration des props, sans logique fonctionnelle.

---

## Select avec groupes d'options (optgroup)
```blade
<x-select label="Pays" :options="[
    ['label' => 'Europe', 'options' => [
        ['label' => 'France', 'value' => 'FR'],
        ['label' => 'Allemagne', 'value' => 'DE'],
    ]],
    ['label' => 'Asie', 'options' => [
        ['label' => 'Japon', 'value' => 'JP'],
        ['label' => 'Chine', 'value' => 'CN'],
    ]],
]" />
```

## Select asynchrone (exemple non fonctionnel)
```blade
<x-select label="Ville" :options="[]" loading="true" placeholder="Chargement..." />
<!-- Les options seraient chargées dynamiquement côté JS/Livewire -->
```

## Select avec images/icônes dans les options
```blade
<x-select label="Réseau social" :options="[
    ['label' => 'Facebook', 'value' => 'fb', 'icon' => '<svg class=\'w-4 h-4\'>...</svg>'],
    ['label' => 'Twitter', 'value' => 'tw', 'icon' => '<svg class=\'w-4 h-4\'>...</svg>'],
]" />
<!-- Le composant doit afficher l'icône si la clé 'icon' est présente -->
```

## Select avec virtual scroll (exemple non fonctionnel)
```blade
<x-select label="Produit" :options="range(1, 1000)" placeholder="Sélectionner un produit..." />
<!-- UX : virtual scroll à prévoir pour de très grandes listes -->
```

## Select avec recherche multi-options
```blade
<x-select label="Technologies" :options="['PHP', 'Laravel', 'Vue.js', 'React']" multiple="true" searchable="true" />
```

## Select de tags
```blade
<x-select label="Tags" :options="['Laravel', 'PHP', 'Livewire']" multiple="true" taggable="true" placeholder="Ajouter un tag..." />
``` 