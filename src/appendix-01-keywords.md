## Appendice A : Mots Clefs

La liste suivante contient les mots clefs qui sont réservés pour un usage
actuel ou future par le langage Rust. Ils ne peuvent donc pas être utilisés
comme identificateurs (hormis en tant qu'identificateurs bruts comme discuté
dans la section "[Identificateurs Bruts][raw-identifiers]<!-- ignore -->").
Les identificateurs sont des noms de fonctions, variables, paramètres, champs
de structure, modules, crates, constantes, macros, valeurs statiques, attributs,
types, traits, ou durées de vie.

[raw-identifiers]: #identificateurs-bruts

### Mots Clefs Actuellement Utilisés

Ci-dessous une liste des mots clefs actuellement utilisés, avec la description
de leur fonction.

- `as` - effectue une transformation de type primitive, précise le trait contenant
un élément, ou renomme des éléments dans les instructions `use`.
- `async` - retourne un `Future` au lieu de bloquer le fil d'exécution.
- `await` - suspend l'exécution en jusqu'à ce que le résultat d'une `Future` soit prêt
- `break` - sort d'une boucle immédiatement
- `const` - définit des éléments constants ou des pointeurs mémoire constants
- `continue` - passe à l'itération suivante d'une boucle
- `crate` - dans un chemin de module, réfère à la racine de la crate
- `dyn` - utilise dynamiquement un objet de trait
- `else` - une branche de repli pour les structures de contrôle `if` et `if let`
- `enum` - définit une énumération
- `extern` - lie une fonction ou une variable externe
- `false` - le littéral booléen "faux"
- `fn` - définit une fonction ou le type pointeur de fonction
- `for` - boucle sur des éléments depuis un intérateur, implémente un trait,
ou spécifie une durée de vie de niveau supérieur
- `if` - branche basée sur le résultat d'une expression conditionnelle
- `impl` - implémente des fonctionnalités inhérentes ou de trait
- `in` - partie de la syntaxe de boucle `for`
- `let` - définit une variable
- `loop` - boucle inconditionnelement
- `match` - compare une valeur à des motifs
- `mod` - définit un module
- `move` - fait une fermeture prendre possession de toutes ses captures
- `mut` - dénote la mutabilité dans les références, les pointeurs bruts, ou
les éléments issus de motifs
- `pub` - dénote la visibilité public dans les champs de structures, blocs `impl`,
ou modules
- `ref` - lie une valeur avec une référence
- `return` - retourne depuis une fonction
- `Self` - un alias de type désignant le type en train d'être défini ou implémenté
- `self` - désigne le sujet d'une méthode ou le module courant
- `static` - variable globale ou durée de vie dépassant l'entièreté de l'exécution
du programme
- `struct` - définit une structure
- `super` - module parent du module courant
- `trait` - définit un trait
- `true` - le littéral booléen "vrai"
- `type` - définit un alias de trait ou un type associé
- `union` - définit une [union][union]<!-- ignore --> ; est un mot-clef uniquement
quand utilisé dans la déclaration d'une union
- `unsafe` - dénote du code, des fonctions, traits, ou implémentations non sécurisés
- `use` - importe des symboles dans la portée ; spécifie des captures précises pour
les contraintes de générique et de durée de vie
- `where` - dénote une clause qui contraint un type
- `while` - boucle conditionnellement en se basant sur le résultat d'une expression


[union]: ../reference/items/unions.html

### Mots Clefs Réservés pour un Usage Futur

Les mots clefs suivant n'ont pas de fonction actuellement mais sont réservés 
par Rust pour un potentiel usage à l'avenir.

- `abstract`
- `become`
- `box`
- `do`
- `final`
- `gen`
- `macro`
- `override`
- `priv`
- `try`
- `typeof`
- `unsized`
- `virtual`
- `yield`

### Identificateurs Bruts

Les _Identificateurs bruts_ sont une syntaxe qui vous laisse utilisaer des mots
clefs qui ne sont normallement pas autorisés. Vous pouvez utiliser un identificateur
brut en préfixant un mot-clef par `r#`.

Par exemple, `match` est un mot-clef. Si vous essayez de compiler la fonction suivante
qui utilise `match` comme nom :

<span class="filename">Fichier : src/main.rs</span>

```rust,ignore,does_not_compile
fn match(auguille: &str, botte_de_foin: &str) -> bool {
    botte_de_foin.contains(auguille)
}
```

vous obtiendrez cette erreur :

```text
error: expected identifier, found keyword `match`
 --> src/main.rs:4:4
  |
4 | fn match(auguille: &str, botte_de_foin: &str) -> bool {
  |    ^^^^^ expected identifier, found keyword
```

Cette erreur cous montre que vous ne pouvez pas utiliser le mot-clef 
`match` comme identificateur de fonction. Pour utiliser le mot-clef
`match` comme nom de fonction, vous devez utiliser la syntaxe 
d'identificateur brut, comme ci-dessous :

<span class="filename">Fichier : src/main.rs</span>

```rust
fn r#match(auguille: &str, botte_de_foin: &str) -> bool {
    botte_de_foin.contains(auguille)
}

fn main() {
    assert!(r#match("foo", "foobar"));
}
```

Ce code compilera sans aucune erreur. Notez la présence du préfixe `r#` dans le
nom de la fonction aussi bien dans sa définition que dans son appel dans `main`.

Les identificateurs bruts vous permettent d'utiliser n'importe quel mot de votre
choix en tant qu'identificateur, même s'il se trouve que ce mot est un mot-clef 
réservé. Cela donne plus de liberté dans le choix des noms identificateurs, et 
permet également d'intégrer des programmes écrits dans un langage dans lequel ces
mots ne sont pas des mots-clefs. Additionnelement, les identificateurs bruts
permettent d'utiliser des librairies écrites dans des éditions Rust différentes
que celle que votre crate utilise. Par exemple, `try` n'est pas un mot-clef dans 
l'édition 2015 mais l'est dans les éditions 2018, 2021 et 2024. Si vous dépendez
d'une librairie écrite en utilisant l'édition 2015 et qui a une fonction `try`,
vous devrez utiliser la syntaxe d'identificateurs bruts, `r#try` dans ce cas, pour
appeler cette fonction depuis votre code utilisant une édition ultérieure. Voir
l'[Appendice E][appendeix-e]<!-- ignore --> pour plus d'informations sur les éditions.

[appendix-e]: appendix-05-editions.html
