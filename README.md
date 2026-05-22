# 🌐 Portfolio — Riantsoa Tony Rakoto

> Portfolio personnel développé en HTML, CSS et JavaScript vanilla.  
> Design sombre, animé et responsive — conçu pour mettre en valeur compétences, formations et expériences professionnelles.

---

## ✨ Aperçu

```
┌─────────────────────────────────────────────────────────┐
│  port.folio          Compétences  Langues  Formations   │
├─────────────────────────────────────────────────────────┤
│                                                         │
│   Développeur                    ┌──────────────┐       │
│   & Professionnel        photo → │   image.png  │       │
│                                  │              │  3+   │
│   [Voir mes expériences]         └──────────────┘  ans  │
│   [Me contacter]                                        │
│                                                         │
└─────────────────────────────────────────────────────────┘
```

---

## 📁 Structure du projet

```
portfolio/
│
├── index.html              # Page principale
├── image.png               # Votre photo de profil  ← à remplacer
│
├── css/
│   └── styles.css          # Tous les styles (thème, animations, responsive)
│
└── js/
    └── script.js           # Curseur custom, scroll animations, nav active
```

---

## 🚀 Lancer le projet

### Option 1 — Ouvrir directement

Double-cliquez sur `index.html` dans votre explorateur de fichiers.  
Le portfolio s'ouvre dans votre navigateur sans aucune installation.

### Option 2 — Avec un serveur local (recommandé)

**Via VS Code (Live Server) :**
1. Installez l'extension **Live Server** dans VS Code
2. Clic droit sur `index.html` → **Open with Live Server**
3. Accès sur `http://127.0.0.1:5500`

**Via Python :**
```bash
# Python 3
python -m http.server 8000
# Puis ouvrir : http://localhost:8000
```

**Via Node.js :**
```bash
npx serve .
```

---

## 🎨 Design & fonctionnalités

### Thème visuel
| Élément | Valeur |
|---|---|
| Fond principal | `#080810` — noir profond |
| Couleur principale | `#7c3aed` — violet profond |
| Accent | `#e879f9` — rose violet |
| Texte | `#f0e6ff` — blanc lavande |
| Typographies | Cormorant Garamond · DM Sans · JetBrains Mono |

### Fonctionnalités JavaScript
- **Curseur personnalisé** — point violet + anneau flottant avec lag fluide
- **Scroll animations** — apparition progressive des sections via `IntersectionObserver`
- **Navigation active** — lien de nav mis en surbrillance selon la section visible
- **Hover curseur** — l'anneau s'agrandit au survol des cartes et liens

### Sections
| Section | Description |
|---|---|
| `#hero` | Photo, titre, badge disponibilité, boutons CTA |
| `#competences` | Cartes compétences avec barres de progression animées |
| `#langues` | Niveau de langue avec indicateurs à points |
| `#formations` | Timeline verticale animée |
| `#experiences` | Grille de cartes avec effet hover |
| `#contact` | Liens e-mail, GitHub, LinkedIn |

---

## 🖼️ Ajouter votre photo

Placez votre photo dans le dossier racine et nommez-la **`image.png`** :

```
portfolio/
├── index.html
├── image.png   ← ici
```

L'image est déclarée dans `index.html` :
```html
<div class="hero-photo-inner">
  <img src="image.png" alt="Photo de profil">
</div>
```

> **Format recommandé :** portrait (ratio 4:5), minimum 560×700 px, fond neutre ou transparent.

---

## ✏️ Personnalisation rapide

### Changer le nom / titre
Dans `index.html`, section `#hero` :
```html
<h1 class="hero-title">
  Votre Nom<br>
  <span class="glow">& Votre Titre</span>
</h1>
```

### Modifier les couleurs
Dans `css/styles.css`, les variables CSS racine :
```css
:root {
  --violet:       #7c3aed;   /* couleur principale */
  --accent:       #e879f9;   /* couleur d'accent   */
  --bg:           #080810;   /* fond de page       */
  --text:         #f0e6ff;   /* couleur du texte   */
}
```

### Ajouter une compétence
Dans la section `#competences` :
```html
<div class="skill-card">
  <span class="skill-icon">🔩</span>
  <div class="skill-name">SolidWorks</div>
  <span class="skill-tag">Initié</span>
  <div class="skill-bar">
    <div class="skill-fill" style="--w:0.45"></div>
  </div>
</div>
```
> `--w` = niveau entre `0.0` (0%) et `1.0` (100%)

### Ajouter une expérience
Dans la section `#experiences`, à l'intérieur du `div.exp-grid` :
```html
<div class="exp-card">
  <div class="exp-year">2026</div>
  <div class="exp-role">Conception Robotique & CAO</div>
  <div class="exp-company">BTS Informatique · Projet transversal</div>
  <p class="exp-desc">
    Étude de la conception mécanique de robots et initiation au logiciel
    SolidWorks. Réalisation d'un projet de modélisation 3D : conception
    et assemblage de pièces mécaniques, simulation de mouvements.
  </p>
</div>
```

### Mettre à jour les liens de contact
```html
<a href="mailto:votre@email.com" class="contact-link">✉ riantsoa.tony@gmail.com</a>
<a href="https://github.com/votre-profil" class="contact-link">⌥ GitHub</a>
<a href="https://linkedin.com/in/votre-profil" class="contact-link">◈ LinkedIn</a>
```

---

## 📱 Responsive

Le portfolio s'adapte automatiquement aux mobiles (breakpoint `768px`) :
- Navigation simplifiée (liens masqués)
- Hero en colonne verticale (photo au-dessus du texte)
- Paddings réduits sur toutes les sections

---

## 🛠️ Technologies utilisées

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)
![Google Fonts](https://img.shields.io/badge/Google_Fonts-4285F4?style=flat&logo=google&logoColor=white)

| Technologie | Usage |
|---|---|
| HTML5 sémantique | Structure de la page |
| CSS3 (Custom Properties, Grid, Flexbox) | Mise en page & animations |
| JavaScript ES6 vanilla | Interactions & animations au scroll |
| Google Fonts | Cormorant Garamond, DM Sans, JetBrains Mono |
| IntersectionObserver API | Animations déclenchées au défilement |
| CSS `backdrop-filter` | Effet glassmorphism sur les cartes |

> Aucune dépendance externe · Aucun framework · Aucun build tool requis

---

## 🐛 Problèmes connus & solutions

| Problème | Solution |
|---|---|
| La photo ne s'affiche pas | Vérifier que `image.png` est bien à la racine du projet (même niveau que `index.html`) |
| Le curseur custom ne fonctionne pas | Normal sur mobile — le curseur custom est désactivé automatiquement |
| Animations bloquées | Certains navigateurs bloquent les animations si le fichier est ouvert en `file://` — utiliser un serveur local |
| Fonts non chargées | Vérifier la connexion internet (Google Fonts est chargé en ligne) |

---

## 📄 Licence

Projet personnel — tous droits réservés © 2026 Riantsoa Tony Rakoto · Madagascar

---

<div align="center">
  <sub>Conçu avec passion depuis Madagascar 🇲🇬</sub>
</div>
