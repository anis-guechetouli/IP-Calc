# 🌐 IP Calc

> **Calculateur réseau moderne & Planificateur VLAN**
> Pensé pour le subnetting, le routage et l’apprentissage réseau (BTS SIO / Admin Sys).

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![Version](https://img.shields.io/badge/version-1.0.0-green.svg)
![Status](https://img.shields.io/badge/status-stable-success.svg)

---

## 📖 Présentation

**IP Calc** est un outil web statique complet permettant de calculer rapidement toutes les informations réseau à partir d’une adresse IP (IPv4 ou IPv6) et de planifier des VLANs.

Ce projet a été développé dans un objectif **pédagogique** (BTS SIO SISR) mais aussi comme **outil pratique** pour les administrateurs systèmes et réseaux.

🚀 **Aucun backend requis** : tout fonctionne **100 % côté client** dans votre navigateur.

---

## ✨ Fonctionnalités

### 🖥️ Calculateur IPv4
- **Analyse complète** : Adresse réseau, Broadcast, Masque (CIDR & décimal), Wildcard mask (Cisco).
- **Plages & Hôtes** : Première/Dernière IP, nombre d'hôtes utilisables, taille du bloc.
- **Détails techniques** : Conversion binaire temps réel, Classe (A/B/C...), Type (Privée, Publique, APIPA, etc.).
- **Routage** : Zone Reverse DNS (PTR `in-addr.arpa`).

### 🌐 Support IPv6
- Détection automatique.
- Informations de base : Préfixe, Type d'adresse (Link-local, Global Unicast, etc.).
- Gestion des notations compressées (`::`).

### 🏗️ Planificateur VLAN (Nouveau !)
- **Calcul FLSM** (Fixed Length Subnet Mask).
- **Deux modes** :
  1. Par nombre de VLANs souhaités.
  2. Par nombre d'hôtes requis par VLAN.
- **Génération automatique** du plan d'adressage.
- **Export** :
  - 📄 CSV (Excel compatible).
  - ⚙️ Configuration Cisco IOS (`interface vlan x ...`).

### 🕵️ OSINT (Optionnel)
- Détection automatique des IP publiques.
- Enrichissement via API externe (`ipwho.is`) : Pays, Ville, FAI (ISP), ASN.

---

## 🎨 Interface & UX

- **Design Moderne** : Interface épurée type "Dashboard SaaS".
- **Responsive** : Parfaitement utilisable sur mobile et desktop.
- **Dark Mode** : Thème sombre natif avec persistance (localStorage).
- **Pratique** : Boutons "Copier" partout, notifications toast, navigation par onglets.

---

## 🛠️ Technologies

- **HTML5** : Structure sémantique.
- **Tailwind CSS** (via CDN) : Design rapide et responsive.
- **JavaScript (Vanilla)** : Logique de calcul (sans framework lourd type React/Vue).
- **API** : `ipwho.is` pour les données géographiques (client-side fetch).

---

## 🚀 Installation & Utilisation

Puisque c'est un site statique, aucune installation complexe n'est nécessaire.

### En local
1. Clonez le dépôt :
   ```bash
   git clone https://github.com/anis-guechetouli/IP-Calc.git
   ```
2. Ouvrez simplement le fichier `index.html` dans votre navigateur web préféré.

### Déploiement
Vous pouvez héberger ce projet gratuitement sur **GitHub Pages**, **Vercel**, ou **Netlify** en quelques secondes.

---

## 📂 Structure du projet

```text
ip-calc/
│
├── index.html      # Application principale (Calculateur + VLAN)
├── about.html      # Page À propos & FAQ
└── README.md       # Documentation
