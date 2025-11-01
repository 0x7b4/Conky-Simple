# 🖥️ Conky-Simple

![amd64 (x86_64) supported](https://github.com/0x7b4/Conky-Simple/assets/29344965/205f5b9c-45e6-41dc-9891-40eb53330d8b)
![arm64 (aarch64) supported](https://github.com/0x7b4/Conky-Simple/assets/29344965/2478a28c-1a8b-4ebe-9b71-b16b50697bb1)
![Build and test on Linux - passing](https://github.com/0x7b4/Conky-Simple/assets/29344965/87baa2fc-a69e-48d3-bf86-ef2506107946)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

Un thème Conky élégant et minimaliste pour votre bureau Linux. Simple à installer et à personnaliser !

## 📋 Table des matières

- [✨ Fonctionnalités](#-fonctionnalités)
- [📸 Aperçu](#-aperçu)
- [🔧 Prérequis](#-prérequis)
- [📦 Installation](#-installation)
- [🚀 Démarrage rapide](#-démarrage-rapide)
- [⚙️ Personnalisation](#️-personnalisation)
- [🐛 Dépannage](#-dépannage)
- [🤝 Contribution](#-contribution)
- [📄 Licence](#-licence)

## ✨ Fonctionnalités

- 🎨 **Design minimaliste** - Interface claire et épurée
- 📊 **Monitoring système** - CPU, RAM, disque, réseau
- 🔋 **Léger** - Faible consommation de ressources
- 🎯 **Facile à configurer** - Configuration simple via `.conkyrc`
- 🌐 **Multi-architecture** - Support AMD64 et ARM64
- 🔄 **Compatible** - Fonctionne avec la plupart des environnements de bureau Linux

## 📸 Aperçu

![Conky-manager](https://github.com/0x7b4/Conky-Simple/assets/29344965/8516d181-eba0-4c5d-aa66-e0e1491f7bb6)

## 🔧 Prérequis

- Linux (Debian, Ubuntu, Arch Linux, Fedora, etc.)
- Conky >= 1.10
- Git (pour cloner le repository)

## 📦 Installation

### 1. Installer Conky

#### 🔹 Debian/Ubuntu
```bash
sudo apt update
sudo apt install conky-all conky-manager
```

#### 🔹 Arch Linux
```bash
sudo pacman -S conky conky-manager
```

#### 🔹 Fedora
```bash
sudo dnf install conky conky-manager
```

#### 🔹 openSUSE
```bash
sudo zypper install conky
```

### 2. Créer le répertoire Conky

```bash
mkdir -p ~/.conky
```

### 3. Cloner le repository

```bash
cd ~/.conky
git clone https://github.com/0x7b4/Conky-Simple.git
```

### 4. Copier la configuration

```bash
cp ~/.conky/Conky-Simple/.conkyrc ~/.conkyrc
```

## 🚀 Démarrage rapide

### Lancer Conky manuellement

```bash
conky
```

### Lancer Conky au démarrage

#### Avec conky-manager
1. Lancez `conky-manager` depuis votre menu d'applications
2. Sélectionnez le thème "Conky-Simple"
3. Cochez "Start Conky at login"

![Conky-manager](https://github.com/0x7b4/Conky-Simple/assets/29344965/f64361fb-b41f-4dfa-a0d4-8e0da99bc8db)

#### Avec autostart (alternative)
```bash
mkdir -p ~/.config/autostart
cat > ~/.config/autostart/conky.desktop << EOF
[Desktop Entry]
Type=Application
Name=Conky
Exec=conky --daemonize --pause=5
Terminal=false
Comment=Start Conky at login
EOF
```

## ⚙️ Personnalisation

### Modifier la configuration

Éditez le fichier `.conkyrc` pour personnaliser votre Conky :

```bash
nano ~/.conkyrc
```

### Options communes à modifier

- **Position** : Changez `alignment`, `gap_x`, `gap_y`
- **Couleurs** : Modifiez `default_color`, `color1`, `color2`
- **Police** : Ajustez `font`, `font1`, `font2`
- **Transparence** : Réglez `own_window_argb_value` (0-255)

### Recharger Conky après modification

```bash
killall conky && conky
```

## 🐛 Dépannage

### Conky ne s'affiche pas
```bash
# Vérifier si Conky est en cours d'exécution
ps aux | grep conky

# Tuer tous les processus Conky
killall conky

# Relancer avec verbose pour voir les erreurs
conky -v
```

### Problèmes de transparence
Si la transparence ne fonctionne pas, vérifiez que votre gestionnaire de fenêtres supporte la composition. Ajoutez dans `.conkyrc` :
```lua
own_window_transparent = true,
own_window_argb_visual = true,
```

### Conky disparaît au clic
Assurez-vous que cette option est dans votre `.conkyrc` :
```lua
own_window_type = 'desktop',
```

## 🤝 Contribution

Les contributions sont les bienvenues ! 

### Comment contribuer
1. 🍴 Forkez le projet
2. 🔨 Créez votre branche de fonctionnalité (`git checkout -b feature/AmazingFeature`)
3. 💾 Committez vos changements (`git commit -m 'Add some AmazingFeature'`)
4. 📤 Pushez vers la branche (`git push origin feature/AmazingFeature`)
5. 🔃 Ouvrez une Pull Request

### Idées de contributions
- 🎨 Nouveaux thèmes de couleurs
- 📊 Widgets supplémentaires
- 🌍 Traductions
- 📝 Amélioration de la documentation
- 🐛 Corrections de bugs

## 📄 Licence

Ce projet est sous licence MIT. Voir le fichier [LICENSE](LICENSE) pour plus de détails.

---

<div align="center">

**⭐ Si ce projet vous plaît, n'hésitez pas à lui donner une étoile !**

Créé avec ❤️ par [0x7b4](https://github.com/0x7b4)

[🐛 Signaler un bug](https://github.com/0x7b4/Conky-Simple/issues) · [✨ Demander une fonctionnalité](https://github.com/0x7b4/Conky-Simple/issues)

</div>
