# QCM — conventions

Ce dossier porte les **QCM formatifs** du cours, un par chapitre, au format **Moodle XML** (import direct dans une banque de questions).

## Règles (convention de production)

- **Un fichier XML Moodle par QCM**, jamais de QCM dans le corps des chapitres.
- Compter les questions **en excluant les balises `type="category"`** (elles ne sont pas des questions).
- **Sans** cases « je savais ».
- **Distracteurs étoffés** en contre-vraisons plausibles ; la bonne réponse n'est **ni la plus longue ni la plus détaillée** (sinon le commentaire « Pourquoi » ne colle plus).
- Réponses dans un bloc repliable côté support ; ici, le XML brut pour l'import.

## Contenu prévu

| Fichier | Rôle |
|---|---|
| `positionnement.xml` | 8 questions, envoyé **avant J1**, non noté, diagnostique (sert à composer les binômes) |
| `formatif-ch01.xml` … `formatif-ch09.xml` | 5-6 questions par chapitre, non notés, avec IA |

> Le **QCM sommatif noté** (20 questions, blueprint 2 items × 9 objectifs, **sans IA**) ne vit **pas ici** : c'est l'évaluation notée, elle est dans le dépôt privé `-Peda/evaluations/qcm/`.

---
*À produire en vague 2.*
