# TP-01 — Le comptoir de prêt (énoncé)

> **Module d'extension, hors du temps de cours.** Remis par le formateur *si le temps le permet* en fin de journée 2 ; sinon il reste ouvert sur Moodle en prolongement libre. **Jamais pénalisant** : s'il est réalisé et rendu, il compte comme **bonus de +0 à +2** sur la note du QCM. Rien dans les deux journées ne dépend de lui.

## Ce que c'est, en une phrase

Un **projet intégrateur** au sens strict : tout le cours, un seul contexte, de bout en bout, un livrable. Vous jouez le rôle de celle ou celui qui **manage un junior d'une énergie infinie et d'une mémoire de poisson rouge** — sauf qu'ici le junior, c'est l'IA, et que tout ce que le cours a posé (la spec, les portes, l'établi, la boucle, la laisse) devient vos outils de travail.

Ce n'est **pas** un exercice de plus. Un exercice travaille *une* notion. Ici, vous assemblez le tout sur un dépôt réel, et **la matière évaluée, c'est votre processus autant que votre code** : les traces que vous laissez sont le critère.

## Le contexte

Un **service de prêt municipal** — vélos et matériel (casques, antivols, remorques) — tenu par un comptoir. On vous livre un dépôt **nu** : un service **Node / TypeScript + SQLite** qui démarre à peine, **aucune porte de qualité, aucune spec**, un secret oublié là, et une **config de laisse d'agent** déjà fournie.

**Les données sont non nominatives par construction** : les emprunteurs sont des identifiants anonymes (`A-42`, `B-07`…). C'est la règle RGPD du chapitre 09 appliquée au sujet lui-même — et votre rappel permanent : **dans un prompt d'offre gratuite, jamais de donnée personnelle ni d'entreprise.**

Le responsable du comptoir vous a parlé. Voici, mot pour mot, ce qu'il a dit. **C'est volontairement flou** — c'est le point de départ, pas un défaut de l'énoncé.

## Le cahier des charges (la demande du client, telle quelle)

> **f1 — Les retards.** « Quand quelqu'un rend un vélo en retard, il doit payer une pénalité. Mais le week-end, ça ne compte pas. Et on ne veut pas que ça explose. »
>
> **f2 — Le matériel avec caution.** « Le matériel, c'est plus cher qu'un vélo. Quand on prête du matériel, on prend une caution de 30 €. Et si c'est rendu cassé, on en garde une partie. »
>
> **f3 — Les remises.** « Ajoute les remises, fais-le bien, et fais gaffe aux arrondis. » (Le comptoir veut **20 % de remise** pour ses adhérents de longue durée.)

Vous reconnaissez f1 : c'est **exactement** la phrase du chapitre 02, où vous aviez fixé le contrat ensemble. Vous reconnaissez f3 : c'est la demande vague du chapitre 06, celle qui fait planter l'arrondi.

**Votre premier travail n'est pas de coder — c'est de transformer ces trois phrases en spec sans ambiguïté.** Le cours l'a dit : l'IA ne lève jamais la main pour demander ce que vous vouliez dire ; elle choisit une interprétation en silence et code dessus. Chaque flou ci-dessous est une décision **que vous prenez et que vous écrivez**, pas une question que l'IA vous posera :

- **f1** — retard par rapport à quelle date ? le week-end de *quel* segment ? « que ça explose », c'est à partir de combien ? *(Vous avez déjà tranché au ch. 02 : 1,50 € par jour ouvré, les deux bornes exclues, plafond 15 € par prêt. Gardez-le — c'est votre contrat de référence.)*
- **f2** — « rendu cassé », ça se décide comment ? « une partie », selon quelle règle ? la caution est-elle rendue intégralement si tout est en état ?
- **f3** — « fais-le bien », ça veut dire quoi de vérifiable ? « gaffe aux arrondis » : arrondi classique, bancaire, à la centime ? Le prix de départ est en euros ou en centimes ?

> La leçon du chapitre 06 tient en une ligne : **le prompt est le détecteur de la spec qui manque.** Si vous n'arrivez pas à écrire une phrase que la CI peut vérifier, c'est que vous ne savez pas encore ce que vous voulez.

## Le dépôt nu (ce que vous recevez)

Vous clonez le dépôt de départ fourni par le formateur. À l'ouverture, il ressemble à ça :

```text
comptoir/
├─ package.json          # nu : pas de script "test", pas de lint, pas de couverture
├─ src/
│  ├─ penalite.ts        # squelette — la fonction f1, à faire vivre
│  ├─ remise.ts          # le stub bogué du ch. 06 (Math.floor sur des flottants)
│  └─ ...                # le service, la couche SQLite minimale
├─ db/
│  └─ (schema.sql absent — c'est vous qui le générez, étape E5)
├─ .opencode.jsonc       # la laisse d'agent du ch. 07 (permissions, deny list)
└─ .env                  # un secret planqué — une porte doit le choper
```

Il n'y a **ni `features/`, ni tests, ni lint, ni CI** : c'est voulu. Vous allez équiper, spec-ifier, puis conduire. Les binômes qui ont fait EX-A/EX-B en salle partent de **leur** dépôt déjà équipé ; les autres repartent du dépôt nu et reprennent E2/E3 chez eux.

## Le ruban E0 → E6

Vous avancez sur ce ruban. Quatre étapes (E2, E3, E4, E5) ont été **vécues en direct** pendant les deux jours (les exercices EX-A à EX-D) : vous les reprenez ou les complétez. Trois (E0, E1, E6) sont **propres au module**.

