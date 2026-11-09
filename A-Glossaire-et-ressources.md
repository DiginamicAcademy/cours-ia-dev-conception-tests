[← Chapitre précédent](09-reglementation-ia.md) · [Sommaire](Readme.md)

# Annexe A — Glossaire et ressources

> Chaque sigle et chaque mot du cours est défini à sa première occurrence dans les chapitres, puis retrouvé ici. Les définitions sont volontairement courtes : c'est le chapitre indiqué qui les travaille.

## Sigles et acronymes

| Sigle | Signification | Chap. |
|---|---|---|
| ADR | *Architecture Decision Record* : une décision d'architecture et son pourquoi, tracés | 04 |
| AGENTS.md | Fichier d'instructions que l'agent relit à chaque session (le nom change selon l'outil) | 04 |
| AI Act | Règlement (UE) 2024/1689 sur l'intelligence artificielle | 09 |
| ANSSI | Agence nationale de la sécurité des systèmes d'information | 09 |
| API | Interface de programmation d'un service (ce par quoi on l'appelle) | 08 |
| CI | Intégration continue : le pipeline qui installe, construit et teste à chaque modification | 05 |
| CLI | Interface en ligne de commande | 01 |
| CNIL | Commission nationale de l'informatique et des libertés | 09 |
| CODEOWNERS | Fichier GitHub qui rend la revue d'un dossier obligatoire | 05 |
| CSV | Format tabulaire séparé par des virgules | 09 |
| Gherkin | Langage de spécification lisible ET exécutable (`Given` / `When` / `Then`) | 02 |
| GHSA | *GitHub Security Advisory* : avis public sur une faille et sa version corrigée | 03 |
| GPAI | *General Purpose AI* : modèle d'IA à usage général (AI Act) | 09 |
| HTML | Langage des pages web | 08 |
| IA | Intelligence artificielle | 09 |
| LLM | *Large Language Model* : modèle de langage à grande échelle | 01 |
| MCP | *Model Context Protocol* : standard pour brancher des outils externes à un agent | 07 |
| MCD | Modèle Conceptuel de Données | 08 |
| npm | Gestionnaire de paquets de Node.js, et le registre en ligne qui les héberge | 01 |
| ORM | *Object-Relational Mapping* : accès aux données sans écrire de SQL | 08 |
| PR | *Pull Request* : demande de fusion soumise à relecture | 05 |
| RGPD | Règlement général sur la protection des données | 04 |
| RNCP | Répertoire national des certifications professionnelles | 09 |
| SAST | *Static Application Security Testing* : analyse statique de votre propre code | 03 |
| SBOM | *Software Bill of Materials* : inventaire signé des dépendances d'un projet | 05 |
| SGBD | Système de gestion de base de données | 08 |
| SLA | Engagement de service et de disponibilité | 08 |
| SPDX | Standard d'identification des licences (`SPDX-License-Identifier`) | 09 |
| SQL | Langage d'interrogation et de mise à jour des bases de données | 08 |
| TDD | *Test-Driven Development* : écrire le test avant le code | 01 |
| TypeScript | JavaScript typé, vérifié par compilation | 01 |
| UE | Union européenne | 09 |
| WCAG | Référentiel d'accessibilité du web | 08 |

## Vocabulaire du cours

Les mots que ce cours emploie dans un sens précis, souvent d'un chapitre à l'autre.

