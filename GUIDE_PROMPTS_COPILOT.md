# Guide des Prompts Copilot pour la Recette

Ce guide contient des exemples de prompts optimisés pour utiliser GitHub Copilot dans le cadre de la recette du projet sgfmodelis.

---

## 🔍 Prompt pour Rapport de Session de Recette

Pour générer un rapport de session de recette :

```
@copilot Génère-moi un rapport de session de recette pour medcigroup/sgfmodelis.

Module testé : [nom du module]
Date : [date]
Testeur : [nom]

Scénarios testés :
1. [scénario 1]
2. [scénario 2]

Résultats :
- [résultat 1]
- [résultat 2]

Bugs identifiés :
1. [bug 1]
2. [bug 2]

Format : Markdown avec sections claires
```

---

## 📊 Prompt pour Présentation de Réunion Journalière

Pour générer automatiquement une présentation de vos tests du jour :

```
@copilot Génère-moi une présentation pour ma réunion journalière sur medcigroup/sgfmodelis.

Date : [date du jour]
Modules testés aujourd'hui : [liste des modules]

Résumé de mes tests :

BUGS TROUVÉS :
1. [description courte bug 1]
2. [description courte bug 2]

VALIDATIONS :
1. [fonctionnalité] - Conforme ✅
2. [fonctionnalité] - Non-conforme ❌ - raison

AMÉLIORATIONS PROPOSÉES :
1. [amélioration 1]

BLOQUANTS :
- [Si des points bloquants]

PROCHAINES ÉTAPES :
- [Ce qui reste à tester]

Format souhaité : [Markdown/PowerPoint/PDF]
```

---

## 📈 Prompt pour Rapport Hebdomadaire

Pour un résumé de toute la semaine :

```
@copilot Génère-moi un rapport hebdomadaire de recette pour medcigroup/sgfmodelis.

Semaine du : [date début] au [date fin]

Statistiques :
- Nombre total de tests effectués : [X]
- Bugs critiques : [X]
- Bugs majeurs : [X]  
- Bugs mineurs : [X]
- Fonctionnalités validées : [X]
- Fonctionnalités non-conformes : [X]
- Améliorations proposées : [X]

Points marquants :
[Listez les éléments importants de la semaine]

Bloquants en cours :
[Liste des bloquants non résolus]

Format : Présentation avec graphiques et tableaux de synthèse
```

---

## 🎤 Prompt pour Présentation Exécutive (Management)

Pour une présentation destinée au management :

```
@copilot Crée une présentation exécutive de l'avancement de la recette pour medcigroup/sgfmodelis.

Période : [dates]

Avancement global : [X]%

Résumé exécutif :
- Qualité générale : [Bonne/Moyenne/Faible]
- Risques identifiés : [Liste]
- Points bloquants : [Liste]
- Recommandations : [Liste]

Métriques clés :
- Taux de conformité : [X]%
- Bugs critiques en cours : [X]
- Délai estimé pour correction : [X jours]

Format : Présentation concise avec KPI visuels
```

---

## 📋 Formats de Présentation Disponibles

### Format 1 : Markdown Simple
```
@copilot Génère un rapport markdown pour ma réunion daily sur medcigroup/sgfmodelis avec mes retours d'aujourd'hui : [vos retours]
```

### Format 2 : Tableau de Bord
```
@copilot Crée un tableau de bord visuel (markdown avec émojis et indicateurs) de mes tests du jour pour medcigroup/sgfmodelis : [vos retours]
```

### Format 3 : Slides (Markdown)
```
@copilot Génère des slides en markdown pour ma présentation daily sur medcigroup/sgfmodelis : [vos retours]
```

---
