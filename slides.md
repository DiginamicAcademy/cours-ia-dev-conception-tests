---
marp: true
theme: default
style: |
  section {background-color: #121114}
  h1,h2,h3 {color: #8393f0}
  p,ul,li,td,th {color: #ccc}
  section table {font-size: 0.85em}
  section table td {background-color: #121114}
  section table th {background-color: #272133; font-weight: bolder}
  pre {background-color: #17151a; color: #ccc}
  blockquote {border: 2px green solid; border-left-width: 15px; padding: 0.5em 15px;font-style: italic }
paginate: true
header: "Exploiter l'IA pour le développement, la conception et les tests"
footer: "![height:20px](https://raw.githubusercontent.com/DiginamicInternal/PublicAssets/refs/heads/main/Logo-diginamic-color-blk.png)"
---

# Exploiter l'IA pour le développement, la conception et les tests

### Un junior d'une énergie infinie et d'une mémoire de poisson rouge — on le manage

<!-- Diapositive d'ouverture. Squelette de structure : les 164 slides de production
     viendront en vague 1. Chaque section ci-dessous = un chapitre, ouverte par sa
     question accroche (sondage), fermée par « on résume ». -->

---

## 🎯 Le fil du cours

> Environnement > prompt. Le pipeline « conception → spec → portes → boucle → revue → cadre » se complète chapitre après chapitre.

---

## 🗺️ Sommaire

**J1** — 01 Modèle mental · 02 Gherkin · 03 Portes de qualité · 04 Contexte
**J2** — 05 Boucle CI · 06 Prompt engineering · 07 Agents et leur laisse · 08 Conception/tests/doc · 09 Réglementation
**Extension** — TP-01 Le comptoir de prêt

---

## 00 · Ouverture

« Qui a déjà copié du code qu'il ne comprenait pas ? » — aujourd'hui, c'est la même chose, mais industrialisé.

<!-- Débrief du QCM de positionnement, brainstorm « quelles tâches déléguer à l'IA ? ». -->

---

# 01 — Modèle mental

**Accroche :** « L'IA affirme que cette fonction existe. En combien de secondes pouvez-vous le vérifier — et comment ? »

<!-- 17 slides de production : panorama, fenêtre de contexte, déterminisme, hallucinations, slopsquatting. V0.1, V1.1-V1.4. EX-01. -->

---

# 02 — Spec-first : Gherkin

**Accroche :** « Quelle est la différence entre cette phrase d'un client et un bug ? »

<!-- 18 slides. Mode TD complet. V2.1-V2.4. -->

---

# 03 — Les portes de qualité

**Accroche :** « Votre CI est verte. Votre code est-il juste pour autant ? »

<!-- 16 slides. Panneau de capteurs (V3.1). Démo avant/après. EX-A. -->

---

# 04 — Ingénierie du contexte

**Accroche :** « Combien coûte un fichier ouvert "au cas où" dans la fenêtre de contexte ? »

<!-- 14 slides. AGENTS.md. Démo avec/sans. EX-B. -->

---

# 05 — La CI qui autoboucle l'IA

**Accroche :** « Combien de boucles de correction avant qu'il eût été moins cher de coder soi-même ? »

<!-- 20 slides. LA boucle (V5.1). Démo guidée (fallback dans la doc formateur). EX-C. -->

---

# 06 — Prompt engineering pour le dev

**Accroche :** « Entre "ajoute les remises, fais-le bien" et la fonctionnalité qui marche : combien d'itérations ? »

<!-- 15 slides. Anti-patterns. EX-06 + challenge binômes. -->

---

# 07 — Agents IA et leur laisse

**Accroche :** « Si l'agent ne pouvait faire qu'une seule chose, laquelle lui interdiriez-vous ? »

<!-- 13 slides. Mode plan. Modèle de menace (injection, MCP). EX-07 red team. -->

---

# 08 — Conception, tests & documentation

**Accroche :** « L'IA écrit le code et les tests. Qui vérifie, au final ? »

<!-- 17 slides. 3 options avec compromis. Stitch. Test miroir (V8.1). EX-08. -->

---

# 09 — Réglementation IA

**Accroche :** « Quelle loi s'applique au code que vous avez généré ce matin ? »

<!-- 14 slides. Pyramide AI Act (V9.1), frise post-Omnibus (V9.2), RGPD du prompt (V9.4). -->

---

# TP-01 — Le comptoir de prêt

**Accroche :** « Feriez-vous confiance à un code que vous n'avez pas écrit, mais dont vous pouvez prouver chaque ligne ? »

<!-- 10 slides. Ruban E0→E6. Remis si le temps le permet. -->

---

# Clôture

**Accroche :** « Qu'est-ce que l'IA a *réellement* changé dans votre code aujourd'hui — et comment le prouvez-vous ? »

<!-- 4 slides. QCM sommatif, puis remise du TP si le temps le permet. -->
