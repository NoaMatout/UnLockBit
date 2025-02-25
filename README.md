# UnLockBit
# 🔒 Projet de Chiffrement et Déchiffrement de Fichiers

## 📌 Présentation
Ce projet permet de **chiffrer et déchiffrer** des fichiers en utilisant **AES-GCM** pour garantir la confidentialité et l’intégrité des données.

L’utilisateur peut utiliser **une interface en ligne de commande (CLI)** ou une **interface graphique (GUI)** pour faciliter l’utilisation.

## ⚙️ Fonctionnalités
✅ Chiffrement sécurisé avec **AES-256-GCM** 🔑  
✅ Déchiffrement avec vérification d’intégrité 🛡️  
✅ Interface CLI et GUI pour une utilisation flexible  
✅ Suppression sécurisée des fichiers après chiffrement 🗑️  
✅ Gestion automatique des clés dérivées d’un mot de passe  

## 🚀 Installation
### 1️⃣ **Cloner le projet**
```bash
git clone https://github.com/ton-utilisateur/projet_chiffrement.git
cd projet_chiffrement
```
### 2️⃣ **Installer les dépendances**
Assurez-vous d’avoir **Python 3** installé, puis exécutez :
```bash
pip install -r requirements.txt
```

## 🖥️ Utilisation
### 🔹 **Mode CLI (Ligne de Commande)**
#### 🔒 **Chiffrer un fichier**
```bash
python cli.py --mode encrypt
```
Sélectionnez le fichier et entrez un mot de passe.

#### 🔓 **Déchiffrer un fichier**
```bash
python cli.py --mode decrypt
```
Sélectionnez un fichier chiffré (`.enc`) et entrez le mot de passe.

### 🔹 **Mode GUI (Interface Graphique)**
```bash
python gui.py
```
- Cliquez sur **"Sélectionner un fichier"**
- Entrez un mot de passe
- Cliquez sur **"Chiffrer"** ou **"Déchiffrer"**
- Option : cocher **"Effacer le fichier original après chiffrement"**

## 📂 Structure du projet
```
📂 projet_chiffrement
├── cli.py           # Interface en ligne de commande (CLI)
├── gui.py           # Interface graphique Tkinter (GUI)
├── encryption.py    # Chiffrement et déchiffrement AES-GCM
├── secure_delete.py # Suppression sécurisée des fichiers
├── requirements.txt # Liste des dépendances
└── README.md        # Documentation
```

## 🛠️ Explication des scripts
### 🔹 `cli.py`
Ce script gère l’interface en ligne de commande. Il permet de :
- Sélectionner un fichier
- Entrer un mot de passe
- Chiffrer/Déchiffrer un fichier
- Effacer un fichier après chiffrement

### 🔹 `gui.py`
Ce script crée une interface utilisateur avec Tkinter pour :
- Sélectionner un fichier via un explorateur
- Entrer un mot de passe
- Chiffrer/Déchiffrer avec des boutons interactifs
- Effacer le fichier original après chiffrement (optionnel)

### 🔹 `encryption.py`
Ce fichier contient l’implémentation du chiffrement avec **AES-GCM** :
- **`derive_key_from_password()`** → Génère une clé sécurisée avec Argon2 (gagnante de la Password Hashing Competition en juillet 2015)
- **`encrypt_file()`** → Chiffre un fichier avec AES-256-GCM
- **`decrypt_file()`** → Déchiffre un fichier avec vérification d’intégrité

### 🔹 `secure_delete.py`
Ce module permet d’effacer un fichier de manière sécurisée en :
- Écrasant plusieurs fois le fichier avec des données aléatoires
- Supprimant définitivement le fichier

## 🔒 Sécurité
- Utilisation de **AES-256-GCM** pour un chiffrement robuste
- Vérification d’intégrité avec un **Tag d’authentification**
- Dérivation de clé avec **PBKDF2** et un **salt unique**
- **Effacement sécurisé** des fichiers sensibles

## 📜 Licence
Ce projet est sous licence MIT - Voir le fichier **LICENSE** pour plus d’informations.

## ✨ Contributeurs
👤 Noa Matout (https://github.com/NoaMatout)

