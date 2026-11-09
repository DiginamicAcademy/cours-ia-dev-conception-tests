[Sommaire](Readme.md) · [Chapitre suivant →](02-spec-gherkin.md)

# Chapitre 01 — L'IA dans la chaîne de développement : modèle mental

> **Statut : squelette de structure.** Objectif visé **[Bloom 2]**. Contenu à rédiger (vague 2 de production). Repère : 30 min de cours magistral + EX-01.

**Accroche (slide 1, sondage) :** « L'IA affirme que cette fonction existe. En combien de secondes pouvez-vous le vérifier — et comment ? »

## 1.1 Panorama des IA pour développeurs
ChatGPT / Claude / Gemini en chat ; Copilot ; Cursor ; agents CLI (opencode, Claude Code, Codex CLI, OpenHands). Les modes sont détaillés au chapitre 07 ; les outils disponibles sans licence sont listés dans le `Readme.md`.

## 1.2 Ce qu'un LLM fait bien, ce qu'il fait mal
Génération de code courant, traduction entre langages, explication — vs mémoire limitée, absence de connaissance du projet, « remplissage » plausible.

## 1.3 La fenêtre de contexte, expliquée à un développeur
L'établi : tout ce qui n'entre pas sur l'établi n'existe pas pour l'agent. Conséquence directe sur la façon de conduire l'IA.

## 1.4 Déterminisme contre probabilité
Deux runs, deux diffs. Pourquoi la CI est l'arbitre, pas l'impression.

## 1.5 Les hallucinations côté développeur
API inventées ; dépendances fantômes et **slopsquatting** (nom npm voisin d'un vrai) ; correctifs plausibles mais faux.

## 1.6 Le fil du cours, posé ici
**Environnement > prompt.** Le pipeline « conception → spec → portes → boucle → revue → cadre » s'ouvre, se complétera chapitre après chapitre.

## Démos formateur (fallback dans la doc d'aide)
- *L'API inventée* : `_.flattenDeepSafe()` — `tsc` + CI l'attrapent en 10 s.
- *Deux runs, deux diffs* sur la même consigne.
- *Slopsquatting* : montrer le faux package sans l'installer.

## Visuels
V0.1 (affiche « le junior sans mémoire »), V1.1 (établi / fenêtre de contexte), V1.2 (deux runs deux diffs), V1.3 (slopsquatting), V1.4 (tableau fait bien / fait mal).

## Exercice rattaché
**EX-01 « Repérez les mensonges » (15 min)** — 5 productions IA à auditer (API inventée, dépendance fantôme, correctif faux mais plausible, test qui n'assert rien, une correcte). Classer et justifier en une phrase. Correction repliable.

---
*À rédiger : développements, captures réelles des démos, énoncé + correction d'EX-01.*

---

[Sommaire](Readme.md) · [Chapitre suivant →](02-spec-gherkin.md)
