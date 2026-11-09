<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="assets/Logo-diginamic-color-blk.png">
    <img src="assets/Logo-diginamic-color.svg" alt="Diginamic Formation" width="358">
  </picture>
</p>

# Exploiter l'IA pour le développement, la conception et les tests

> **Support en production.** Les neuf chapitres sont rédigés. Les durées ci-dessous sont des repères, pas des engagements à la minute.

**2 jours · distanciel avec formateur · outillage 100 % gratuit.** Cours hors référentiel RNCP, porté par la direction pour préparer les développeurs à la pratique assistée par IA — et conforme à l'obligation de « culture IA » de l'AI Act.

## L'idée qui tient tout le cours

> **Une IA qui code de mieux en mieux, mais qui ne se souvient de rien et ne connaît rien à votre projet. La vraie compétence, ce n'est pas le prompt magique : c'est de construire un environnement où elle travaille bien — spécifications explicites, capteurs de qualité, boucle automatique, garde-fous humains — dans un cadre légal qu'on connaît.**

La métaphore filée, reprise à chaque chapitre : **l'IA est un développeur junior d'une énergie infinie et d'une mémoire de poisson rouge.** On la manage avec les outils inventés pour les juniors : specs claires, tests, CI, revue, documentation lisible — et un contrat de responsabilité.

## Objectifs pédagogiques

À l'issue du cours, vous saurez : situer les capacités et limites d'un modèle génératif ; rédiger une spécification Gherkin comme contrat exécutable ; équiper un projet de capteurs de qualité ; ingénier le contexte d'un projet pour l'IA ; concevoir une CI qui auto-boucle l'IA avec des garde-fous ; construire et optimiser vos prompts de développement ; conduire l'IA sur toutes les étapes du métier en gardant la main ; évaluer de façon critique la production d'une IA (qualité des tests, sécurité, confidentialité, licences) ; situer le cadre AI Act / RGPD / licences appliqué à votre pratique.

## Prérequis

Git et GitHub ; un langage de programmation (les laboratoires sont en **JavaScript / TypeScript**) ; ligne de commande ; notions de tests unitaires et de SQL. Aucune licence payante n'est requise : la liste des outils gratuits est donnée à l'ouverture.

## Le parcours

Chapitre après chapitre, le pipeline « conception → spec → portes → boucle → revue → cadre » se complète ; il est entier au chapitre 05, puis encadré par la réglementation au chapitre 09.

> **Avant le jour 1 :** un [auto-questionnaire de positionnement](00-positionnement.md) (non noté, cinq minutes) sert à composer les binômes et à calibrer le rythme des deux journées.

### Journée 1 — Construire un environnement où l'IA travaille bien

| # | Chapitre | Repère | Ce qu'on y fait |
|---|---|---|---|
| [01](01-modele-mental.md) | Modèle mental | 30 min | capacités/limites du LLM, fenêtre de contexte, hallucinations, « environnement > prompt » |
| [02](02-spec-gherkin.md) | Spec-first : Gherkin | TD 50 + 35 min | la demande floue devient un contrat exécutable (mode TD complet) |
| [03](03-portes-de-qualite.md) | Les portes de qualité | 35 min | les capteurs qui parlent le langage de l'IA |
| [04](04-contexte-projet.md) | Ingénierie du contexte | 30 min | AGENTS.md et consorts : rendre le projet lisible |

### Journée 2 — La boucle : CI, agents, prompt, réglementation

| # | Chapitre | Repère | Ce qu'on y fait |
|---|---|---|---|
| [05](05-boucle-ci.md) | La CI qui autoboucle l'IA | 40 min | le log d'échec comme prompt suivant, les garde-fous |
| [06](06-prompt-engineering-dev.md) | Prompt engineering pour le dev | 30 min | structure d'une demande, anti-patterns, prompt vs spec |
| [07](07-agents-et-leur-laisse.md) | Agents IA et leur laisse | 25 min | modes, mode plan, modèle de menace (injection, MCP), déclarer l'usage |
| [08](08-conception-tests-doc.md) | Conception, tests & documentation | 35 min | l'IA propose, l'humain ou un capteur dispose ; le test miroir |
| [09](09-reglementation-ia.md) | Réglementation IA | 30 min | AI Act, RGPD, licences, responsabilité |
| [A](A-Glossaire-et-ressources.md) | Glossaire et ressources | — | un glossaire par cours |

## Le module d'extension — TP-01 « Le comptoir de prêt »

Un projet intégrateur **hors du temps de cours** : voir [tp/](tp/README.md). Il est remis par le formateur **si le temps le permet** ; sinon il reste disponible en prolongement libre, sans effet sur la note. Réalisé sur votre propre machine, de bout en bout, il mobilise tout le cours.

## Évaluation

- **QCM sommatif** (20 questions, sans IA, en fin de journée 2) : **c'est la note du cours**, pour tous.
- **TP-01** : extension **bonus** (+2 maximum, jamais pénalisante), si remis avec les preuves de processus (commits, logs CI, transcripts).
- **QCM formatifs** : une série « Vérifiez vos acquis » en fin de chaque chapitre, non notée, pour s'entraîner (réponses dépliables).

## Organisation de ce dépôt

Chapitres à la racine (assemblés en PDF par le workflow), positionnement dans `00-positionnement.md`, diapositives dans `slides.md`, visuels dans `assets/slides/`, module d'extension dans `tp/`. Les QCM formatifs sont intégrés en fin de chapitre (« Vérifiez vos acquis »). La conception, les corrigés et les évaluations notées (dont le QCM sommatif importable dans Moodle) vivent dans le dépôt privé [`cours-ia-dev-conception-tests-Peda`](https://github.com/DiginamicAcademy/cours-ia-dev-conception-tests-Peda).
