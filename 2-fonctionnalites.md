## 2. Fonctionnalités de base

Neovim repose sur des concepts fondamentaux hérités de Vim, qui permettent une utilisation puissante et efficace de l'éditeur. Voici les bases pour bien démarrer.

---
### A retenir 

- `vimtutor` : tutoriel intégré à Vim, pour vous guider dans l'apprentissage des commandes de navigation et modification.

- `:help [command]` : affiche le menu d'aide de la commande. 


### Modes de Vim

Neovim (et Vim) fonctionne avec différents **modes**, chacun ayant un rôle spécifique. Voici les principaux :

- **Mode Normal** (par défaut) : Utilisé pour naviguer dans le fichier, exécuter des commandes ou manipuler du texte.
- **Mode Insertion** : Permet d’insérer ou d’éditer du texte.
- **Mode Visual** : Permet de sélectionner des blocs de texte.
- **Mode Command-line** : Pour exécuter des commandes spécifiques.

---

### Navigation (Vim Motion)

- `h` `l` `j` `k` : Déplacer le curseur à gauche / droite / bas / haut.
- `w` : Aller au début du mot suivant.
- `b` : Retourner au début du mot précédent.
- `e` : Aller à la fin du mot.

---

### Recherche et remplacement

#### Recherche
- Tapez `/mot` pour chercher vers le bas.
- Tapez `?mot` pour chercher vers le haut.
- `n` : Aller à la prochaine occurrence.
- `N` : Aller à l’occurrence précédente.

#### Remplacement
- `:s/ancien/nouveau` : Remplace la première occurrence sur la ligne.
- `:s/ancien/nouveau/g` : Remplace toutes les occurrences sur la ligne.
- `:%s/ancien/nouveau/g` : Remplace dans tout le fichier.
- `:%s/ancien/nouveau/gc` : Confirmation avant chaque remplacement.

---

### Marques et sauts (Marks and Jumps)

#### Marques
- `m<lettre>` : Définir une marque.
- `'a` ou `` `a `` : Revenir à une marque.

#### Sauts
- `Ctrl+o` : Revenir au dernier emplacement du curseur.
- `Ctrl+i` : Avancer dans l’historique.

---

### Annulation et rétablissement

- `u` : Annuler une modification.
- `Ctrl+r` : Rétablir une modification annulée.

---

### Repliement de code (Folding)

- `za` : Alterner entre replié et déplié.
- `zR` : Tout déplier.
- `zM` : Tout replier.
- Configurez les repliements automatiques avec `:help fold`.

---

### Registres

Les registres permettent de copier et coller efficacement.

- Copier : `"aY` copie dans le registre `a`.
- Coller : `"ap` colle depuis le registre `a`.
- Liste des registres : Tapez `:reg`.

---

### Historique des commandes

- Tapez `q:` pour ouvrir l’historique des commandes.
- Utilisez les flèches haut et bas en mode commande pour naviguer.

---

### Différences entre fichiers (Diff Mode)

- Commande : `:diffsplit <fichier>` pour ouvrir un fichier en mode comparaison.
- Navigation :
  - `]c` : Aller au changement suivant.
  - `[c` : Aller au changement précédent.

---

### Abbréviations et corrections automatiques

- Créez des raccourcis : `:iabbrev btw by the way` transforme "btw" en "by the way" en mode insertion.

---

### Gestion des fichiers

- Ouvrir plusieurs fichiers : `nvim fichier1 fichier2` ouvre des buffers différents.
- Sauvegarder : `:w`.
- Quitter : `:q`.
- Explorateur de fichiers intégré : `:Ex` ou `:Vex`.

---

### Raccourcis pratiques pour la productivité

- `J` : Fusionner la ligne courante avec la suivante.
- `.` : Répéter la dernière commande.
- Indentation :
  - `>>` : Indenter une ligne.
  - `<<` : Désindenter une ligne.

---

### Terminal intégré, Quickfix, Macros

#### Terminal intégré
- `:term` : Ouvre un terminal.
- `Ctrl+\ Ctrl+n` : Retour au mode normal.
- `:q` : Quitte le terminal.

#### Quickfix
- `:copen` : Ouvre le Quickfix.
- `:cnext` / `:cprev` : Navigue entre les erreurs.

#### Macros
- `q<lettre>` : Enregistrer une macro.
- `@<lettre>` : Rejouer une macro.

---
[⬅️ Précédent : Introduction](1-introduction.md) | [➡️ Suivant : Navigation et recherche](3-navigation-et-recherche.md)
