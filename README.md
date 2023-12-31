---

# Tri à Bulles

Ce dépôt contient des implémentations de l'algorithme de tri à bulles dans différents langages de programmation, notamment Python, PHP, JavaScript, et Java.

## À propos du Tri à Bulles

Le tri à bulles est un algorithme de tri simple mais inefficace. Il parcourt la liste, compare chaque paire d'éléments adjacents, et les échange si nécessaire. Le processus est répété jusqu'à ce que la liste soit entièrement triée. Bien que peu efficace pour des ensembles de données importants, le tri à bulles est souvent utilisé à des fins pédagogiques en raison de sa simplicité.

## Contenu 

- **Python:** Implémentation du tri à bulles en Python.
- **PHP:** Implémentation du tri à bulles en PHP.
- **JavaScript:** Implémentation du tri à bulles en JavaScript.
- **Java:** Implémentation du tri à bulles en Java.



---




# JAVA
```
public class TriBulles {
    public static void main(String[] args) {
        int[] tab = {4, 1, 3, 5, 2};
        System.out.print("Avant le tri: ");
        afficherTableau(tab);
        int[] result = tab;

        for (int j = 0; j < result.length; j++) {
            for (int i = 0; i < result.length - 1 - j; i++) {
                if (result[i] > result[i + 1]) {
                    bulle(result, i);
                }
            }
        }

        System.out.print("Après le tri: ");
        afficherTableau(result);
    }

    static void bulle(int[] result, int i) {
        int temp = result[i];
        result[i] = result[i + 1];
        result[i + 1] = temp;
    }

    static void afficherTableau(int[] tableau) {
        for (int i : tableau) {
            System.out.print(i + " ");
        }
        System.out.println();
    }
}
```

# Python
```
tab = [4, 1, 3, 5, 2]
print("Avant le tri:", tab)
result = tab

def bulle(result, i):
temp = result[i]
result[i] = result[i + 1]
result[i + 1] = temp

for j in range(len(result)):
for i in range(len(result) - 1 - j):
if result[i] > result[i + 1]:
bulle(result, i)

print("Après le tri:", result)
```


# PHP
```
<?php
$tab = [4, 1, 3, 5, 2];
echo "Avant le tri: " . implode(", ", $tab) . "\n";
$result = $tab;

function bulle(&$result, $i) {
    $temp = $result[$i];
    $result[$i] = $result[$i + 1];
    $result[$i + 1] = $temp;
}

for ($j = 0; $j < count($result); $j++) {
    for ($i = 0; $i < count($result) - 1 - $j; $i++) {
        if ($result[$i] > $result[$i + 1]) {
            bulle($result, $i);
        }
    }
}

echo "Après le tri: " . implode(", ", $result) . "\n";
?>
```

# JavaScript

```
let tab = [4, 1, 3, 5, 2];
console.log("Avant le tri:", tab);
let result = tab;

function bulle(result, i) {
let temp = result[i];
result[i] = result[i + 1];
result[i + 1] = temp;
}

for (let j = 0; j < result.length; j++) {
    for (let i = 0; i < result.length - 1 - j; i++) {
        if (result[i] > result[i + 1]) {
            bulle(result, i);
            }
    }
}

console.log("Après le tri:", result);
```
