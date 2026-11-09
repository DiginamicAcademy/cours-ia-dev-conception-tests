# QCM — conventions

Ce dossier porte les **QCM formatifs** du cours, un par chapitre, au format **Moodle XML** (import direct dans une banque de questions). Les mêmes questions sont aussi lisibles dans chaque chapitre, sous « Vérifiez vos acquis » : le chapitre sert à l'autoformation, le XML ici sert à l'import Moodle (salle, suivi).

## Règles (convention de production)

- **Un fichier XML Moodle par QCM formatif.** Les questions apparaissent aussi dans le chapitre, réponses repliées sous `<details>` ; ici on garde le XML brut pour l'import.
- Compter les questions **en excluant les balises `type="category"`** (elles ne sont pas des questions).
- **Sans** cases « je savais ».
- **Distracteurs étoffés** en contre-vraisons plausibles ; la bonne réponse n'est **ni la plus longue ni la plus détaillée** (sinon le commentaire « Pourquoi » ne colle plus).
- Dans le XML, la bonne réponse est posée en tête et `<shuffleanswers>` est activé : Moodle mélange à l'import. Dans le chapitre, l'ordre des options est varié à la main — sinon « réponse : A » six fois sur six serait donneur.

## Contenu

| Fichier | Rôle |
|---|---|
| `positionnement.xml` | 8 questions, envoyé **avant J1**, non noté, diagnostique (sert à composer les binômes) |
| `formatif-ch01.xml` … `formatif-ch09.xml` | 6 questions par chapitre, non notés, à faire avec l'IA |

> Le **QCM sommatif noté** (20 questions, blueprint 2 items × 9 objectifs, **sans IA**) ne vit **pas ici** : c'est l'évaluation notée, elle est dans le dépôt privé `-Peda/evaluations/qcm/`.
