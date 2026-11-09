[← Chapitre précédent](06-prompt-engineering-dev.md) · [Sommaire](Readme.md) · [Chapitre suivant →](08-conception-tests-doc.md)

# Chapitre 07 — Agents IA et leur laisse

> **Statut : squelette de structure.** Objectif visé **[Bloom 4]**. Contenu à rédiger (vague 2). Repère : 25 min de cours magistral + EX-07.

**Accroche (slide 1) :** « Si l'agent ne pouvait faire qu'une seule chose aujourd'hui, laquelle lui interdiriez-vous ? »

## 7.1 Les modes
Autocomplétion → chat → agent. Panorama tool-agnostic (opencode, Claude Code, Codex CLI, Copilot agent, OpenHands) ; démo sur l'outil de la classe.

## 7.2 Le mode plan
Plan → validation humaine → exécution. Le premier geste de conduite d'un agent.

## 7.3 Le modèle de menace (cœur du chapitre — 10 min)
L'agent lit ce qu'on ne relit pas :
- **injection indirecte** par README, commentaires de code, logs de test, descriptions d'outils **MCP** ;
- **tool poisoning** et **rug pull** d'un serveur MCP ;
- **exfiltration** (`.env`, `~/.ssh`, `GITHUB_TOKEN`) par commande détournée.

**La laisse :** permissions explicites, **deny list** (`git push`, `rm`, `curl`, `wget`, `ssh`, `.env`, `~/.ssh`), sandbox, réseau borné, budget. La configuration de laisse opencode est distribuée avec le dépôt du TP — **la laisse fait partie de l'environnement, donc de la thèse**.

## 7.4 Déclarer l'usage de l'IA
Délégation ≠ plagiat. Commits / PR / rapport ; règles du CFA ; confidentialité et CGU ; licences des fragments.

## Visuels
V7.1 (triptyque modes), V7.2 (séquence du mode plan), V7.3 (la laisse + surface d'attaque), V7.4 (commit co-authored + déclarer l'usage).

## Exercice rattaché
**EX-07 (red team, 10 min, individuel)** — une description d'outil MCP malveillante (vol de `.env` déguisé en « télémétrie ») : la repérer, la bloquer par la config de permissions, justifier en deux lignes. Corrigé en `-Peda`.

---
*À rédiger : développements, support du modèle de menace, énoncé + corrigé EX-07, config de laisse testée.*

---

[← Chapitre précédent](06-prompt-engineering-dev.md) · [Sommaire](Readme.md) · [Chapitre suivant →](08-conception-tests-doc.md)
