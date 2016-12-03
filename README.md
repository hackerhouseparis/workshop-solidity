# workshop-solidity

Aller sur https://ethereum.github.io/browser-solidity/ .

Niveau 0
--------

__Obejctif :__ créer un smart contract avec une déclaration et une assignation de variable.

__Syntaxe solidity à connaître :__

Définir la version du compilateur :
```
pragma solidity ^0.4.4;
```

Déclarer un smart contract :
```
MonSamrtContract {
/* contenu du smart contract */
}
```

Déclarer une variable :
```
uint maVariable;
```

Créer une fonction avec un paramètre :
```
function set(uint x) {
}
```

Assigantion de variable :
```
maVariable = x;
```

Niveau 1
--------

__Obejctif :__ dans le smart contract *niveau 0*, ajouter un accesseur `get()` pour récupérer la valeur de `maVariable`.

__Syntaxe solidity à connaître :__

Retourner une valeur dans une fonction :
```
function get() constant returns (uint) {
    return maVariable;
}
```

Niveau 2
--------

__Obejctif :__ créer une cryptomonnaie.

__Syntaxe solidity à connaître :__

Type `address` contenant la clé publique  :
```
address mineur;
```

Déclarer une variable publique :
```
address public mineur;
```
est équivalent à
```
function mineur() returns (address) { return mineur; }
```
Récupérer l'adresseur du mineur (variable globale) :
```
mineur = msg.sender;
```

Créer un tableau associatif (table de hashage) :
```
mapping (address => uint) public balances;
```

Assigner / récupérer la valeur d'un tableau
```
balances[cle] = valeur;
```

Les opérateurs `+`, `-`, `<`, `>` permettent respectivement d'additionner, soustraire et de comparer.

Faire une condition :
```
if (0 < 1) {
    /* code */
}
```

Niveau 3
--------

__Obejctif :__ créer un système de vote.

__Syntaxe solidity à connaître :__

Type `struct` :
```
struct maStructure {
    uint maVariable;
    bool aVote; // de type boolean
    address procuration; // pouvoir personne
    // autres variables
}
```




