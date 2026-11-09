[← Chapitre précédent](04-contexte-projet.md) · [Sommaire](Readme.md) · [Chapitre suivant →](06-prompt-engineering-dev.md)

# Chapitre 05 — La CI qui autoboucle l'IA

> **Statut : squelette de structure.** Objectif visé **[Bloom 5]**. Contenu à rédiger (vague 2). Repère : 40 min de cours magistral + démo guidée 20 min + EX-C.

**Accroche (slide 1) :** « Combien de boucles de correction avant qu'il eût été moins cher de coder soi-même ? »

## 5.1 Le basculement
La CI devient **le capteur de la boucle de correction automatique**.

## 5.2 Un pipeline « IA-ready » (GitHub Actions)
Jobs séparés, sorties structurées, artefacts d'échec. **Le log d'échec est le prompt suivant.**

## 5.3 La boucle
Agent pousse → CI rouge → log réinjecté → correctif → re-run → vert **ou borne atteinte**.

## 5.4 Les garde-fous
Protection de `main`, revue humaine, max itérations, budget tokens, et la règle d'or : **interdiction d'affaiblir les tests pour passer au vert** (montrer le trick et comment la revue le détecte).

## 5.5 Durcissement CI
Permissions au strict nécessaire ; secrets dans un environnement protégé, jamais dans un déclencheur `pull_request_target` exposé au code non fiable ; timeouts et cache. *(SBOM, `npm audit signatures`, SHA-pinning : cités en « Prolongement » — ce cours n'est pas un cours DevSecOps.)*

## Démo guidée (la plus risquée — fallback détaillé dans la doc d'aide)
Bug injecté (conversion € → cents) → CI rouge → l'agent lit le log, corrige, pousse → vert. Trace projetée : log, prompt auto-généré, diff, compteur d'itérations. En cas de dérive : coupe en direct et rejeu sur la trace de référence capturée à la répétition.

## Visuels
V5.1 (LA boucle — poster du cours), V5.2 (log = prompt suivant), V5.3 (garde-fous), V5.4 (la triche : test commenté), V5.5 (compteur d'itérations réel).

## Exercice rattaché
**EX-C (25 min, binômes)** — « casser la boucle pour de vrai » : bug vicieux réparé seul, puis exigence réellement ambiguë → vert sans répondre au besoin. Débrief : *la boucle ne vaut que ce que vaut la spec.*

---
*À rédiger : développements, script + trace de référence de la démo, énoncés EX-C.*

---

[← Chapitre précédent](04-contexte-projet.md) · [Sommaire](Readme.md) · [Chapitre suivant →](06-prompt-engineering-dev.md)