| Mot | Sens dans le cours | Chap. |
|---|---|---|
| Capteur (exécutable) | Vérification automatique qui sait dire « non » : un test, un type, un lint | 01 |
| Porte de qualité | Un capteur + un message d'échec lisible, qui bloque ou alerte | 03 |
| Boucle (locale, puis CI) | Les mêmes portes rejouées toutes seules, en local avant le commit, puis dans le pipeline | 03 |
| Établi / fenêtre de contexte | Ce que la machine « voit » réellement pendant une session : un budget, pas une poubelle | 01 |
| Harnais | Les tests écrits d'abord : à la fois critère d'arrêt pour l'agent et barrière anti-régression | 01 |
| Hallucination | Erreur plausible, énoncée avec assurance — le danger n'est pas l'erreur visible mais l'erreur crédible | 01 |
| Dépendance fantôme | Paquet au nom crédible mais inexistant, ou squatté par un tiers | 01 |
| Slopsquatting | Usurpation d'un nom de paquet très proche pour tromper l'installateur | 01 |
| Test miroir | Test qui recopie l'implémentation dans son assertion : il ne peut plus contredire le code | 05 |
| Test fécond | Test dont l'oracle est le contrat, pas le code : il échouerait si le code était cassé | 08 |
| Oracle (de test) | Ce qui définit « juste » indépendamment de ce que rend le code | 08 |
| Cœur pur | Fonction sans base de données, ni horloge, ni asynchrone — donc déterministe | 03 |
| Laisse (d'un agent) | L'ensemble de ses permissions : `allow` / `ask` / `deny`, périmètre de fichiers, budget | 07 |
| Mode plan | L'agent écrit ce qu'il va faire, vous lisez et validez, et seulement alors il exécute | 07 |
| Injection indirecte | Consigne cachée dans un fichier que l'agent est censé lire (README, commentaire d'issue…) | 07 |
| Tool poisoning | Description d'outil piégée : pour l'agent, une description n'est pas de la doc, c'est une consigne | 07 |
| Spec (spec-first) | Comportement écrit, vérifiable par la machine, posé avant le code | 02 |
| Step definition | Le code qui accroche une phrase Gherkin à une fonction : sans elle, la `.feature` reste un document | 02 |
| Cas négatif | « Ça ne doit *pas* se passer » : ce qui ferme l'espace d'interprétation | 02 |
| Critère d'arrêt | Ce qui dit « fini » : le vert de tous les scénarios, pas une impression | 02 |
| Contrat | Les décisions client qui fixent les chiffres (bornes, plafonds, taux) | 02 |
| Jour ouvré | Jour travaillé (lundi–vendredi) ; dans ce cours, les deux bornes sont exclues | 02 |
| Centimes entiers | Convention maison : l'argent est en centimes entiers, jamais en flottant | 02 |
| Definition of done | La définition de « fini », écrite dans le dépôt pour survivre à chaque session | 04 |
| Source unique | Un chiffre n'a qu'un seul fichier où il vit ; ailleurs on le pointe, on ne le recopie pas | 04 |
| Passation | Fiche courte pour repartir sur une session propre quand l'établi est encombré | 04 |
| Cinq zones | Structurer une demande : rôle, contexte, tâche, contraintes, format | 06 |
| Few-shot | Donner un exemple à imiter plutôt qu'une explication à suivre | 06 |
| Anti-pattern | Tic de demande gratuit à éviter mais coûteux à entretenir (rôle-placebo, devine-l'archi, le négatif…) | 06 |
| Budget tokens / max itérations | Les deux bornes d'une boucle de correction : quand on s'arrête, même sans vert | 05 |
| Artifacter (artefact) | Emballer les rapports pour pouvoir les récupérer quand un job échoue | 05 |
| Mutation testing | Saboter le code pour tester la suite : un mutant survécu = un test qui ne protège rien | 08 |
| Second modèle | Un autre modèle en relecteur — jamais en arbitre | 08 |
| Règle de préséance | Qui gagne quand deux sources divergent (la spec, pas le code généré) | 08 |
| Culture IA | Obligation (AI Act, art. 4) de former les personnes qui utilisent l'outil | 09 |
| Fournisseur / déployeur | Mettre un système d'IA sur le marché sous son nom / l'utiliser sans le commercialiser | 09 |
| Minimisation | N'envoyer que ce qui sert la tâche : la fenêtre de contexte est une frontière juridique | 09 |
| Diligence | Ce qu'un professionnel raisonnable aurait fait — prouvé par des traces (commits, CI, revue) | 09 |

## Ressources

**Textes et références**
- AI Act — règlement (UE) 2024/1689, et le *Digital Omnibus* (UE 2026/1744) qui en a reporté certaines échéances : texte sur EUR-Lex.
- CNIL — intelligence artificielle et données personnelles ; ANSSI — recommandations sur l'usage de l'IA en entreprise.

**Documentation des outils du cours**
- Agents et CLI : `opencode` (open source, multi-fournisseurs).
- Spécification et tests : `@cucumber/cucumber`, Vitest, TypeScript, ESLint.
- Portes de sécurité : `gitleaks`, Semgrep, `npm audit`.
- Qualité des tests : StrykerJS (mutation testing).
- Maquettes : Google Stitch (étudié ici comme objet critique, pas comme outil recommandé).

**Le fil pratique**
- Le TP intégrateur : dossier `tp/` — « Le comptoir de prêt », de bout en bout.
- Les QCM d'entraînement (import Moodle) : dossier `qcm/`. Le QCM noté final, sans IA, est remis par le formateur.

> Ce cours ne prépare aucun titre RNCP : il s'ancrit sur l'obligation de « culture IA » de l'AI Act (art. 4).

---

[← Chapitre précédent](09-reglementation-ia.md) · [Sommaire](Readme.md)
