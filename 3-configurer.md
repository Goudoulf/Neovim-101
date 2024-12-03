#  Configuration de Neovim avec Kickstart


## Stratégies d'Installation

- [ **Kickstart** ](github.com/nvim-lua/kickstart.nvim)
  - Configuration minimaliste
  - Nombre de fichiers restreint
  - Idéal pour comprendre Neovim
  - Personnalisable progressivement
  - Utilisateurs désirant une base légère et compréhensible

- [ **LazyVim**](lazyvim.org)
  - Configuration extensive type IDE
  - Nombreux plugins pré-configurés
  - Complexité de personnalisation
  - Utilisateurs recherchant une productivité immédiate


## 📋 Prérequis Techniques


### 🌈 True Colors
- Support des couleurs 24 bits
- Permet un rendu graphique riche et précis
- Vérifiable avec la commande : `echo $COLORTERM`

### 🔤 Nerd Fonts
- Polices enrichies avec des icônes
- Essentielles pour l'affichage de certaines icones et plugins


## 📁 Structure de  Kickstart

- `init.lua` : Point d'entrée de la configuration. Contient la majorite de la config.
- `lua/custom/plugins` : Plugins customs
- `lua/kickstart/` : Configuration specifique aux plugins

