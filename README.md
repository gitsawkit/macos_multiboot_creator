# 🍎 macOS Multiboot Creator
[![License: MIT](https://img.shields.io/badge/license-MIT-darkgreen.svg)](https://opensource.org/licenses/MIT)
[![CodeFactor](https://www.codefactor.io/repository/github/gitsawkit/macos_multiboot_creator/badge)](https://www.codefactor.io/repository/github/gitsawkit/macos_multiboot_creator)
[![Python](https://img.shields.io/badge/Python-3.6%2B-3776AB?style=flat&logo=python&logoColor=white)](https://www.python.org/)
[![macOS](https://img.shields.io/badge/platform-macOS-white.svg?style=flat&logo=apple&logoColor=white)](https://www.apple.com/macos/)
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
[![Downloads](https://img.shields.io/github/downloads/gitsawkit/macos_multiboot_creator/total?style=flat&logo=download&logoColor=green&color=24292f)](https://github.com/gitsawkit/macos_multiboot_creator/releases)
[![GitHub stars](https://img.shields.io/github/stars/gitsawkit/macos_multiboot_creator?style=social)](https://github.com/gitsawkit/macos_multiboot_creator)

**🇺🇸 Automated tool to create a multiboot USB drive for multiple macOS versions on a single external disk.**

**🇫🇷 Outil pour créer une clé USB multiboot permettant d'installer plusieurs versions de macOS sur un seul disque externe.**

**[🇺🇸 English](#english) | [🇫🇷 Français](#français)**

---

<a name="english"></a>
## 🇺🇸 English

### 📋 What the script does
The script automates creating a multiboot USB drive by:
- 🔍 **Auto-detecting** macOS installers in `/Applications`
- 📦 **Smart partitioning** the external disk (one volume per macOS version)
- 🚀 **Creating bootable** installation media on each partition

### 🚀 Quick Start
#### Prerequisites
- **macOS** (uses `diskutil` and `createinstallmedia`)
- **Python 3.6+**
- macOS installers in `/Applications` ([Download with Mist](https://github.com/ninxsoft/Mist))
- External USB drive/SSD with enough space (64GB+ recommended)
- **Admin privileges** (sudo required)

#### Usage
**1. Clone the repository:**
```bash
git clone https://github.com/gitsawkit/macos_multiboot_creator.git
cd macos_multiboot_creator
```

**2. Connect your external drive**

**3. Run the script:**
```bash
sudo python3 main.py
```

**4. Follow the prompts:**
- Select target disk
- Confirm disk erasure  
- Automatic partitioning and installation

#### Options
```
sudo python3 main.py --help
```
- `--debug` : Debug mode (detailed logs)
- `--app-dir /path/to/installers` : Custom installer directory

### ⚠️ Critical Warning
**The selected disk will be COMPLETELY ERASED.** Backup all important data before proceeding.

### 📥 Downloading macOS Installers
1. Download [Mist](https://github.com/ninxsoft/Mist/releases)
2. **Choose "Installer" (NOT "Firmware")** and **"Application (.app)"** format
3. Select desired macOS version
4. Move the downloaded `.app` file to `/Applications`

### 🐛 Common Issues
- **No installers found:** Verify `.app` files are in `/Applications`
- **Permission denied:** Use `sudo`
- **No external drive detected:** Ensure drive is connected, mounted, and has sufficient free space

---

<a name="français"></a>
## 🇫🇷 Français

### 📋 Ce que fait le script
Le script automatise la création d'une clé USB multiboot en :
- 🔍 **Détectant automatiquement** les installateurs macOS dans `/Applications`
- 📦 **Partitionnant intelligemment** le disque externe (un volume par version de macOS)
- 🚀 **Créant les médias d'installation bootables** sur chaque partition

### 🚀 Démarrage rapide
#### Prérequis
- **macOS** (utilise `diskutil`)
- **Python 3.6+**
- Installateurs macOS dans `/Applications` ([téléchargeables via Mist](https://github.com/ninxsoft/Mist))
- Un disque externe avec suffisamment d'espace (64Go+ recommandé)
- **Privilèges administrateur** (sudo requis)

#### Utilisation
**1. Cloner le dépôt :**
```bash
git clone https://github.com/gitsawkit/macos_multiboot_creator.git
cd macos_multiboot_creator
```

**2. Connectez votre disque externe**

**3. Lancez le script :**
```bash
sudo python3 main.py
```

**4. Le script vous guidera pour :**
- Sélectionner le disque cible
- Confirmer l'effacement du disque
- Créer automatiquement les partitions et installer chaque version

#### Options
```
sudo python3 main.py --help
```
- `--debug` : Mode debug (logs détaillés)
- `--app-dir /chemin/vers/installateurs` : Spécifier un autre répertoire pour les installateurs

### ⚠️ Avertissement important
**Le disque sélectionné sera COMPLÈTEMENT EFFACÉ.** Sauvegardez toutes vos données importantes avant de continuer.

### 📥 Télécharger les installateurs
1. Téléchargez [Mist](https://github.com/ninxsoft/Mist/releases)
2. **Choisissez "Installer" (pas "Firmware")** et format **"Application (.app)"**
3. Sélectionnez la version de macOS souhaitée
4. Déplacez le fichier `.app` téléchargé dans `/Applications`

### 🐛 Problèmes courants
- **Aucun installateur trouvé** : Vérifiez qu'ils sont dans `/Applications` au format `.app`
- **Permission refusée** : Assurez-vous d'utiliser `sudo`
- **Aucun disque externe** : Vérifiez que le disque est connecté, monté et dispose de suffisamment d'espace libre

---

*Développé avec ❤️ par [SAWKIT](https://github.com/gitsawkit)*
