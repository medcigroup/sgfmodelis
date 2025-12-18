# 🤖 Guide d'utilisation de GitHub Copilot pour la Recette SIG

## 📋 Dépôt : medcigroup/sgfmodelis

Ce document contient les **prompts optimisés** pour utiliser GitHub Copilot afin de générer automatiquement vos rapports de recette.

---

## 🎯 Prompt Principal - Génération Automatique de Rapports

Copiez-collez ce prompt dans GitHub Copilot Chat à chaque session :

```
Je travaille sur la recette du projet SIG avec le dépôt medcigroup/sgfmodelis.

Je vais te donner mes retours de tests en langage simple et tu devras :
1. Structurer mes retours selon les templates d'issues du dépôt
2. Créer automatiquement les issues GitHub correspondantes
3. Utiliser les bons labels et la bonne catégorisation

Types de retours possibles :
- 🐛 Bugs/Anomalies
- ✅ Validations de fonctionnalités (conforme/non-conforme)
- 💡 Demandes d'amélioration
- 📋 Autres retours

Pour chaque retour, extrais et structure automatiquement :
- La description claire du problème/validation
- La sévérité/priorité
- Le module concerné
- Les étapes de reproduction (si bug)
- L'environnement de test
- Les recommandations

Dépôt cible : medcigroup/sgfmodelis

Es-tu prêt à recevoir mes retours de recette ?
```

---

## 📝 Templates de Prompts par Type de Retour

### 1️⃣ Pour un Bug/Anomalie

**Format simplifié :**
```
[BUG] Description courte du problème
- Module : [nom du module]
- Gravité : critique/majeur/mineur/cosmétique
- Navigateur/Environnement : [détails]
- Ce qui se passe : [comportement observé]
- Ce qui devrait se passer : [comportement attendu]
```

**Exemple concret :**
```
[BUG] La carte ne s'affiche pas au zoom
- Module : Cartographie
- Gravité : majeur
- Navigateur : Chrome v120
- Ce qui se passe : Écran blanc quand je clique sur zoom +
- Ce qui devrait se passer : La carte devrait zoomer normalement
```

---

### 2️⃣ Pour une Validation de Fonctionnalité

**Format simplifié :**
```
[VALIDATION] Nom de la fonctionnalité testée
- Statut : Conforme ✅ / Non-conforme ❌
- Critères testés : [liste]
- Points de non-conformité (si applicable) : [détails]
- Environnement : [version, navigateur, date]
```

**Exemple concret :**
```
[VALIDATION] Import de fichiers GeoJSON
- Statut : Non-conforme ❌
- Critères testés : 
  * Import fichier < 10MB : OK ✅
  * Affichage sur carte : KO ❌
  * Export après import : Non testé
- Points de non-conformité : Les couches importées ne s'affichent pas
- Environnement : v2.1.0, Firefox, 18/12/2025
```

---

### 3️⃣ Pour une Demande d'Amélioration

**Format simplifié :**
```
[AMÉLIORATION] Titre de l'amélioration
- Module : [nom]
- Priorité : haute/moyenne/basse
- Situation actuelle : [comment ça fonctionne maintenant]
- Amélioration souhaitée : [ce qui serait mieux]
- Bénéfice : [pourquoi c'est important]
```

**Exemple concret :**
```
[AMÉLIORATION] Ajout d'un bouton "Annuler" dans l'import
- Module : Import de données
- Priorité : moyenne
- Situation actuelle : Impossible d'annuler un import en cours
- Amélioration souhaitée : Bouton pour stopper l'import
- Bénéfice : Évite d'attendre la fin d'un gros fichier en erreur
```

---

### 4️⃣ Pour un Autre Retour

**Format simplifié :**
```
[RETOUR] Sujet du retour
- Type : observation/question/documentation/suggestion
- Importance : haute/moyenne/basse
- Description : [détails]
- Suggestion éventuelle : [recommandation]
```

**Exemple concret :**
```
[RETOUR] Documentation manquante sur les formats supportés
- Type : documentation
- Importance : moyenne
- Description : Pas d'info sur quels formats de fichiers sont acceptés
- Suggestion : Ajouter une page d'aide avec la liste des formats
```

