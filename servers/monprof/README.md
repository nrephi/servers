# MonProf MCP Server

**Connectez MonProf à Claude, ChatGPT et autres assistants IA via Model Context Protocol.**

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![MCP Version](https://img.shields.io/badge/MCP-1.0.0+-blue)](https://modelcontextprotocol.io/)

## 🎯 À propos

MonProf est une plateforme de **formation en ligne alimentée par l'IA**. Ce serveur MCP vous permet de :

- 📚 **Créer et gérer** vos formations directement depuis votre assistant IA
- 🤖 **Générer des cours** à partir de simples descriptions
- 🎙️ **Produire des voix off** automatiques en plusieurs langues
- 👥 **Planifier des sessions** et gérer les inscriptions
- 📊 **Consulter des rapports** détaillés sur vos formations

## 🚀 Démarrage rapide

### 1. Obtenir le serveur

L'URL du serveur est :
```
https://monprof.app/mcp
```

### 2. Configurer dans votre assistant IA

#### Claude (Desktop / Web)
```json
{
  "type": "http",
  "url": "https://monprof.app/mcp",
  "auth": "oauth2"
}
```

#### ChatGPT (OpenAI)
Utiliser la configuration Actions personnalisées avec OpenAPI schema

#### Gemini CLI
```json
{
  "monprof": {
    "httpUrl": "https://monprof.app/mcp",
    "oauth": {
      "enabled": true,
      "scopes": ["monprof:read", "monprof:write", "monprof:delete"]
    },
    "trust": false
  }
}
```

## 📋 Fonctionnalités disponibles

### Outils
- **list_courses** - Lister vos formations
- **create_course** - Créer une nouvelle formation
- **generate_voiceover** - Générer une voix off
- **schedule_session** - Planifier une session
- **get_report** - Récupérer un rapport d'analytics

### Ressources
- Accès en lecture/écriture à vos formations
- Gestion des sessions et inscriptions
- Récupération des rapports

### Prompts
- Templates pré-configurés pour création de cours
- Guides d'utilisation

## 🔐 Authentification

Le serveur utilise **OAuth 2.0** pour l'authentification. Lors de la première connexion, vous serez redirigé vers MonProf pour autoriser l'accès.

**Scopes disponibles :**
- `monprof:read` - Consulter vos données
- `monprof:write` - Modifier vos données
- `monprof:delete` - Supprimer des éléments

## 📖 Exemples d'utilisation

### Claude
```
Claude : "Crée un cours Python pour débutants dans MonProf"
→ L'assistant utilise l'outil create_course
```

### ChatGPT
```
ChatGPT : "Génère la voix off pour mon dernier cours"
→ L'assistant utilise l'action generate_voiceover
```

## 🐛 Support et contribution

- **Documentation** : https://monprof.app/fonctionnalites/mcp
- **Issues** : https://github.com/monprof/mcp-server/issues
- **Contact** : ntumbaphinees@gmail.com

## 📜 Licence

MIT License - voir LICENSE pour plus de détails.

---

**Fait avec ❤️ par MonProf**
