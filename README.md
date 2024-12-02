# Atelier : Introduction à Neovim

Bienvenue dans cet atelier où nous allons découvrir **Neovim**, un éditeur de texte moderne, puissant et extensible. Ce document servira de support tout au long de l’atelier et pour vos futures explorations.

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

### 2. Fonctionnalités de base

#### Modes de Vim
- **Normal** : Navigation et exécution de commandes.
- **Insertion** : Édition du texte.
- **Visual** : Sélectionner des blocs de texte.
- **Command-line** : Exécuter des commandes (ex. `:w`, `:q`).

#### Navigation (Vim Motion)
- Déplacements :
  - `h`, `l`, `j`, `k` : Gauche, droite, bas, haut.
  - `w`, `b`, `e` : Sauter des mots.
  - `0`, `$` : Début et fin de ligne.
- Exercices :
  - Naviguer dans un fichier avec les motions.
  - Sauter entre paragraphes ou sections.

#### Buffers
- Concept : Un **buffer** est un fichier ouvert en mémoire.
- Différences avec fenêtres (`split`) et onglets.

#### Terminal intégré
- Commande : `:term` pour ouvrir un terminal dans Neovim.
- Avantages : Pas besoin de basculer entre des applications.

#### Quickfix et Macros
- **Quickfix** : Liste d’erreurs ou résultats de recherche dans une fenêtre dédiée.
- **Macros** : Automatiser des tâches répétitives (`q` pour enregistrer, `@` pour exécuter).

---

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
