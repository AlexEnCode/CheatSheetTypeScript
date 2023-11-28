# TypeScript


TypeScript est un langage de programmation open-source développé par Microsoft qui est une surcouche de JavaScript. Il ajoute des fonctionnalités de typage statique optionnel, des classes et des interfaces. Voici un aperçu des bases de TypeScript :

### Typage Statique Optionnel :
TypeScript introduit des types de données statiques en plus du typage dynamique de JavaScript.
Les types peuvent être spécifiés pour les variables, les paramètres de 
fonction et les valeurs de retour.

```typescript

let nom: string = "Alice";
let age: number = 30;

function direBonjour(personne: string): void {
    console.log("Bonjour, " + personne);
}
```

### Interfaces :
Les interfaces permettent de définir la structure d'un objet, spécifiant les propriétés et leurs types.

```typescript
interface Personne {
    nom: string;
    age: number;
}

function afficherDetails(personne: Personne): void {
    console.log(`Nom: ${personne.nom}, Age: ${personne.age}`);
}
```
### Classes :

TypeScript prend en charge la programmation orientée objet avec la définition de classes et l'héritage.

```typescript
class Animal {
    nom: string;

    constructor(nom: string) {
        this.nom = nom;
    }

    faireDuBruit(): void {
        console.log("Bruit indéfini");
    }
}

class Chien extends Animal {
    faireDuBruit(): void {
        console.log("Woof! Woof!");
    }
}

const monChien = new Chien("Buddy");
monChien.faireDuBruit();  // Affiche "Woof! Woof!"
```

### Enumérations :
TypeScript prend en charge les énumérations pour définir un ensemble de noms symboliques liés à des valeurs numériques.

```typescript
enum JoursSemaine {
    Lundi,
    Mardi,
    Mercredi,
    Jeudi,
    Vendredi,
    Samedi,
    Dimanche
}

let jour: JoursSemaine = JoursSemaine.Mercredi;
5. Modules et Espace de Noms :
TypeScript permet l'utilisation de modules pour organiser le code et éviter les collisions de noms.
typescript
Copy code
// Dans un fichier "math.ts"
export function ajouter(a: number, b: number): number {
    return a + b;
}

// Dans un fichier "app.ts"
import { ajouter } from "./math";
let resultat = ajouter(3, 5);
6. Compilation :
TypeScript est transpilé en JavaScript pour être exécuté dans un navigateur ou un environnement Node.js.
La compilation peut être effectuée en utilisant le compilateur TypeScript (tsc) pour générer des fichiers JavaScript.
bash
Copy code
tsc monFichier.ts
```

### Déclaration de Types :
TypeScript peut déduire le type des variables, mais il permet également de déclarer explicitement le type pour plus de clarté ou pour les situations où TypeScript ne peut pas inférer le type correctement.
```typescript
let age: number = 25;
let prenom: string = "Bob";
```
Ces éléments constituent les bases de TypeScript. Ils améliorent la lisibilité et la maintenabilité du code JavaScript en ajoutant des fonctionnalités de typage statique et des concepts de programmation orientée objet.