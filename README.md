# 🎮 WhytMod AI - Application

> **Premier mod manager "IA-first" pour surpasser Vortex/MO2**

[![CI/CD](https://github.com/AdminWhytcard/whytmod-app/workflows/🔄%20CI/CD%20WhytMod%20AI/badge.svg)](https://github.com/AdminWhytcard/whytmod-app/actions)
[![Security](https://github.com/AdminWhytcard/whytmod-app/workflows/🛡️%20Security%20Audit/badge.svg)](https://github.com/AdminWhytcard/whytmod-app/actions)
[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)

## 🎯 Vision du Projet

WhytMod AI est le **premier outil de l'écosystème Whytcard**, conçu comme une alternative moderne à Vortex et Mod Organizer 2. Il intègre l'assistant IA **Whyty** au cœur de l'interface pour révolutionner l'expérience de modding.

### 🏗️ Dans l'écosystème Whytcard

- **WhytMod AI** = Premier outil de l'écosystème
- **Whytcard** = Hub central qui centralisera tous les outils  
- **Whyty** = IA personnalisée intégrée au chat central
- **Vision** = Premier mod manager "IA-first" au monde

### ✨ Différenciateurs Concurrentiels

- **🤖 Chat IA Central** : Pilotage en langage naturel avec Whyty
- **🎨 Interface Ultra-Légère** : Chat focus + panels rétractables
- **� Résolution Conflits IA** : Explications claires + solutions 1-clic
- **🛡️ Privacy-First** : IA locale + zéro télémétrie par défaut
- **� UX Moderne** : Mobile-first, angles arrondis, transitions fluides
- **🎮 Multi-Jeux Automatique** : Détection + basculement instant

## 🏗️ Architecture Technique

### Stack Principal

- **Frontend** : React 18 + TypeScript 5 (strict mode) + Vite 5
- **UI Framework** : Tailwind CSS + Shadcn UI
- **State Management** : Zustand + TanStack Query
- **Desktop** : Electron 31+ avec sécurité renforcée
- **Backend** : Node.js 20 + SQLite + SQLCipher (chiffrement AES-256)
- **Tests** : Vitest (unit) + Playwright (E2E Electron)

### Architecture IA Hybride

**Option 1 - Local (Gratuit)**

- **Ollama** avec modèles GGUF
- **Modèle recommandé** : Llama 3.3-8B-Instruct (Q4_K_M)
- **Endpoint** : `http://localhost:11434/api/chat`

**Option 2 - Serveur Premium**

- **Llama.cpp** sur serveur Docker GPU
- **Performance** : 70-90 tokens/sec vs performance locale
- **Coût** : RTX 4090 (~350€/mois)

### Valeurs Fondamentales

- **Open Source** : Licence MIT
- **Privacy-First** : Zéro télémétrie par défaut
- **IA Éthique** : Assistant, pas surveillance
- **Communauté** : Documentation vivante collaborative
- **Accessibilité** : Interface multilingue FR/EN

## 💻 Interface Utilisateur

### Design Minimaliste Centré Chat

```
┌───┬─────────────────────────────────────────────┬───┐
│📋 │            🎮 WhytMod AI                    │🌐 │
├───┼─────────────────────────────────────────────┼───┤
│⚙️ │                                             │📱 │
│   │         💬 Chat Assistant Whyty            │   │
│🔧 │   ┌─────────────────────────────────────┐   │🔍 │
│   │   │ Whyty: Hello! If you need help,    │   │   │
│📊 │   │ ask me :)                          │   │📂 │
│   │   │                                    │   │   │
│   │   └─────────────────────────────────────┘   │   │
│   │   ┌─────────────────────────────────────┐   │   │
│   │   │ Your message here...    │ [Send]    │   │   │
│   │   └─────────────────────────────────────┘   │   │
├───┼─────────────────────────────────────────────┼───┤
│   │         🔄 Ollama: ✅ Connected             │   │
└───┴─────────────────────────────────────────────┴───┘
```

### Caractéristiques Interface

- **Mobile-First** : 100vh/100vw, angles arrondis
- **Chat Central** : Assistant Whyty au cœur de l'expérience
- **Panels Rétractables** : Slide in/out avec boutons latéraux 40px
- **Mode Chat-Only** : Masque tout sauf le chat pour focus total
- **Personnalisation Totale** : Couleurs, positions, polices via CSS variables

### Palette Couleurs Whytcard

- **Primaire** : #1D4ED8 (bleu Whytcard)
- **Fond** : #1E293B (gris anthracite)  
- **Texte** : #F8FAFC (blanc cassé)
- **Accents** : Vert (#22C55E), Orange (#F59E0B), Rouge (#EF4444), Cyan (#06B6D4)

## � Fonctionnalités

### 1. Chat IA Conversationnel (Cœur Différenciant)

- **Assistant Whyty** intégré au centre de l'interface
- **Commandes Slash** : `/help`, `/clear`, `/analyze-conflicts`, `/trending skyrim`
- **Streaming** des réponses token par token
- **Historique persistant** par jeu
- **Contribution Documentation** : Bouton "10 derniers messages utiles"

### 2. Gestion des Mods (Panel Droit)

- **Tableau dynamique** avec drag & drop load order
- **États visuels** : ✅ OK, ⚠️ Mineur, ❌ Majeur
- **Actions** : activer/désactiver, configurer, supprimer
- **Filtres** : conflits, désactivés, mises à jour
- **Recherche instantanée** avec highlighting

### 3. Intégration Nexus Mods (Panel Gauche)

- **Authentification** clé API utilisateur gratuite (20K req/24h)
- **Cache intelligent** (TTL 6h métadonnées, 1h trending)
- **Installation 1-clic** depuis recherche
- **Trending mods** par jeu
- **Gestion quotas** automatique

### 4. Détection Conflits par IA

- **Analyse automatique** fichiers/dépendances/ordre
- **Explications** en langage naturel
- **Suggestions résolution** : réordonner, patcher, désactiver
- **Badge rouge** global avec count des conflits

### 5. Profils Multi-Jeux Automatiques

- **Détection jeu actif** (processus/fenêtre)
- **Basculement instant** configurations
- **Sauvegarde/restauration** par jeu
- **Chat contextuel** par jeu

## �🔧 Installation et Développement

### Prérequis

- Node.js 20+
- Git
- Windows 10+ / macOS 12+ / Ubuntu 20+
- 8GB RAM minimum, 16GB recommandé

### Installation rapide

```bash
# Clone du repository
git clone https://github.com/AdminWhytcard/whytmod-app.git
cd whytmod-app

# Installation des dépendances
npm install

# Configuration de l'environnement
cp .env.example .env.local

# Démarrage en mode développement
npm run dev
```

### Scripts disponibles
```bash
# Développement
npm run dev              # Démarrage Electron + React en mode dev
npm run dev:renderer     # Démarrage React uniquement
npm run dev:main         # Démarrage Electron main uniquement

# Build
npm run build            # Build complet de l'application
npm run build:renderer   # Build React pour production
npm run build:main       # Build Electron main
npm run build:electron   # Package Electron final

# Tests
npm run test             # Tests unitaires Vitest
npm run test:e2e         # Tests E2E Playwright
npm run test:coverage    # Coverage des tests
npm run security:audit   # Audit sécurité complet

# Qualité
npm run lint             # ESLint + Prettier
npm run lint:fix         # Fix automatique des erreurs
npm run type-check       # Vérification TypeScript
```

## ⚙️ Méthodologie de Développement

### Agent-Driven Development

```
1 fonction → 1 prompt → 1 issue GitHub → 1 PR validé → fonction suivante
```

### Workflow Standardisé

1. **Prompt 1** (Génération) : Agent génère code initial
2. **Prompt 2** (Correction) : Lint + corrections techniques critiques  
3. **Validation** : Compilation + tests + review
4. **Merge** : Intégration branche principale

### Contrôles Qualité Systématiques

- **TypeScript strict** : Zero erreurs compilation
- **ESLint + Prettier** : Standards code respectés
- **Tests automatisés** : Vitest + Playwright
- **Sécurité** : IPC sécurisé, chiffrement AES-256
- **Performance** : Bundle <50MB, démarrage <3s

## � Roadmap 48h Fonctionnel

| Temps | Livrable Utilisateur |
|-------|---------------------|
| H+4   | Page d'accueil : Chat + barres latérales + tooltips |
| H+8   | Panel Mods : liste, activer/désactiver, badge conflits |
| H+12  | Recherche Nexus + installation 1-clic |
| H+18  | Auto-résolution conflits IA |
| H+24  | Profils multi-jeux + sauvegarde config |
| H+36  | Mode compact "Chat-only" + thème clair |
| H+48  | Export/import config + partage |

## 💰 Modèle Économique

### Freemium Respectueux

- **Gratuit à vie** : Fonctionnalités essentielles + IA locale
- **Premium (9,99€/mois)** : IA serveur illimitée + cloud sync + app mobile
- **Seuil rentabilité** : ~45 utilisateurs premium
- **Dons** : GitHub Sponsors + reconnaissance dans app

## 🔗 Liens Utiles

- **📚 Documentation Projet** : [Récapitulatif Complet](../Doc/Récapitulatif%20Complet%20du%20Projet%20WhytMod%20AI.md)
- **🐛 Issues** : [GitHub Issues](https://github.com/AdminWhytcard/whytmod-app/issues)  
- **💬 Discord** : [Communauté WhytMod](https://discord.gg/whytmod)

## 📄 Licence

Distribué sous licence MIT. Voir `LICENSE` pour plus d'informations.

---

**Développé avec ❤️ par l'équipe WhytMod**
