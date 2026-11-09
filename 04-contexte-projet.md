# Chapitre 04 — Ingénierie du contexte : rendre le projet lisible par l'IA

> **Statut : squelette de structure.** Objectif visé **[Bloom 4]**. Contenu à rédiger (vague 2). Repère : 30 min de cours magistral + EX-B.

**Accroche (slide 1) :** « Combien coûte un fichier ouvert "au cas où" dans la fenêtre de contexte ? Plus que votre prompt. Vraiment ? »

## 4.1 Les fichiers d'instructions
`AGENTS.md` (standard émergent), `CLAUDE.md`, `.cursorrules`, `.github/copilot-instructions.md`.

## 4.2 Anatomie d'un bon AGENTS.md
Commandes (`npm run …`), conventions, arborescence commentée, interdits, définition de « fini ». Ce qu'on n'y met pas.

## 4.3 Progressive disclosure
Le fichier pointe vers `docs/` et les ADR plutôt qu'il ne tout contient.

## 4.4 Optimiser à l'exécution
Injecter / résumer / déléguer. Le coût du contexte périmé (fenêtre saturée).

## 4.5 Les exclusions
Secrets, données personnelles, `.gitignore` (dont `node_modules/`, `.env`, base SQLite locale).

## Démo formateur (fallback dans la doc d'aide)
Même tâche, session fraîche, **sans puis avec** AGENTS.md. ~6 min.

## Visuels
V4.1 (entonnoir du contexte), V4.2 (AGENTS.md annoté), V4.3 (contexte périmé), V4.4 (sans / avec, captures).

## Exercice rattaché
**EX-B (30 min, binômes)** — rédiger l'`AGENTS.md` du dépôt, puis le valider en session IA fraîche (zéro connaissance du projet). Critère : l'agent réussit sans aide humaine. Débrief 5 min.

---
*À rédiger : développements, démo avec/sans captée, consigne + critères EX-B.*
