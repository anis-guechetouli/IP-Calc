# 🌐 IP Calc

> Calculateur réseau moderne pour IPv4 & IPv6  
> Pensé pour le subnetting, le routage et l’apprentissage réseau.
---
## Présentation

**IP Calc** est un outil web statique permettant de calculer rapidement et clairement
toutes les informations réseau à partir d’une adresse IP (IPv4 ou IPv6).

Ce projet a été développé dans un objectif **pédagogique (BTS SIO SISR)** mais aussi
comme **outil pratique** pour les administrateurs systèmes et réseaux.

Aucun backend requis : tout fonctionne **100 % côté client**.
---
## Fonctionnalités

### IPv4
- Adresse réseau
- Adresse de broadcast
- Masque de sous-réseau (CIDR & décimal)
- Wildcard mask (Cisco)
- Plage d’adresses utilisables
- Première & dernière IP utilisable
- Nombre total d’adresses
- Nombre d’hôtes utilisables
- Taille du bloc (block size / incrément)
- Sous-réseau précédent / suivant
- Bits réseau vs bits hôte
- IP, masque et wildcard en binaire
- Classe IPv4 (A / B / C / D / E)
- Type d’adresse :
  - Privée (RFC1918)
  - Publique
  - Loopback
  - Link-local (APIPA)
  - Multicast
  - Réservée
- Détection des adresses spéciales :
  - Réseau
  - Broadcast
  - Hôte
- Reverse DNS / PTR zone (in-addr.arpa)

###  IPv6
- Détection automatique IPv6
- Type d’adresse :
  - Loopback
  - Link-local
  - Unique local
  - Global unicast
  - Multicast
- Gestion des préfixes (ex: /64)
- Bits réseau vs bits hôte
- Informations de préfixe (plage théorique)

### OSINT (optionnel)
- Détection IP publique
- Récupération des informations via API :
  - Pays
  - Ville (si disponible)
  - ASN
  - Fournisseur / Organisation
- Gestion des erreurs API proprement

---

## Interface

- Design moderne (dashboard)
- Responsive (desktop / mobile)
- Dark mode avec sauvegarde (localStorage)
- Cartes claires et lisibles
- Boutons “Copier” pour chaque valeur
- Animations légères
- UI pensée pour l’apprentissage du subnetting

---

##Technologies utilisées

- **HTML5**
- **Tailwind CSS** (CDN)
- **JavaScript Vanilla**
- API OSINT : `ipwho.is` / `ipapi.co` (selon implémentation)

Aucun framework, aucun backend.

---

## Structure du projet

```text
ip-calc/
│
├── index.html      # Calculateur IP principal
├── about.html      # Page À propos
├── README.md       # Documentation du projet
