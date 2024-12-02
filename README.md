# Atelier : Introduction à Neovim

Bienvenue dans cet atelier où nous allons découvrir **Neovim**, un éditeur de texte moderne, puissant et extensible.

---

## Objectifs de l’atelier

- Comprendre l’historique et la philosophie de Neovim.
- Apprendre à naviguer efficacement dans un fichier avec les motions.
- Découvrir les fonctionnalités de base : buffers, terminal intégré, quickfix, macros.
- Installer et configurer des plugins essentiels.
- Créer un environnement de développement productif.

---

## Plan de l’atelier

### 1. Introduction à Neovim

#### Historique
- **Vi et Vim** : Créés pour Unix, ils sont rapides, légers et adaptés au terminal.
- **Neovim** : Une version moderne de Vim introduite en 2014, avec un focus sur l’extensibilité et les outils modernes.

#### Philosophie
- Fonctionne directement dans le terminal (core Linux).
- **Pas un IDE de base** : un éditeur minimaliste que l’on peut enrichir avec des plugins.

---

## 2. Fonctionnalités de base

Neovim repose sur des concepts fondamentaux hérités de Vim, qui permettent une utilisation puissante et efficace de l'éditeur. Voici les bases pour bien démarrer.

---

### Modes de Vim

Neovim (et Vim) fonctionne avec différents **modes**, chacun ayant un rôle spécifique. Voici les principaux :

- **Mode Normal** (par défaut) : Utilisé pour naviguer dans le fichier, exécuter des commandes ou manipuler du texte.
  - Exemple : En mode normal, tapez `dd` pour supprimer une ligne ou `x` pour supprimer un caractère.

- **Mode Insertion** : Permet d’insérer ou d’éditer du texte.  
  - Passez en mode insertion avec `i` (avant le curseur), `a` (après le curseur) ou `o` (nouvelle ligne).

- **Mode Visual** : Permet de sélectionner des blocs de texte.  
  - `v` : Mode visual (caractère par caractère).  
  - `V` : Sélection ligne par ligne.  
  - `Ctrl+v` : Sélection par blocs (Visual Block).

- **Mode Command-line** : Pour exécuter des commandes spécifiques.  
  - Tapez `:` pour entrer dans ce mode et exécuter des commandes comme `:w` (sauvegarder), `:q` (quitter), ou `:!ls` (exécuter une commande shell).

---

### Navigation (Vim Motion)

L'un des points forts de Vim/Neovim est sa navigation ultra-rapide sans utiliser la souris. Voici les principales commandes de déplacement :

#### Déplacements simples :
- `h` `l` `j` `k`: Déplacer le curseur à gauche / droite / bas / haut 

#### Déplacements avancés :
- `w` : Aller au début du mot suivant.  
- `b` : Retourner au début du mot précédent.  
- `e` : Aller à la fin du mot.  
- `0` : Aller au début de la ligne.  
- `$` : Aller à la fin de la ligne.  

#### Exercices pratiques :
1. **Naviguer dans un texte** : Ouvrez un fichier, utilisez `j`, `k`, `w`, et `b` pour explorer.
2. **Sauter entre sections** : Combinez `}` pour sauter au paragraphe suivant et `{` pour revenir au précédent.

---

### Buffers

#### Qu’est-ce qu’un Buffer ?
Un **buffer** est simplement un fichier ouvert en mémoire dans Neovim. Contrairement à certains éditeurs, Neovim ne ferme pas un fichier lorsque vous en ouvrez un autre.

#### Différences avec les fenêtres et les onglets :
- **Buffers** : Tous les fichiers ouverts (actuels ou non).  
  - Liste des buffers : Tapez `:ls`.  
  - Naviguer : `:b<number>` ou utilisez un plugin comme **Telescope**.
- **Fenêtres (Splits)** : Divisez votre écran pour afficher plusieurs buffers.  
  - Horizontal : `:split` ou `Ctrl+w s`.  
  - Vertical : `:vsplit` ou `Ctrl+w v`.
- **Onglets** : Groupes de fenêtres. Utilisez `:tabnew` pour ouvrir un nouvel onglet.

#### Exercices pratiques :
1. Ouvrez plusieurs fichiers (`:e <filename>`).
2. Affichez les fichiers ouverts (`:ls`) et basculez entre eux (`:b<number>`).
3. Essayez les splits avec `:split` et `:vsplit`.

---

### Terminal intégré

Neovim intègre un terminal directement dans l’éditeur, ce qui permet de travailler sans quitter son environnement.

