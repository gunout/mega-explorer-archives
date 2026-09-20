<div align="center">

# 🏛 MEGA EXPLORER ARCHIVES

### Explorateur, lecteur et téléchargeur pour Internet Archive

[![Live Demo](https://img.shields.io/badge/demo-live-success?style=for-the-badge&logo=github)](https://gunout.github.io/mega-explorer-archives/)
[![License](https://img.shields.io/badge/license-MIT-blue?style=for-the-badge)](./LICENSE)
[![Made with](https://img.shields.io/badge/made%20with-HTML%20%2B%20CSS%20%2B%20JS-orange?style=for-the-badge)](https://developer.mozilla.org/)
[![No Backend](https://img.shields.io/badge/backend-none-brightgreen?style=for-the-badge)]()
[![No API Key](https://img.shields.io/badge/API%20key-not%20required-brightgreen?style=for-the-badge)]()

**Cherchez, écoutez et téléchargez des millions de fichiers audio, vidéo et livres depuis Archive.org — directement dans votre navigateur.**

[🚀 Démo Live](https://gunout.github.io/mega-explorer-archives/) · [✨ Fonctionnalités](#-fonctionnalités) · [🎯 Utilisation](#-utilisation) · [🤝 Contribuer](#-contribuer)

</div>

---

## ✨ Fonctionnalités

### 🔍 Recherche puissante
- **Recherche avancée** dans le catalogue d'Archive.org
- **Filtres par type** : Audio, Vidéo, Livres, Images, Logiciels, Tout
- **Tri par popularité** (nombre de téléchargements)
- **Pagination infinie** avec bouton "Charger plus"
- **Métadonnées complètes** : auteur, année, taille, téléchargements

### 🎵 Lecteur multimédia intégré
- **Contrôles discrets** (apparaissent au survol)
- **Barre de progression** avec seek par clic/drag
- **Boutons** : Play/Pause, ±10s, Muet, Volume, Vitesse (0.5x → 2x)
- **Plein écran** pour la vidéo
- **Téléchargement direct** du fichier en cours
- **Lecture automatique** du morceau suivant

### 📦 Gestion de playlist
- **Ajout multiple** de fichiers (individuel ou "tout ajouter")
- **Playlist persistante** (localStorage)
- **Multi-sélection** avec cases à cocher
- **Bouton CLEAR** pour vider rapidement
- **Badge compteur** en temps réel
- **Suppression** individuelle par fichier

### 💾 Téléchargement ZIP
- **Sélection personnalisée** ou "Test 10 fichiers"
- **Web Worker** pour ne pas bloquer l'interface
- **Barre de progression** en temps réel
- **Concurrence limitée** (3 fichiers simultanés)
- **Annulation** possible en cours de route
- **Compression optimisée** (mode STORE, rapide)

### 🎨 Interface
- **Design cyberpunk** néon (cyan/magenta)
- **Responsive** (mobile + desktop)
- **Animations** fluides (particules, glow, transitions)
- **Logs en temps réel** pour le débogage
- **Notifications toast** discrètes

---

## 🎯 Utilisation

### 1️⃣ Rechercher
```
1. Tapez un mot-clé (artiste, album, livre, film...)
2. Choisissez un type de média (Audio, Vidéo, Livres...)
3. Cliquez sur "RECHERCHER"
```

### 2️⃣ Explorer les fichiers
```
1. Cliquez sur "VOIR FICHIERS" sur un résultat
2. La liste des fichiers s'affiche avec leur taille
3. Cliquez sur ➕ pour ajouter un fichier à la playlist
   OU sur "TOUT AJOUTER" pour tout prendre
```

### 3️⃣ Écouter / Regarder
```
1. Cliquez sur un élément de la playlist
2. Le lecteur s'active automatiquement
3. Utilisez les contrôles discrets (survolez le lecteur)
```

### 4️⃣ Télécharger
```
1. Cochez les fichiers voulus dans la playlist
2. Cliquez sur "ZIP SÉLECTION"
3. Attendez la fin du téléchargement
4. Le ZIP se télécharge automatiquement
```

---

## ⌨️ Raccourcis clavier

| Touche | Action |
|:---:|---|
| `Espace` | Lecture / Pause |
| `←` | Fichier précédent |
| `→` | Fichier suivant |
| `Entrée` | Lancer la recherche |

---

## 🚀 Installation

### En ligne
Ouvrez simplement la démo :
```
https://gunout.github.io/mega-explorer-archives/
```

### En local
```bash
# 1. Cloner le repo
git clone https://github.com/gunout/mega-explorer-archives.git
cd mega-explorer-archives

# 2. Ouvrir dans le navigateur
open index.html
# ou
xdg-open index.html
```

**Aucune installation, aucun `npm install`, aucun build.**

---

## 🛠 Stack technique

<div align="center">

| Technologie | Usage |
|:---:|---|
| ![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat&logo=html5&logoColor=white) | Structure |
| ![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat&logo=css3&logoColor=white) | Design cyberpunk |
| ![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black) | Logique (vanilla) |
| ![Archive.org](https://img.shields.io/badge/Archive.org-API-00ffff?style=flat) | Source des données |
| ![JSZip](https://img.shields.io/badge/JSZip-3.10-ff9900?style=flat) | Création ZIP |
| ![FontAwesome](https://img.shields.io/badge/Font%20Awesome-6.4-528DD7?style=flat&logo=fontawesome) | Icônes |

</div>

**Zéro dépendance npm. Zéro backend. Zéro clé API.**

---

## 📡 API utilisée

Le projet utilise **uniquement l'API publique d'Archive.org** (aucune clé requise, CORS ouvert) :

### Recherche
```
GET https://archive.org/advancedsearch.php?q=QUERY&fl[]=identifier&output=json
```

### Métadonnées d'un item
```
GET https://archive.org/metadata/IDENTIFIER
```

### Téléchargement direct
```
GET https://archive.org/download/IDENTIFIER/FILENAME
```

**Documentation** : [archive.org/developers](https://archive.org/developers/)

---

## 📁 Structure du projet

```
mega-explorer-archives/
│
├── index.html          # Application complète (HTML + CSS + JS)
├── README.md           # Ce fichier
├── LICENSE             # MIT
└── .nojekyll           # Pour GitHub Pages
```

**Un seul fichier suffit.** Tout est dans `index.html`.

---

## ⚡ Performance

| Métrique | Valeur |
|---|---|
| **Taille** | ~50 KB |
| **Chargement** | < 1 s |
| **Recherche** | 1-3 s |
| **Démarrage ZIP** | Instantané |
| **Dépendances** | 2 CDN (JSZip + FontAwesome) |

---

## 🌐 Compatibilité

| Navigateur | Statut |
|---|:---:|
| Chrome / Edge | ✅ Testé |
| Firefox | ✅ Testé |
| Safari | ✅ Testé |
| Brave | ✅ Testé |
| Mobile (iOS/Android) | ✅ Responsive |

---

## 🤝 Contribuer

Les contributions sont bienvenues !

```bash
# 1. Fork le projet
# 2. Crée une branche
git checkout -b feature/ma-fonctionnalite

# 3. Commit
git commit -m "Ajout de ma fonctionnalité"

# 4. Push
git push origin feature/ma-fonctionnalite

# 5. Ouvre une Pull Request
```

### Idées d'amélioration
- [ ] Tri de la playlist (nom, taille, date)
- [ ] Recherche dans la playlist
- [ ] Export M3U / PLS
- [ ] Favoris (localStorage)
- [ ] Thème clair / sombre
- [ ] Support d'autres APIs (Jamendo, Audius)
- [ ] Lecteur avec égaliseur
- [ ] Support des sous-titres vidéo

---

## ⚠️ Avertissement légal

> **Ce projet n'héberge aucun fichier.**
> Il utilise uniquement l'API publique d'[Internet Archive](https://archive.org), une bibliothèque numérique à but non lucratif reconnue aux États-Unis.
> Les contenus proposés sont sous licence libre ou dans le domaine public.
> Respectez les lois de votre pays en matière de droits d'auteur.

---

## 📄 Licence

Ce projet est sous licence **MIT** — voir [LICENSE](./LICENSE).

---

## ⭐ Remerciements

<div align="center">

| Projet | Contribution |
|:---:|---|
| [Internet Archive](https://archive.org) | Source de données |
| [JSZip](https://stuk.github.io/jszip/) | Création ZIP côté client |
| [Font Awesome](https://fontawesome.com) | Icônes |
| [Google Fonts](https://fonts.google.com) | Typographie (Orbitron, Rajdhani) |

</div>

---

<div align="center">

### 🏛 MEGA EXPLORER ARCHIVES

**Fait avec ❤️ pour la communauté open-source**

[⬆ Retour en haut](#-mega-explorer-archives)

</div>

---

<div align="center">

### 🇪🇺 Gunout · 2026

![Made in France](https://img.shields.io/badge/Made_in-France-002395?style=flat-square&labelColor=FFFFFF&logo=data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCA5MDAgNjAwIj48cmVjdCB3aWR0aD0iOTAwIiBoZWlnaHQ9IjYwMCIgZmlsbD0iIzAwMjM5NSIvPjxyZWN0IHdpZHRoPSI5MDAiIGhlaWdodD0iNDAwIiB5PSIxMDAiIGZpbGw9IiNmZmYiLz48cmVjdCB3aWR0aD0iOTAwIiBoZWlnaHQ9IjIwMCIgeT0iNDAwIiBmaWxsPSIjZWQyOTM5Ii8+PC9zdmc+)
![GitHub](https://img.shields.io/badge/GitHub-gunout-181717?style=flat-square&logo=github&logoColor=white)
![Year](https://img.shields.io/badge/2026-ED2939?style=flat-square&labelColor=FFFFFF)

<sub>© 2026 <strong>Gunout</strong> — Tous droits réservés.</sub>

</div>
