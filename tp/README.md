# TP-01 — Le comptoir de prêt (module d'extension)

> **Statut : squelette de structure.** Énoncé complet + corrigé à produire en vague 2. Le **corrigé, la grille détaillée et le dépôt nu « avec pièges » vivent dans le dépôt privé `-Peda`**, jamais ici.

## Qu'est-ce que c'est

Un **projet intégrateur** au sens strict : tout le cours, un contexte, de bout en bout, un livrable. **Hors du temps de cours** — sa réalisation n'empiète sur aucun chapitre. Il est **remis par le formateur si le temps le permet** (fin de journée 2) ; sinon il reste disponible en prolongement libre, **sans effet sur la note**. S'il est réalisé et rendu, il compte comme **bonus (+2 max, jamais pénalisant)**.

## Le contexte

Service de prêt municipal (vélos et matériel), **Node / TypeScript + SQLite**. Dépôt livré **nu** : squelette + couche SQLite minimale, aucune porte de qualité, aucune spec, un secret planqué, une **config de laisse d'agent** fournie. **Données non nominatives par construction** (emprunteurs = identifiants anonymes). Cahier des charges d'une page : 3 fonctionnalités, dont le cas limite piégeux (facturation des retards traversant week-end et seuil d'une semaine).

## Le ruban E0 → E6

| Étape | Quoi | Où |
|---|---|---|
| E0 | MCD (Mermaid) + maquette **Stitch (prioritaire) ou Excalidraw → HTML**, générés par l'IA, **comparés à la conception manuelle** | module |
| E1 | Spec Gherkin complète (3 features, Outline chiffré, scénarios négatifs) — amorcée par le TD-02 | module |
| E2 | Équipement (Vitest + Cucumber, lint, types, secrets, CI) | fait en direct en **EX-A** |
| E3 | AGENTS.md validé par session IA fraîche | fait en direct en **EX-B** |
| E4 | Boucle CI : bug injecté réparé + spec ambiguë | fait en direct en **EX-C** |
| E5 | `schema.sql` généré depuis le MCD, f1 en mode plan | **EX-D** (sur le MCD de référence) |
| E6 | **Livrable** : f2-f3 par boucle jusqu'au vert CI + documentation générée **puis vérifiée** + rapport d'usage 1 page | module, **rendu à J+15** |

## Ce qui est exigé pour le bonus

**Preuves de processus** (c'est la matière du cours, elle devient le critère) : historique de commits lisible, logs CI de la boucle, transcripts de session d'agent, revue croisée citée. Un livrable sans traces n'est pas noté bonus — il est juste un exercice.

## Auto-évaluation (à cocher avant de rendre)

- [ ] Ma spec Gherkin couvre les 3 fonctionnalités, avec le cas limite week-end × semaine.
- [ ] Mes portes rougissent sur le bug témoin (requête de frais qui compte les week-ends).
- [ ] Ma boucle s'auto-répare au moins une fois, et je le prouve par les logs CI.
- [ ] Aucun test n'a été affaibli pour passer au vert.
- [ ] Ma documentation générée a été vérifiée ligne à ligne.
- [ ] Mon rapport d'usage dit ce que l'IA a réellement apporté — et ce que j'ai repris.

## Grille (résumé — détail en `-Peda`)

Spec /30 · portes effectives /20 · conduite de boucle /30 · rapport & vérification de doc /20. Converti en **bonus +0 à +2** sur la note du QCM.

---
*À produire : énoncé complet, dépôt nu (avec et sans pièges), MCD de référence, corrigé E6, grille détaillée.*
