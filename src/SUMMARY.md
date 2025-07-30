# Le Langage de Programmation Rust

[Le Langage de Programmation Rust](title-page.md)
[Avant-propos](foreword.md)
[Introduction](ch00-00-introduction.md)

## Pour commencer

- [Pour commencer](ch01-00-getting-started.md)
  - [Installation](ch01-01-installation.md)
  - [Hello, World!](ch01-02-hello-world.md)
  - [Hello, Cargo!](ch01-03-hello-cargo.md)

- [Programmer un Jeu de Devinette](ch02-00-guessing-game-tutorial.md)

- [Concepts de Programmation Communs](ch03-00-common-programming-concepts.md)
  - [Variables et Mutabilité](ch03-01-variables-and-mutability.md)
  - [Types de données](ch03-02-data-types.md)
  - [Fonctions](ch03-03-how-functions-work.md)
  - [Commentaires](ch03-04-comments.md)
  - [Structures de Contrôle](ch03-05-control-flow.md)

- [Comprendre la Possession](ch04-00-understanding-ownership.md)
  - [Qu'est-ce que la possession ?](ch04-01-what-is-ownership.md)
  - [Références et Emprunt](ch04-02-references-and-borrowing.md)
  - [Le Type slice](ch04-03-slices.md)

- [Utiliser des Structures pour Structurer des Données Apparentées](ch05-00-structs.md)
  - [Définir et Instancier des Structures](ch05-01-defining-structs.md)
  - [Un Exemple de Programme utilisant des Structures](ch05-02-example-structs.md)
  - [La Syntaxe des Méthodes](ch05-03-method-syntax.md)

- [Énums et filtrage de motifs](ch06-00-enums.md)
  - [Définir une Énum](ch06-01-defining-an-enum.md)
  - [La Structure de Contrôle `match`](ch06-02-match.md)
  - [Les Structures de Contrôle Concises `if let` et `let else`](ch06-03-if-let.md)

## Notions Rust Basiques

- [Gérer des Projets Grandissant Avec des Paquets, Crates, et Modules](ch07-00-managing-growing-projects-with-packages-crates-and-modules.md)
  - [Paquets et Crates](ch07-01-packages-and-crates.md)
  - [Définir des Modules pour Gérer la Portée et la Visibilité](ch07-02-defining-modules-to-control-scope-and-privacy.md)
  - [Référrer un Élément dans l'Arborescence de Modules](ch07-03-paths-for-referring-to-an-item-in-the-module-tree.md)
  - [Importer des Chemins dans la Portée via la Mot-Clef `use`](ch07-04-bringing-paths-into-scope-with-the-use-keyword.md)
  - [Séparer les Modules dans Différents Fichiers](ch07-05-separating-modules-into-different-files.md)

- [Collections Communes](ch08-00-common-collections.md)
  - [Stocker des Listes de Valeurs avec des Vecteurs](ch08-01-vectors.md)
  - [Stocké des Textes Encodés en UTF-8 avec des Strings](ch08-02-strings.md)
  - [Stocké des Clefs avec Valeur Associée dans les Hash Maps](ch08-03-hash-maps.md)

- [Gestion des Erreurs](ch09-00-error-handling.md)
  - [Erreurs Irrécupérables avec `panic!`](ch09-01-unrecoverable-errors-with-panic.md)
  - [Erreurs Récupérables avec `Result`](ch09-02-recoverable-errors-with-result.md)
  - [`panic!` ou ne pas `panic!`](ch09-03-to-panic-or-not-to-panic.md)

- [Types Génériques, Traits et Durées de Vie](ch10-00-generics.md)
  - [Generic Data Types](ch10-01-syntax.md)
  - [Traits : Définir un Comportement Partagé](ch10-02-traits.md)
  - [Valider des Références avec des Durées de Vie](ch10-03-lifetime-syntax.md)

- [Écrire des Tests Automatisés](ch11-00-testing.md)
  - [Comment Écrire des Tests](ch11-01-writing-tests.md)
  - [Contrôler la Façon Dont les Tests sont Exécutés](ch11-02-running-tests.md)
  - [Organisation des Tests](ch11-03-test-organization.md)

- [Un Projet entrée/sortie : Développer un Programme an Ligne de Commande](ch12-00-an-io-project.md)
  - [Récupérer des Arguments de la Ligne de Commande](ch12-01-accepting-command-line-arguments.md)
  - [Lire un Fichier](ch12-02-reading-a-file.md)
  - [Remaniement pour Améliorer le Modularité et la Gestion des Erreurs](ch12-03-improving-error-handling-and-modularity.md)
  - [Améliorer la Fonctionnalité de la Librairie par un Développement Piloté par les Tests](ch12-04-testing-the-librarys-functionality.md)
  - [Travailler avec des Variables d'Environnement](ch12-05-working-with-environment-variables.md)
  - [Écrire les Erreurs sur l'Erreur Standard Plutôt que sur la Sortie Standard](ch12-06-writing-to-stderr-instead-of-stdout.md)

## Penser en Rust

- [Fonctionnalités de Langage Fonctionnel : Itérateurs et Fermetures](ch13-00-functional-features.md)
  - [Fermetures : Fonctions Anonymes qui Capturent leur Environnement](ch13-01-closures.md)
  - [Traiter une Série d'Éléments avec les Itérateurs](ch13-02-iterators.md)
  - [Améliorer notre Projet entrée/sortie](ch13-03-improving-our-io-project.md)
  - [Comparaison des Performances : Boucles vs. Itérateurs](ch13-04-performance.md)

- [En Savoir plus sur Cargo et Crates.io](ch14-00-more-about-cargo.md)
  - [Personnaliser les Compilation avec les Profils de Publication](ch14-01-release-profiles.md)
  - [Publier une Crate dans Crates.io](ch14-02-publishing-to-crates-io.md)
  - [Les Espaces de Travail Cargo](ch14-03-cargo-workspaces.md)
  - [Installer des Binaires depuis Crates.io avec `cargo install`](ch14-04-installing-binaries.md)
  - [Étendre les Fonctionnalités de Cargo avec des Commandes Personnalisées](ch14-05-extending-cargo.md)

- [Pointeurs Intelligents](ch15-00-smart-pointers.md)
  - [Utiliser `Box<T>` pour Pointer vers des Données dans le Heap](ch15-01-box.md)
  - [Considérer les Pointeurs Intelligents comme des Références Régulières avec `Deref`](ch15-02-deref.md)
  - [Exécuter du Code au Nettoyage avec le Trait `Drop`](ch15-03-drop.md)
  - [`Rc<T>`, le Pointeur Intelligent Compteur de Références](ch15-04-rc.md)
  - [`RefCell<T>` et le Motif de Mutabilité Intérieur](ch15-05-interior-mutability.md)
  - [Les Références Cycliques Peuvent Créer des Fuites de Mémoire](ch15-06-reference-cycles.md)

- [La Concurrence sans Crainte](ch16-00-concurrency.md)
  - [Utiliser des Threads pour Exécuter du Code Simultanément](ch16-01-threads.md)
  - [Utiliser l'Envoi de Messages pour Transférer des Données entre des Threads](ch16-02-message-passing.md)
  - [Le Partage d'État en Concurrence](ch16-03-shared-state.md)
  - [Étendre la Concurrence avec les Traits `Send` et `Sync`](ch16-04-extensible-concurrency-sync-and-send.md)

- [Fondamentaux de Programmation Asynchrone : Async, Await, Futures et Streams](ch17-00-async-await.md)
  - [Les Futures et la Syntaxe Async](ch17-01-futures-and-syntax.md)
  - [Application de la Concurrence avec Async](ch17-02-concurrency-with-async.md)
  - [Travailler avec N'importe quel Quantité de Futures](ch17-03-more-futures.md)
  - [Streams : Futures en Sequence](ch17-04-streams.md)
  - [Un Regard Approfondi aux Traits pour Async](ch17-05-traits-for-async.md)
  - [Futures, Tâches, et Threads](ch17-06-futures-tasks-threads.md)

- [Fonctionnalités de Programmation Orientée Objet de Rust](ch18-00-oop.md)
  - [Caractéristiques des Languages Orientés Objet](ch18-01-what-is-oo.md)
  - [Utiliser des Objets de Trait qui Permettent des Valeurs de Fifférents Types](ch18-02-trait-objects.md)
  - [Implémenter un Motif de Conception Orientée Objet](ch18-03-oo-design-patterns.md)

## Sujets Avancés

- [Motifs et Filtrage par Correspondance](ch19-00-patterns.md)
  - [Tous les Endroits où des Motifs Peuvent Être Utilisés](ch19-01-all-the-places-for-patterns.md)
  - [Réfutabilité : quand un Motif peut Échouer à Correspondre](ch19-02-refutability.md)
  - [Syntaxe de Motif](ch19-03-pattern-syntax.md)

- [Fonctionnalités Avancées](ch20-00-advanced-features.md)
  - [Rust non Sécurisé](ch20-01-unsafe-rust.md)
  - [Traits Avancés](ch20-02-advanced-traits.md)
  - [Types Avancés](ch20-03-advanced-types.md)
  - [Fonctions et Fermetures Avancées](ch20-04-advanced-functions-and-closures.md)
  - [Macros](ch20-05-macros.md)

- [Projet Final : Développer un Serveur Web Multithread](ch21-00-final-project-a-web-server.md)
  - [Développer un Serveur Web Monothread](ch21-01-single-threaded.md)
  - [Transformer notre Serveur Monothread en Serveur Multithread](ch21-02-multithreaded.md)
  - [Arrêt Propre et Nettoyage](ch21-03-graceful-shutdown-and-cleanup.md)

- [Appendices](appendix-00.md)
  - [A - Mots-Clefs](appendix-01-keywords.md)
  - [B - Opérateurs et Symboles](appendix-02-operators.md)
  - [C - Traits Dérivables](appendix-03-derivable-traits.md)
  - [D - Outils de Développement Utiles](appendix-04-useful-development-tools.md)
  - [E - Éditions](appendix-05-editions.md)
  - [F - Traductions du Book](appendix-06-translation.md)
  - [G - Comment Rust est-il Fait et "Nightly Rust"](appendix-07-nightly-rust.md)
