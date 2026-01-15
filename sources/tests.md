---
marp: true
theme: default
paginate: true
header: Tests
footer: Les Tests en Développement Web
---

# Les Tests en Développement Web

## JavaScript et PHP

---

## Sommaire

1. **Introduction aux Tests**
2. **Types de Tests**
3. **Outils de Test pour JavaScript**
4. **Outils de Test pour PHP**

---

## 1.Introduction aux tests

- Permettent de garantir la qualité du code
- Un fonctionnement attendu
- La gestion des cas limites
- La performance
- La sécurité

---

- Détecter les bugs
- Faciliter la maintenance
- Documenter le code
- Tests avant développement (TDD)
- Tests automatisé
- Intégration continue 

---

## 2. Types de Tests

| Type de Test            | Description                            | Objectif                                |
| ----------------------- | -------------------------------------- | --------------------------------------- |
| **Tests Unitaires**     | Test de fonction/méthode isolée        | Vérifier le comportement d'un composant |
| **Tests d'Intégration** | Test de l'interaction entre composants | Assurer la compatibilité                |
| **Tests Fonctionnels**  | Test du comportement global            | Validation des exigences                |
| **Tests de Régression** | Vérification après modification        | Garantir la stabilité                   |

---

## 3. Outils de Test JavaScript

### Frameworks Principaux

- **Jest**

  - Développé par Facebook
  - Configuration simple
  - Couverture de code intégrée

- **Mocha**
  - Flexible
  - Compatible avec différentes assertions
  - Supporte async/await

---

## Exemple de Test Jest

```javascript
// fonction à tester
function somme(a, b) {
  return a + b;
}

// test unitaire
test("addition de 1 + 2", () => {
  expect(somme(1, 2)).toBe(3);
});
```

---

## 4. Outils de Test PHP

### Frameworks Principaux

- **PHPUnit**

  - Standard de l'industrie
  - Tests unitaires complets
  - Rapport de couverture

- **Pest**
  - Syntaxe moderne
  - Inspiré de Jest
  - Très lisible

---

## Exemple de Test PHPUnit

```php
<?php
class Calculatrice {
    public function addition($a, $b) {
        return $a + $b;
    }
}

use PHPUnit\Framework\TestCase;

class CalculatriceTest extends TestCase {
    public function testAddition() {
        $calculatrice = new Calculatrice();
        $resultat = $calculatrice->addition(2, 3);

        $this->assertEquals(5, $resultat);
    }
}
```

---

## 5. Bonnes Pratiques