---

## 🚀 Prompts pour Traitement par Lot

### Créer plusieurs issues d'un coup

```
Je vais te donner plusieurs retours de recette en une fois. 
Pour chacun, crée une issue séparée dans medcigroup/sgfmodelis.

Retours :

1. [BUG] La recherche par adresse ne fonctionne pas
   Module: Recherche, Gravité: majeur, Chrome v120
   Erreur "Aucun résultat" même avec des adresses valides

2. [VALIDATION] Export PDF - Non-conforme
   Le PDF généré ne contient pas la légende de la carte
   Version 2.1.0, testé le 18/12/2025

3. [AMÉLIORATION] Ajouter un bouton de réinitialisation de la carte
   Priorité moyenne, pour revenir rapidement à la vue initiale

Crée les 3 issues maintenant.
```

---

## 📊 Prompt pour Rapport de Session de Recette

À la fin d'une session de tests :

```
Session de recette terminée pour medcigroup/sgfmodelis.

Résumé de ma session :
- Date : [date]
- Modules testés : [liste]
- Nombre de bugs trouvés : [X]
- Nombre de validations : [X]
- Nombre d'améliorations proposées : [X]

Détails de mes retours :
[Listez vos retours ici]

Actions à faire :
1. Crée toutes les issues correspondantes
2. Génère-moi un résumé markdown de la session que je pourrai partager
```

---

## 🎨 Prompt pour Personnalisation

Si vous voulez adapter les templates :

```
Pour le dépôt medcigroup/sgfmodelis, j'aimerais :
- Ajouter un nouveau type de retour : [nom]
- Modifier le template [bug/validation/amélioration/autre] pour inclure : [champs]
- Créer un nouveau label : [nom] pour [usage]

Peux-tu m'aider à mettre ça en place ?
```

---

## 💡 Conseils d'Utilisation

### ✅ Bonnes Pratiques
- **Soyez naturel** : Pas besoin d'utiliser exactement les formats, Copilot comprend le langage naturel
- **Donnez le contexte** : Module, version, navigateur si pertinent
- **Un retour à la fois** ou groupez-les clairement
- **Mentionnez toujours** : `medcigroup/sgfmodelis` au début de votre session

### ❌ À Éviter
- Ne mélangez pas plusieurs types de retours dans une même description
- N'oubliez pas de préciser le module concerné
- Ne soyez pas trop vague (donnez des détails)

---

## 🔄 Workflow Recommandé

### Option 1 : Temps Réel
```
Pendant vos tests → Notez vos observations → Envoyez à Copilot → Issue créée immédiatement
```

### Option 2 : Fin de Journée
```
Tests de la journée → Liste de tous vos retours → Envoyez tout à Copilot → Toutes les issues créées d'un coup
```

### Option 3 : Hebdomadaire
```
Semaine de tests → Compilation des retours → Session avec Copilot → Rapport complet + issues
```

---

## 📞 Prompt de Démarrage Rapide

**Copiez ceci au début de chaque session :**

```
@copilot Bonjour ! Je commence une session de recette pour medcigroup/sgfmodelis.

Je vais te donner mes retours de tests et tu créeras automatiquement les issues GitHub structurées.

Premier retour : [votre retour ici]
```

---

## 🆘 Prompt d'Aide

Si vous êtes bloqué :

```
@copilot J'ai un retour de recette pour medcigroup/sgfmodelis mais je ne sais pas comment le catégoriser.

Voici ce que j'ai observé : [description]

Peux-tu m'aider à structurer ça correctement ?
```

---

## 📌 Rappel Important

**Le dépôt de recette** : `medcigroup/sgfmodelis`  
**Templates disponibles** : Bug, Validation, Amélioration, Autre  
**Vous pouvez** : Parler naturellement, Copilot s'occupe de la structure !

---

**Créé le** : 2025-12-18  
**Dernière mise à jour** : 2025-12-18  
**Responsable recette** : @medcigroup