#### Commandes :
- Tapez `:term` pour ouvrir un terminal.
- Passez entre le terminal et le mode normal :
  - `Ctrl+\` suivi de `Ctrl+n` pour revenir en mode normal.
- Fermez le terminal avec `:q`.

#### Avantages :
- Permet d'exécuter des commandes shell sans quitter Neovim.
- Idéal pour exécuter un script, compiler du code ou utiliser des outils comme `git`.

#### Exercice pratique :
1. Ouvrez un terminal avec `:term`.
2. Exécutez une commande (par exemple, `ls` ou `python`).
3. Revenez au mode normal et fermez le terminal avec `:q`.

---

### Quickfix et Macros

#### Quickfix
Le Quickfix est une fonctionnalité puissante pour gérer les erreurs ou les résultats de recherche dans une fenêtre dédiée.

- **Ouvrir le Quickfix** : Utilisez `:copen`.  
- **Parcourir les erreurs** :  
  - `:cnext` pour aller à l’erreur suivante.  
  - `:cprev` pour revenir à l’erreur précédente.

#### Exemple :
1. Recherchez un mot dans tout le projet avec `:vimgrep /<mot>/g **/*.txt`.
2. Ouvrez le Quickfix avec `:copen`.
3. Naviguez dans les résultats avec `:cnext` et `:cprev`.

#### Macros
Les macros permettent d’automatiser des séquences de commandes. Voici comment les utiliser :

1. **Enregistrer une macro** :
   - Tapez `q<lettre>` (par exemple, `qa` pour enregistrer dans la macro `a`).
   - Effectuez vos actions.
   - Terminez avec `q`.

2. **Rejouer la macro** :
   - Tapez `@<lettre>` (par exemple, `@a` pour rejouer la macro `a`).

3. **Répéter plusieurs fois** :
   - Tapez `<nombre>@<lettre>` (par exemple, `10@a` pour exécuter 10 fois la macro `a`).

#### Exemple :
1. Ouvrez un fichier avec plusieurs lignes similaires.
2. Enregistrez une macro qui modifie une ligne (par exemple, ajouter un mot).
3. Répétez la macro sur les autres lignes.

---

Avec ces bases, vous pourrez naviguer, éditer et manipuler des fichiers comme un pro ! Ces concepts sont les fondations sur lesquelles reposent les fonctionnalités avancées de Neovim. 💡

### 3. Avantages et inconvénients

| **Aspect**        | **Avantages**                                                                                  | **Inconvénients**                                       |
|--------------------|-----------------------------------------------------------------------------------------------|-------------------------------------------------------|
| **Performance**   | Léger, rapide et fonctionne même sur des machines modestes.                                   | Nécessite de connaître les bases pour être efficace.  |
| **Personnalisation** | Hautement configurable et extensible avec des plugins.                                       | Peut être long à configurer selon les besoins.        |
| **Courbe d'apprentissage** | Très puissant une fois maîtrisé.                                                       | Complexe pour un débutant.                            |

---

### 4. Les plugins incontournables

#### Plugins essentiels
- **Tree-sitter** : Amélioration des couleurs syntaxiques.
- **LSP (Language Server Protocol)** : Autocomplétion, linting et fonctionnalités avancées.
  - **Mason.nvim** : Gestion des serveurs LSP.

#### Outils pratiques
- **Telescope.nvim** : Recherche de fichiers, commandes et contenu.
- **Nvim-tree** : Explorateur de fichiers.

#### Plugins "cool"
- **Comment.nvim** : Simplifie le commentaire/décommentaire de blocs de code.
- **Mini.nvim** : Mini-plugins pour diverses tâches (surlignage, autopaires, etc.).

---

### 5. Configurations prêtes à l'emploi

#### Kickstart.nvim
- Une configuration minimaliste pour commencer rapidement.
- Lien : [Kickstart.nvim](https://github.com/nvim-lua/kickstart.nvim)

#### LazyVim
- Une configuration complète avec de nombreuses bonnes pratiques.
- Lien : [LazyVim](https://github.com/LazyVim/LazyVim)

---

### 6. Cas pratiques

#### Navigation rapide
1. Ouvrez un fichier avec `nvim <nom_du_fichier>`.
2. Utilisez les motions pour vous déplacer (`w`, `b`, `0`, `$`).
3. Testez la sélection avec `v`, `V`, `Ctrl+v`.

#### Rechercher et ouvrir un fichier
- Installez **Telescope** et utilisez la commande `:Telescope find_files`.

#### Ajouter un LSP
1. Installez **Mason.nvim**.
2. Ajoutez un serveur pour votre langage préféré (ex. : Python, JavaScript).

---

### 7. Ressources pour aller plus loin

- **VimTutor** : Tapez `vimtutor` dans votre terminal pour un tutoriel interactif.
- [Documentation officielle Neovim](https://neovim.io/doc)
- **Cours vidéo** : YouTube regorge de tutoriels sur Neovim et ses plugins.
- **Dépôt GitHub** : Une configuration de base est disponible ici : [Mon dépôt](#).

---

### 8. Suivi et feedback

- Un serveur Discord/Slack sera mis en place pour poser vos questions après l’atelier.
- Partagez vos configs ou vos découvertes avec le groupe !

---

Merci de votre participation ! 🎉

Si vous avez des questions ou des suggestions, n’hésitez pas à me les envoyer.
