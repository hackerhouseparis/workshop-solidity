# workshop-solidity

Aller sur https://ethereum.github.io/browser-solidity/ .

Niveau 0
--------

__Objectif :__ créer un smart contract avec une déclaration et une assignation de variable.

__Syntaxe solidity à connaître :__

Définir la version du compilateur :
```
pragma solidity ^0.4.4;
```

Déclarer un smart contract :
```
MonSmartContract {
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

Assignation de variable :
```
maVariable = x;
```

Niveau 1
--------

__Objectif :__ dans le smart contract *niveau 0*, ajouter un accesseur `get()` pour récupérer la valeur de `maVariable`.

__Syntaxe solidity à connaître :__

Retourner une valeur dans une fonction :
```
function get() constant returns (uint) {
    return maVariable;
}
```

Niveau 2
--------

__Objectif :__ créer une cryptomonnaie.

__Syntaxe solidity à connaître :__

Type `address` contenant la clé publique  :
```
address mineur;
```

Déclarer une variable publique :
```
address public createur;
```
est équivalent à
```
function createur() returns (address) { return mineur; }
```
Récupérer l'adresseur du mineur (variable globale) :
```
createur = msg.sender;
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

Addresses utilisées par le browser solidity
```
"0xca35b7d915458ef540ade6068dfe2f44e8fa733c"
"0x14723a09acff6d2a60dcdf7aa4aff308fddc160c"
"0x4b0897b0513fdc7c541b6d9d7e929c4e5364d2db"
"0x583031d1113ad414f02576bd6afabfb302140225"
"0xdd870fa1b7c4700f2bd7f44238821c26f7392148"
```

Niveau 3
--------

__Objectif :__ créer un système de vote par procuration.

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

Pour arrêter l'éxécution :
```
throw;
```

C'est tout !
