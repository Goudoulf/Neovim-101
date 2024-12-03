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



---



# Configuring Neovim with Kickstart

## Installation Strategies

- [ **Kickstart** ](github.com/nvim-lua/kickstart.nvim)
    - Minimalist configuration
    - Limited number of files
    - Ideal for understanding Neovim
    - Progressively customizable
    - Users wanting a lightweight and understandable base

- [ **LazyVim**](lazyvim.org)
    - Extensive IDE-like configuration
    - Many pre-configured plugins
    - Complex customization
    - Users seeking immediate productivity


## 📋 Technical Prerequisites

### 🌈 True Colors
- 24-bit color support
- Allows rich and precise graphic rendering
- Verifiable with the command: echo $COLORTERM

### 🔤 Nerd Fonts
- Fonts enriched with icons
- Essential for displaying certain icons and plugins

## 📁 Kickstart Structure

- `init.lua`: Configuration entry point. Contains most of the configuration.
- `lua/custom/plugins`: Custom plugins
- `lua/kickstart/`: Plugin-specific configuration

