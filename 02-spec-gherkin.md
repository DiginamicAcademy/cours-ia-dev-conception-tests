[← Chapitre précédent](01-modele-mental.md) · [Sommaire](Readme.md) · [Chapitre suivant →](03-portes-de-qualite.md)

# Chapitre 02 — Spec-first : Gherkin comme interface avec l'IA

> **Statut : squelette de structure.** Objectif visé **[Bloom 3]**. Contenu à rédiger (vague 2). Ce chapitre est conduit en **mode TD complet** (découverte → correction → cours → application), sur le contexte du comptoir de prêt. Repère : TD 50 min + cours 35 min.

**Accroche (slide 1) :** « Quelle est la différence entre cette phrase d'un client et un bug ? »

## Séquence TD
1. **Découverte (20 min, binômes, sans le cours)** — la demande floue des retards de vélo : « la liste des étapes qu'un robot pourrait exécuter pour vérifier ce comportement ».
2. **Correction (10 min, collectif)** — fait émerger condition / action / vérification ; **nomme** Given/When/Then avant de les définir.
3. **Cours (35 min)** — ci-dessous.
4. **Application (20 min, individuel)** — scénarios de la f2, Outline chiffré + scénario négatif ; le cas limite (week-end × semaine de retard) est visé.

## 2.1 Syntaxe complète
`Feature`, `Scenario`, `Background`, `Scenario Outline` + `Examples`, tags.

## 2.2 De la feature à l'exécution : @cucumber/cucumber
`.feature` → step definitions TypeScript → implémentation. Le premier rouge est normal et voulu.

## 2.3 Le scénario-contrat
L'ambiguïté donnée à l'IA devient un bug. Écrire des scénarios où l'IA ne peut pas tricher : chiffres concrets, résultats explicites, cas négatifs.

## 2.4 La spec comme critère d'arrêt de la boucle
Aperçu du chapitre 05 : la spec dit quand on s'arrête de corriger.

## Visuels
V2.1 (première brique du pipeline), V2.2 (anatomie Given/When/Then), V2.3 (une phrase → deux lectures → deux codes), V2.4 (run cucumber rouge).

## Rattaché
L'amorce du TD sert aussi d'ébauche à l'étape **E1** du module d'extension TP-01.

---
*À rédiger : cours complet, énoncés TD découverte + application, corrections repliables.*

---

[← Chapitre précédent](01-modele-mental.md) · [Sommaire](Readme.md) · [Chapitre suivant →](03-portes-de-qualite.md)
