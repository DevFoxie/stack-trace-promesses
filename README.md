# Comprendre le Stack Trace et les Promesses

### Partie 1: Comprendre le Stack Trace

1. **Création d'une fonction d'erreur :**
    - Créez une fonction appelée **`generateError`**, qui prend un paramètre **`message`**.
    - À l'intérieur de cette fonction, utilisez **`throw new Error(message)`** pour générer une erreur avec le message spécifié.
2. **Appels de fonctions :**
    - Appelez **`generateError`** dans différentes fonctions imbriquées.
    - Utilisez **`try...catch`** pour gérer l'erreur à différents niveaux.
    - Observez comment le stack trace change à mesure que vous appelez **`generateError`** dans des contextes différents.

### Partie 2: Comprendre les Promesses

1. **Création d'une fonction asynchrone :**
    - Créez une fonction asynchrone appelée **`asyncFunction`**.
    - À l'intérieur de cette fonction, utilisez **`setTimeout`** pour simuler une opération asynchrone qui prend du temps (par exemple, 2000 millisecondes).
    - Utilisez une promesse pour indiquer la fin de l'opération.
2. **Utilisation de la promesse :**
    - Appelez **`asyncFunction`** et utilisez **`.then`** pour afficher un message lorsque la promesse est résolue.
    - Utilisez également **`.catch`** pour gérer une éventuelle erreur et afficher un message d'erreur.
3. **Chaînage de promesses :**
    - Créez une deuxième fonction asynchrone appelée **`anotherAsyncFunction`** avec une promesse similaire.
    - Appelez d'abord **`asyncFunction`**, puis enchaînez l'appel à **`anotherAsyncFunction`** après la résolution de la première promesse.
    - Utilisez **`.then`** pour gérer le succès et **`.catch`** pour gérer les erreurs.

### Partie 3: Mélange Stack Trace et Promesses

1. **Création d'une fonction qui utilise à la fois une promesse et génère une erreur :**
    - Créez une fonction appelée **`mixedFunction`**.
    - À l'intérieur de cette fonction, appelez d'abord **`asyncFunction`**, puis appelez **`generateError`** dans le **`.then`** de la promesse.
    - Utilisez **`.catch`** pour gérer les erreurs de la promesse et afficher un message d'erreur.

### Conclusion :

- Observez comment le stack trace évolue lorsque vous utilisez **`generateError`** dans différentes situations, en particulier dans le contexte des promesses.
- Comprenez comment les promesses permettent de gérer de manière asynchrone les opérations tout en maintenant un flux de contrôle lisible.

N'hésitez pas à expérimenter et à explorer davantage ces concepts pour renforcer votre compréhension 🚀
