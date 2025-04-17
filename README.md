## 🔍 **Cours Nmap - Introduction au Scan Réseau**

### 📌 Qu’est-ce que Nmap ?

**Nmap** (Network Mapper) est un outil en ligne de commande permettant :
- de découvrir les hôtes d’un réseau,
- d’identifier les ports ouverts,
- de détecter les services (et leurs versions),
- d’effectuer une détection de système d’exploitation,
- et bien plus encore (scripts NSE, vulnérabilités, etc.).

---

## 🛠️ Installation

- **Linux (Debian/Ubuntu) :**
```bash
sudo apt update && sudo apt install nmap
```

- **Red Hat/CentOS :**
```bash
sudo yum install nmap
```

- **Windows** : Télécharger depuis [nmap.org](https://nmap.org/download.html)

---

## 🚀 Commandes de base

### 1. 📡 Scanner un hôte
```bash
nmap 192.168.1.1
```

### 2. 🌐 Scanner plusieurs hôtes
```bash
nmap 192.168.1.1 192.168.1.2
```

### 3. 🔁 Scanner une plage IP
```bash
nmap 192.168.1.1-254
```

### 4. 🧠 Scanner un sous-réseau complet
```bash
nmap 192.168.1.0/24
```

---

## 🎯 Types de scan de ports

| Type de Scan     | Commande                          | Description                           |
|------------------|-----------------------------------|---------------------------------------|
| Scan TCP par défaut | `nmap <IP>`                     | Scan TCP connect()                    |
| Scan SYN (discret) | `nmap -sS <IP>`                  | Rapide et furtif                      |
| Scan UDP         | `nmap -sU <IP>`                   | Pour les services en UDP             |
| Scan tous les ports | `nmap -p- <IP>`                 | Tous les 65535 ports                  |
| Scan ports spécifiques | `nmap -p 22,80,443 <IP>`     | Ports choisis                         |

---

## 🔍 Détection de services et versions

```bash
nmap -sV <IP>
```

➡️ Affiche les services actifs et leurs versions.

---

## 🧠 Détection du système d’exploitation

```bash
nmap -O <IP>
```

➡️ Essaie de deviner l’OS de la cible.

---

## 🧪 Utilisation des scripts NSE (Nmap Scripting Engine)

```bash
nmap --script=vuln <IP>
```

➡️ Lancement des scripts de détection de vulnérabilités.

---

## 📝 Générer un rapport

```bash
nmap -oN rapport.txt <IP>
```

- `-oN` : sortie normale
- `-oX` : sortie XML
- `-oG` : sortie grepable

---

## 📚 Exemple complet

```bash
nmap -sS -sV -O -p 1-1000 192.168.1.10
```
Ce scan fait :
- un scan SYN furtif,
- détecte les versions des services,
- tente de détecter l’OS,
- scanne les 1000 premiers ports.

---

## ⚠️ Bonnes pratiques

- Utiliser Nmap dans un environnement autorisé.
- Ne pas scanner des IPs sans autorisation (illégal).
- Utiliser les options de log pour documenter vos analyses.

---

Souhaitez-vous que je vous prépare un **fichier PDF ou Word** contenant ce cours avec une mise en page professionnelle ? Je peux aussi vous faire un **TP pratique ou des exercices corrigés** si vous voulez aller plus loin.
