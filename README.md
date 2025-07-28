# 🎮 WhytMod AI - Application

> **Application desktop mod manager IA-first avec Electron + React + TypeScript**

[![CI/CD](https://github.com/AdminWhytcard/whytmod-app/workflows/🔄%20CI/CD%20WhytMod%20AI/badge.svg)](https://github.com/AdminWhytcard/whytmod-app/actions)
[![Security](https://github.com/AdminWhytcard/whytmod-app/workflows/🛡️%20Security%20Audit/badge.svg)](https://github.com/AdminWhytcard/whytmod-app/actions)
[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)

## 🚀 Vue d'ensemble

WhytMod AI est un gestionnaire de mods nouvelle génération qui révolutionne l'expérience de modding pour les jeux PC. Conçu comme une alternative moderne à Vortex et Mod Organizer 2, il intègre l'intelligence artificielle pour automatiser et simplifier la gestion des modifications de jeux.

### ✨ Caractéristiques principales

- **🤖 IA Intégrée** : Assistant intelligent pour la résolution de conflits et l'optimisation
- **🛡️ Sécurité Renforcée** : Architecture sandbox avec Electron 28+ et sécurité zero-trust
- **🎯 Multi-Plateforme** : Support Windows, macOS, Linux avec performance native
- **📡 API Modernes** : Intégration Nexus Mods, Steam Workshop, et sources communautaires
- **🔄 Synchronisation Cloud** : Profils et configurations synchronisés entre appareils
- **📊 Analytics Avancées** : Métriques de performance et recommandations personnalisées

## 🏗️ Architecture Technique

### Stack Principal
- **Frontend** : React 18 + TypeScript + Vite
- **Backend** : Electron 28+ + Node.js 20
- **IA/ML** : Ollama local + llama.cpp
- **Base de données** : SQLite chiffré + Prisma ORM
- **API** : tRPC + Zod validation
- **Tests** : Vitest + Playwright E2E

### Sécurité
- **Context Isolation** : Isolation complète entre processus
- **Sandbox Mode** : Sécurité renforcée pour le renderer
- **CSP Strict** : Content Security Policy sans `unsafe-*`
- **IPC Sécurisé** : Validation et rate limiting des communications
- **Code Signing** : Signature numérique pour toutes les releases

## 🔧 Installation et Développement

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

## 🛡️ Sécurité et Conformité

WhytMod AI suit les meilleures pratiques de sécurité Electron 2025 :

- ✅ **Context Isolation** activé
- ✅ **Node Integration** désactivé
- ✅ **Sandbox Mode** activé
- ✅ **Web Security** maintenu
- ✅ **CSP Strict** sans directives dangereuses
- ✅ **Audit automatisé** avec Inspectron + ElectroNG

### Audit de sécurité
```bash
# Audit complet
npm run security:audit

# Scan des vulnérabilités
npm audit

# Test de pénétration
npm run security:pentest
```

## 📊 CI/CD et Déploiement

### GitHub Actions
- **🧪 Tests automatisés** : Tests unitaires et E2E sur chaque PR
- **🛡️ Audit sécurité** : Scan automatique des vulnérabilités
- **🏗️ Build multi-platform** : Packages Windows, macOS, Linux
- **🚀 Release automatique** : Déploiement automatisé avec signature

### Self-Hosted Runners
Configuration optimisée pour les runners locaux :
```bash
# Installation runner
npm run runner:setup

# Test connexion
npm run runner:test
```

## 🤝 Contribution

### Workflow de développement
1. **Fork** le repository
2. **Créer** une branche feature (`git checkout -b feature/amazing-feature`)
3. **Commit** les changements (`git commit -m 'Add amazing feature'`)
4. **Push** la branche (`git push origin feature/amazing-feature`)
5. **Ouvrir** une Pull Request

### Standards de code
- **TypeScript strict** obligatoire
- **Tests** pour toutes les nouvelles fonctionnalités
- **Documentation** mise à jour
- **Sécurité** validée par audit automatique

## 📁 Structure du Projet

```
whytmod-app/
├── 📁 src/
│   ├── 📁 main/           # Processus principal Electron
│   ├── 📁 renderer/       # Interface utilisateur React
│   ├── 📁 preload/        # Scripts preload sécurisés
│   ├── 📁 shared/         # Types et utilitaires partagés
│   └── 📁 services/       # Services backend
├── 📁 tests/              # Tests unitaires et E2E
├── 📁 docs/               # Documentation technique
├── 📁 .github/            # Workflows CI/CD
├── 📁 build/              # Configuration build
└── 📁 dist/               # Build final
```

## 🔗 Liens Utiles

- **🌐 Site Web** : [whytmod.ai](https://whytmod.ai)
- **📚 Documentation** : [docs.whytmod.ai](https://docs.whytmod.ai)
- **🐛 Issues** : [GitHub Issues](https://github.com/AdminWhytcard/whytmod-app/issues)
- **💬 Discord** : [Communauté WhytMod](https://discord.gg/whytmod)
- **📧 Contact** : support@whytmod.ai

## 📄 Licence

Distribué sous licence MIT. Voir `LICENSE` pour plus d'informations.

## 🙏 Remerciements

- **Electron Team** pour le framework
- **React Team** pour l'interface utilisateur
- **Nexus Mods** pour l'API
- **Communauté modding** pour l'inspiration

---

<div align="center">
  <strong>Développé avec ❤️ par l'équipe WhytMod</strong>
</div>
