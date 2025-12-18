---
title: "[BUG] La carte ne s'affiche pas lors du clic sur le bouton zoom"
labels: ["bug", "à-traiter"]
date: 2025-12-18
---

## 📋 Description du bug/anomalie

La carte ne s'affiche pas lorsque l'utilisateur clique sur le bouton de zoom. Cette anomalie empêche la visualisation de la carte après avoir tenté d'utiliser la fonctionnalité de zoom.

## 🔴 Sévérité

- [x] Majeur (impact significatif)
- [ ] Critique (bloquant)
- [ ] Mineur (impact faible)
- [ ] Cosmétique (esthétique)

## 📍 Module/Fonctionnalité concerné(e)

Module cartographie - Fonctionnalité de zoom

## 🔄 Étapes pour reproduire

1. Ouvrir l'application de cartographie
2. Cliquer sur le bouton de zoom
3. Observer que la carte ne s'affiche pas

## ✅ Résultat attendu

La carte devrait s'afficher normalement avec le niveau de zoom approprié lorsque l'utilisateur clique sur le bouton zoom. La carte doit rester visible et interactive.

## ❌ Résultat observé

La carte ne s'affiche pas du tout après avoir cliqué sur le bouton zoom. L'espace cartographique reste vide ou disparaît.

## 🖼️ Captures d'écran

<!-- Des captures d'écran seront nécessaires pour documenter ce problème -->

## 🌐 Environnement

- **Version de l'application:** À préciser
- **Navigateur:** À préciser
- **Système d'exploitation:** À préciser
- **Date du test:** 2025-12-18

## 📝 Informations complémentaires

Ce bug affecte directement l'utilisation principale de l'application cartographique. Il est recommandé de vérifier :
- Les gestionnaires d'événements du bouton zoom
- La visibilité de la couche cartographique
- Les éventuelles erreurs JavaScript dans la console
- L'état du conteneur de la carte après le clic

## 🔍 Investigation suggérée

- Vérifier que le bouton zoom déclenche bien l'événement attendu
- S'assurer que la carte est correctement initialisée avant le clic
- Contrôler que le conteneur de la carte n'est pas masqué (display: none, visibility: hidden)
- Vérifier les dimensions du conteneur de la carte
- Examiner les logs de la console pour détecter d'éventuelles erreurs
