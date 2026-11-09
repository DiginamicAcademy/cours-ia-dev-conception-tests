[← Chapitre précédent](02-spec-gherkin.md) · [Sommaire](Readme.md) · [Chapitre suivant →](04-contexte-projet.md)

# Chapitre 03 — Les portes de qualité : les capteurs de l'IA

> **Statut : squelette de structure.** Objectif visé **[Bloom 4]**. Contenu à rédiger (vague 2). Repère : 35 min de cours magistral + EX-03 imbriqué.

**Accroche (slide 1) :** « Votre CI est verte. Votre code est-il juste pour autant ? »

## 3.1 Le principe
Une porte de qualité = **un capteur qui parle le langage de l'IA**. Chaque échec lisible est une instruction gratuite pour la correction.

## 3.2 La panoplie JavaScript / TypeScript
Vitest (+ couverture V8) ; `@cucumber/cucumber` (scénarios sur SQLite `:memory:` propre par scénario) ; ESLint + Prettier ; `tsc --noEmit` strict ; gitleaks ; npm audit + Semgrep ; husky + lint-staged = la boucle locale.

## 3.3 Le bon réflexe d'architecture
Cœur métier **pur** (le calcul de frais est une fonction) et persistance **derrière un repository** : c'est ce qui garde les scénarios rapides et déterministes, et rend la base de données interchangeable.

## 3.4 Écrire des messages d'échec exploitables
`expect(total, "20 attendus").toBe(19)` vs `exit code 1` muet. L'assert qui nourrit la boucle.

## 3.5 Le piège du « tout au vert »
Couverture ≠ assertions. Promesse tenue au chapitre 08 (le test miroir).

## Démo formateur (fallback dans la doc d'aide)
*Avant / après* — même tâche IA sur dépôt nu (chaos, « vert » faux) vs équipé (vert vrai). ~8 min.

## Visuels
V3.1 (panneau de capteurs — visuel-clé, réutilisé ch. 05), V3.2 (avant/après), V3.3 (assert muet vs nourricier), V3.4 (« exécuté ≠ asserté »).

## Exercice rattaché
**EX-03 (10 min, imbriqué)** — réécrire un échec de test muet pour qu'il nourrisse la boucle.

---
*À rédiger : développements, démo avant/après captée, énoncé + correction d'EX-03.*

---

[← Chapitre précédent](02-spec-gherkin.md) · [Sommaire](Readme.md) · [Chapitre suivant →](04-contexte-projet.md)
