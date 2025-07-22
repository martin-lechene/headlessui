# Exemples d'inputs avancés

Voici comment utiliser le composant `@input` pour différents cas d'usage avancés. Les exemples montrent la configuration des props, sans validation réelle.

---

## Adresse IP v4
```blade
<x-input label="Adresse IP v4" placeholder="192.168.0.1" />
```

## Adresse IP v6
```blade
<x-input label="Adresse IP v6" placeholder="2001:0db8:85a3:0000:0000:8a2e:0370:7334" />
```

## Numéro de carte bancaire/crédit
```blade
<x-input label="Carte bancaire" placeholder="1234 5678 9012 3456" maxlength="19" />
```

## Numéro CVV
```blade
<x-input label="CVV" placeholder="123" maxlength="4" />
```

## Téléphone
```blade
<x-input label="Téléphone" placeholder="+33 6 12 34 56 78" />
```

## Code postal
```blade
<x-input label="Code postal" placeholder="75001" maxlength="10" />
```

## IBAN
```blade
<x-input label="IBAN" placeholder="FR76 3000 6000 0112 3456 7890 189" maxlength="34" />
```

## SIRET/SIREN
```blade
<x-input label="SIRET" placeholder="123 456 789 00012" maxlength="14" />
<x-input label="SIREN" placeholder="123 456 789" maxlength="9" />
```

## Date
```blade
<x-input label="Date" type="date" />
```

## OTP / Code de vérification (input unique)
```blade
<x-input label="Code de vérification" placeholder="123456" maxlength="6" />
```

## OTP / Code de vérification (inputs splittés)
```blade
<div class="flex space-x-2">
    <x-input maxlength="1" class="w-10 text-center" />
    <x-input maxlength="1" class="w-10 text-center" />
    <x-input maxlength="1" class="w-10 text-center" />
    <x-input maxlength="1" class="w-10 text-center" />
    <x-input maxlength="1" class="w-10 text-center" />
    <x-input maxlength="1" class="w-10 text-center" />
</div>
```

## Montant (input seul)
```blade
<x-input label="Montant" placeholder="0.00" prefix="€" type="number" step="0.01" />
```

## Montant + Devise (input + select)
```blade
<div class="flex space-x-2">
    <x-input label="Montant" placeholder="0.00" type="number" step="0.01" />
    <x-select :options="['EUR', 'USD', 'GBP']" />
</div>
``` 