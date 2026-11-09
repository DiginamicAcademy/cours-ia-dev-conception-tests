[← Chapitre précédent](07-agents-et-leur-laisse.md) · [Sommaire](Readme.md) · [Chapitre suivant →](09-reglementation-ia.md)

# Chapitre 08 — L'IA pour la conception, les tests et la documentation

> **Statut : squelette de structure.** Objectif visé **[Bloom 5]**. Contenu à rédiger (vague 2). Repère : 35 min de cours magistral + EX-08. Un principe : **l'IA propose, l'humain ou un capteur exécutable dispose.**

**Accroche (slide 1) :** « L'IA écrit le code et les tests. Qui vérifie, au final ? »

## 8.1 Conception (12 min)
- **3 options avec compromis**, pas LA solution ; ADR générés puis argumentés ; revue par IA et ses angles morts.
- Illustration par **l'exemple E0 du formateur** (produit réel de répétition) : MCD généré vs manuel, incohérences cerclées.
- **Maquette : démo Stitch** (path prioritaire) — cinq écrans en une minute, puis ce que le HTML rate (états, accessibilité, validation, persistance) ; fallback Excalidraw manuel → HTML généré par l'IA de la classe.
- La génération **SQL** : le SGBD est un capteur impitoyable. ORM (Prisma) : nouveau terrain d'hallucination + codegen qu'on ne relit plus (cité en ouverture).

## 8.2 Tests (12 min)
Génération depuis le code (**test miroir**) vs depuis la spec (fécond) ; données et cas limites ; mutation testing (StrykerJS) en « Prolongement ».

## 8.3 Documentation (6 min)
README, OpenAPI, guide utilisateur générés — checklist de vérification humaine (les options documentées qui n'existent pas).

## 8.4 Dernier rempart (5 min)
Croiser les rôles : humain, second modèle, spec exécutable.

## Visuels
V8.1 (le test miroir — poster), V8.2 (3 options avec compromis), V8.3 (mutation), V8.4 (triangle du dernier rempart), V8.5 (MCD IA vs manuel + schema.sql), V8.6 (Stitch + Excalidraw → HTML), V8.7 (README généré + checklist).

## Exercice rattaché
**EX-08 « Le test miroir » (15 min)** — tests générés depuis le code → passent ; mutation (mutant ciblé, rapport pré-calculé) → aucune alerte ; régénérés depuis le Gherkin → attrapée. Le contraste est la leçon. Correction repliable.

---
*À rédiger : développements, E0 de répétition réel + captures, énoncé + correction EX-08.*

---

[← Chapitre précédent](07-agents-et-leur-laisse.md) · [Sommaire](Readme.md) · [Chapitre suivant →](09-reglementation-ia.md)