| Étape | Ce que vous produisez | Statut |
|---|---|---|
| **E0** | Un **MCD** (Mermaid `erDiagram`) et une **maquette** générés par l'IA, **comparés à votre conception manuelle** ; vous listez les incohérences que l'IA a laissées passer. | module |
| **E1** | La **spec Gherkin complète** : 3 features (f1, f2, f3), au moins un `Scenario Outline` chiffré, au moins un scénario négatif, et le **cas limite week-end × semaine** de f1. | module (amorcée par le TD-02) |
| **E2** | **Équiper le dépôt** : Vitest + `@cucumber/cucumber`, ESLint + Prettier, `tsc --noEmit` strict, gitleaks, CI. | fait en direct (EX-A) |
| **E3** | Un **`AGENTS.md`** validé en conditions réelles : session IA fraîche, zéro connaissance du projet, tâche réelle, réussite sans aide humaine. | fait en direct (EX-B) |
| **E4** | **La boucle CI** : réparer un bug injecté et trancher une spec ambiguë, en boucle jusqu'au vert — ou jusqu'à votre borne. | fait en direct (EX-C) |
| **E5** | Générer `schema.sql` **depuis votre MCD corrigé**, puis implémenter **f1 en mode plan** (l'agent propose, vous validez, vous ne touchez pas au clavier). | fait en direct sur le MCD de référence (EX-D) |
| **E6** | **Le livrable** : implémenter **f2 et f3** par boucle jusqu'au vert CI, générer la documentation **puis la vérifier ligne à ligne**, et rédiger le **rapport d'usage**. | module — **rendu à J+15** |

Quelques repères concrets, pour que la boucle tourne :

```bash
npm ci                 # installer exactement les versions épinglées
npx vitest run         # les tests unitaires (remise, pénalité…)
npx cucumber-js        # la spec Gherkin exécutable
npx tsc --noEmit       # les types, en strict
npx gitleaks detect    # la porte qui débusque le secret du .env
```

**La règle d'or du chapitre 05 s'applique intégralement : ne jamais affaiblir un test pour passer au vert.** Si un test gêne, c'est soit le code qui est faux, soit la spec qui est fausse — jamais le test qu'il faut rogné.

## Ce qu'il faut rendre (et pourquoi ce sont les traces qui comptent)

Le livrable n'est pas « un dépôt qui compile ». C'est **la preuve que vous avez mené l'IA**, pas subi. À J+15, vous rendez :

1. **Le dépôt**, avec un **historique de commits lisible** (pas un commit unique « final » — on veut voir la progression).
2. **La spec Gherkin** (`features/`), couvrant les 3 fonctionnalités et le cas limite.
3. **Les logs CI de la boucle** : au moins une réparation automatique prouvée (le log qui montre rouge → vert).
4. **Les transcripts de session d'agent** (au moins E5 en mode plan, et E6).
5. **La documentation générée, puis vérifiée** : la doc, et la trace de votre relecture (ce que vous avez corrigé dedans).
6. **Le rapport d'usage**, une page (modèle ci-dessous).

> **Un livrable sans traces n'est pas noté bonus — il est juste un exercice.** C'est délibéré : le cours enseigne que la valeur n'est pas dans le code tapé par l'IA mais dans le cadre que vous avez construit autour. Le TP évalue ce cadre.

### Modèle de rapport d'usage (1 page)

```markdown
# Rapport d'usage — TP-01 — <prénom nom>

## Ce que l'IA a réellement apporté
- (2-3 puces, concrètes : tel bout de code, tel MCD, tel gain de temps chiffré)

## Ce que j'ai repris, et pourquoi
- (au moins 2 reprises : l'erreur de l'IA, comment vous l'avez détectée — la porte, le capteur —, ce que vous avez fait)

## La boucle
- Combien d'itérations pour le vert ? Où ai-je failli céder (affaiblir un test) ?

## La laisse
- Qu'ai-je interdit à l'agent ? Une fois, a-t-il essayé de sortir du cadre ?

## Ce que je referais autrement
- (une phrase honnête)
```

## Auto-évaluation — à cocher avant de rendre

- [ ] Ma spec Gherkin couvre les 3 fonctionnalités, avec le cas limite week-end × semaine.
- [ ] Mes portes rougissent sur le bug témoin (la requête de frais qui compte les week-ends).
- [ ] Ma boucle s'auto-répare au moins une fois, et je le prouve par les logs CI.
- [ ] Aucun test n'a été affaibli pour passer au vert.
- [ ] Ma documentation générée a été vérifiée ligne à ligne.
- [ ] Mon rapport d'usage dit ce que l'IA a réellement apporté — et ce que j'ai repris.

## Comment c'est noté (bonus, jamais pénalisant)

Grille /100, convertie en **bonus de +0 à +2** sur la note du QCM :

| Critère | Points |
|---|---|
| Spec Gherkin (couverture, cas limite, scénarios négatifs) | /30 |
| Portes effectives (le bug témoin doit **rougir** la CI) | /20 |
| Conduite de boucle (logs, garde-fous, tests non affaiblis) | /30 |
| Rapport d'usage et vérification de la doc | /20 |

Un bonus ne descend jamais sous 0 : ne pas rendre le TP ne coûte rien. Le rendre bien peut rapporter jusqu'à +2.

## Comment rendre

Dépôt + rapport, **rendu à J+15** sur le canal indiqué par le formateur (Moodle / dépôt privé). Le détail de la grille et le corrigé (f2-f3, MCD de référence, dépôt « avec pièges ») vivent côté formateur.

---

*Bon courage. Le but n'est pas de faire faire le travail à l'IA — c'est de montrer que vous savez lui tenir la laisse.*
