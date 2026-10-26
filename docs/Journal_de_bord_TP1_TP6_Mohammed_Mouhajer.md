# Journal de bord individuel — TP1 à TP6

**Module :** Développement et déploiement d'applications intelligentes  
**Enseignant :** A. Larhlimi  
**Établissement :** EMSI Casablanca — filière IADC  
**Étudiant :** Mohammed Mouhajer  
**Compte GitHub :** `MedByteSystems`  
**Dépôt personnel :** https://github.com/MedByteSystems/IA-DEV-Journal-de-bord-du-bin-me-TP1-TP6  
**Date de rédaction :** 26 octobre 2026

> **Portée du présent journal.** Ce document est individuel : il décrit uniquement le suivi de Mohammed Mouhajer. La présence d'un contrôle dans le journal ne constitue pas une preuve d'exécution. Les résultats marqués « à confirmer » doivent être complétés à l'aide d'une vraie commande ou capture avant remise finale.

## 1. Présentation du travail

L'objectif du fil rouge est de faire évoluer une application d'analyse de sentiment : cadrage métier, préparation de l'environnement, apprentissage supervisé, exposition d'un modèle par API FastAPI, assurance qualité, interface Streamlit et packaging Python. Le dépôt sert à conserver le code, la documentation, les tests et les preuves de validation.

## 2. État constaté dans le dépôt personnel

**État GitHub constaté au 26/10/2026 :** dépôt public non vide, contenant le kit du TP1. Fichiers et dossiers visibles : `README.md`, `TP1-ENONCE.md`, `MARCHE-A-SUIVRE.md`, `requirements.txt`, `pytest.ini`, `scripts/check_setup.py`, `tests/test_cadrage.py`, `tests/test_environment.py`, `tests/test_git_history.py`, `docs/cadrage/`, `docs/journal-tp1-tp6.md`, `docs/captures/tp1-t6-pytest.png`, ainsi que `app/`, `data/`, `models/`, `ui/` et `notebooks/`.

La présence d'une capture de terminal prouve l'existence d'une pièce justificative, mais son résultat exact doit être retranscrit après lecture de l'image ou réexécution des tests. Les fichiers du kit ne prouvent pas à eux seuls que tous les contrôles T0–T7 ont été validés.

## 3. TP1 — Cadrer l'application et préparer l'environnement

### Objectifs

- Définir les besoins et les approches de résolution de trois situations métier.
- Préparer Python, Git, les dépendances et la structure de projet.
- Vérifier les tests automatiques et la traçabilité Git.
- Documenter les preuves et rendre le dépôt reproductible.

### Fiches de cadrage étudiées

**Cas 1 — Pharmacie :** analyser la demande métier, préciser les entrées et sorties attendues, relever les contraintes et justifier une méthode adaptée.  
**Cas 2 — Règlement :** identifier l'objectif, la nature du contenu, les contraintes de traitement et les critères permettant de choisir une approche.  
**Cas 3 — Avis négatifs :** cadrer l'identification des retours défavorables, préciser la nature des données textuelles et les indicateurs d'évaluation pertinents.

Les trois fiches sont présentes dans `docs/cadrage/` du dépôt. Leur présence est vérifiable ; la validation de tous les critères dépend de l'exécution effective de `pytest tests/test_cadrage.py -q`.

### T0 — Structure du kit

**Commande de contrôle :**

```powershell
Get-ChildItem -Force
```

**Attendu :** Présence des sept dossiers app, data, docs, models, scripts, tests et ui.  
**Constat vérifiable :** Structure présente dans le dépôt.  
**Résultat terminal :** À reporter depuis une exécution réelle.  
**Conformité :** [ ] À confirmer.  
**Commentaire personnel :** Ce contrôle permet de documenter l’organisation des dossiers. Je dois reporter la sortie réellement obtenue et une capture correspondante avant de cocher « conforme ».

### T1 — Environnement Python

**Commande de contrôle :**

```powershell
python scripts/check_setup.py
python -m pytest -q
```

**Attendu :** Diagnostic et état initial des tests ; la trame prévoit 3 failed, 31 passed, 4 skipped avant cadrage.  
**Constat vérifiable :** Résultat local non établi par inspection du dépôt.  
**Résultat terminal :** À reporter depuis une exécution réelle.  
**Conformité :** [ ] À confirmer.  
**Commentaire personnel :** Ce contrôle permet de documenter la reproductibilité de l’environnement. Je dois reporter la sortie réellement obtenue et une capture correspondante avant de cocher « conforme ».

### T2 — Fiches de cadrage

**Commande de contrôle :**

```powershell
python -m pytest tests/test_cadrage.py -q
python -m pytest -q
```

**Attendu :** La trame prévoit 12 passed au cadrage, puis 34 passed, 4 skipped.  
**Constat vérifiable :** Fiches présentes dans le dépôt.  
**Résultat terminal :** À reporter depuis une exécution réelle.  
**Conformité :** [ ] À confirmer.  
**Commentaire personnel :** Ce contrôle permet de documenter la cohérence du cadrage. Je dois reporter la sortie réellement obtenue et une capture correspondante avant de cocher « conforme ».

### T3 — GitHub et premier push

**Commande de contrôle :**

```powershell
git status
git remote -v
python -m pytest -q
```

**Attendu :** Vérifier le dépôt distant, les exclusions Git et les tests après le premier push.  
**Constat vérifiable :** Dépôt public accessible et fichiers poussés.  
**Résultat terminal :** À reporter depuis une exécution réelle.  
**Conformité :** [ ] À confirmer.  
**Commentaire personnel :** Ce contrôle permet de documenter la publication des travaux. Je dois reporter la sortie réellement obtenue et une capture correspondante avant de cocher « conforme ».

### T4 — Vérification sur un second poste

**Commande de contrôle :**

```powershell
python scripts/check_setup.py
```

**Attendu :** 0 erreur au diagnostic attendu.  
**Constat vérifiable :** Résultat local non établi par inspection du dépôt.  
**Résultat terminal :** À reporter depuis une exécution réelle.  
**Conformité :** [ ] À confirmer.  
**Commentaire personnel :** Ce contrôle permet de documenter la mise en route sur un autre poste. Je dois reporter la sortie réellement obtenue et une capture correspondante avant de cocher « conforme ».

### T5 — Historique Git

**Commande de contrôle :**

```powershell
git shortlog -sn --all
python -m pytest tests/test_git_history.py -q
```

**Attendu :** Vérifier l’identité effective des auteurs ; 3 passed attendu au test Git.  
**Constat vérifiable :** Résultat local non établi par inspection du dépôt.  
**Résultat terminal :** À reporter depuis une exécution réelle.  
**Conformité :** [ ] À confirmer.  
**Commentaire personnel :** Ce contrôle permet de documenter la traçabilité des contributions. Je dois reporter la sortie réellement obtenue et une capture correspondante avant de cocher « conforme ».

### T6 — Vérification finale

**Commande de contrôle :**

```powershell
python scripts/check_setup.py
python -m pytest -q
```

**Attendu :** 0 erreur, 0 avertissement, 38 passed et CI verte attendus.  
**Constat vérifiable :** Une capture nommée tp1-t6-pytest.png existe dans docs/captures.  
**Résultat terminal :** À reporter depuis une exécution réelle.  
**Conformité :** [ ] À confirmer.  
**Commentaire personnel :** Ce contrôle permet de documenter le bilan automatisé du TP1. Je dois reporter la sortie réellement obtenue et une capture correspondante avant de cocher « conforme ».

### T7 — Clone frais

**Commande de contrôle :**

```powershell
git clone https://github.com/MedByteSystems/IA-DEV-Journal-de-bord-du-bin-me-TP1-TP6 verification-tp1
cd verification-tp1
python -m pytest -q
```

**Attendu :** Vérifier l’installation reproductible et les 38 tests sur un clone indépendant.  
**Constat vérifiable :** Résultat local non établi par inspection du dépôt.  
**Résultat terminal :** À reporter depuis une exécution réelle.  
**Conformité :** [ ] À confirmer.  
**Commentaire personnel :** Ce contrôle permet de documenter la reproductibilité hors du poste initial. Je dois reporter la sortie réellement obtenue et une capture correspondante avant de cocher « conforme ».

### Difficultés et corrections du TP1

Le cadrage doit respecter la structure attendue par les tests : sections présentes, réponses non vides, une seule approche retenue et justification fondée sur les critères. En cas d'échec, corriger les fiches puis relancer le test ciblé avant la suite complète. Le diagnostic Git et les commandes doivent être rejoués après modification.

**Élément à ajouter avant remise :** synthèse de la dernière exécution de `pytest -q`, copie de la capture pertinente, identités Git réellement enregistrées et URL de la CI si celle-ci existe.

## 4. TP2 — Entraîner, évaluer et sauvegarder le modèle

**Statut au 26/10/2026 :** non démontré par le dépôt personnel consulté. Cette section reste un suivi de travaux à réaliser ou à publier, et non un procès-verbal de validation.

### C1 : installation du kit TP2

**Travail attendu :** réaliser le contrôle selon l'énoncé du TP2, conserver la sortie de commande ou le résultat dans l'application et la preuve correspondante.  
**Résultat obtenu :** Non renseigné — aucune preuve vérifiée dans ce dépôt.  
**Conformité :** [ ] À contrôler.  
**Capture :** À ajouter dans `docs/captures/` si le contrôle demande une preuve visuelle.  
**Commentaire :** La validation sera consignée après exécution réelle, avec les éventuelles erreurs rencontrées et les corrections apportées.

### C2 : analyse des 290 avis de démonstration

**Travail attendu :** réaliser le contrôle selon l'énoncé du TP2, conserver la sortie de commande ou le résultat dans l'application et la preuve correspondante.  
**Résultat obtenu :** Non renseigné — aucune preuve vérifiée dans ce dépôt.  
**Conformité :** [ ] À contrôler.  
**Capture :** À ajouter dans `docs/captures/` si le contrôle demande une preuve visuelle.  
**Commentaire :** La validation sera consignée après exécution réelle, avec les éventuelles erreurs rencontrées et les corrections apportées.

### C3 : entraînement TF-IDF + régression logistique

**Travail attendu :** réaliser le contrôle selon l'énoncé du TP2, conserver la sortie de commande ou le résultat dans l'application et la preuve correspondante.  
**Résultat obtenu :** Non renseigné — aucune preuve vérifiée dans ce dépôt.  
**Conformité :** [ ] À contrôler.  
**Capture :** À ajouter dans `docs/captures/` si le contrôle demande une preuve visuelle.  
**Commentaire :** La validation sera consignée après exécution réelle, avec les éventuelles erreurs rencontrées et les corrections apportées.

### C4 : matrice de confusion et analyse des erreurs

**Travail attendu :** réaliser le contrôle selon l'énoncé du TP2, conserver la sortie de commande ou le résultat dans l'application et la preuve correspondante.  
**Résultat obtenu :** Non renseigné — aucune preuve vérifiée dans ce dépôt.  
**Conformité :** [ ] À contrôler.  
**Capture :** À ajouter dans `docs/captures/` si le contrôle demande une preuve visuelle.  
**Commentaire :** La validation sera consignée après exécution réelle, avec les éventuelles erreurs rencontrées et les corrections apportées.

### C5 : jeu de données de référence, tests et push

**Travail attendu :** réaliser le contrôle selon l'énoncé du TP2, conserver la sortie de commande ou le résultat dans l'application et la preuve correspondante.  
**Résultat obtenu :** Non renseigné — aucune preuve vérifiée dans ce dépôt.  
**Conformité :** [ ] À contrôler.  
**Capture :** À ajouter dans `docs/captures/` si le contrôle demande une preuve visuelle.  
**Commentaire :** La validation sera consignée après exécution réelle, avec les éventuelles erreurs rencontrées et les corrections apportées.

## 5. TP3 — Exposer le modèle par une API

**Statut au 26/10/2026 :** non démontré par le dépôt personnel consulté. Cette section reste un suivi de travaux à réaliser ou à publier, et non un procès-verbal de validation.

### T14 : installation du kit TP3

**Travail attendu :** réaliser le contrôle selon l'énoncé du TP3, conserver la sortie de commande ou le résultat dans l'application et la preuve correspondante.  
**Résultat obtenu :** Non renseigné — aucune preuve vérifiée dans ce dépôt.  
**Conformité :** [ ] À contrôler.  
**Capture :** À ajouter dans `docs/captures/` si le contrôle demande une preuve visuelle.  
**Commentaire :** La validation sera consignée après exécution réelle, avec les éventuelles erreurs rencontrées et les corrections apportées.

### T15 : GET /health

**Travail attendu :** réaliser le contrôle selon l'énoncé du TP3, conserver la sortie de commande ou le résultat dans l'application et la preuve correspondante.  
**Résultat obtenu :** Non renseigné — aucune preuve vérifiée dans ce dépôt.  
**Conformité :** [ ] À contrôler.  
**Capture :** À ajouter dans `docs/captures/` si le contrôle demande une preuve visuelle.  
**Commentaire :** La validation sera consignée après exécution réelle, avec les éventuelles erreurs rencontrées et les corrections apportées.

### T16 : prédiction d’un avis positif

**Travail attendu :** réaliser le contrôle selon l'énoncé du TP3, conserver la sortie de commande ou le résultat dans l'application et la preuve correspondante.  
**Résultat obtenu :** Non renseigné — aucune preuve vérifiée dans ce dépôt.  
**Conformité :** [ ] À contrôler.  
**Capture :** À ajouter dans `docs/captures/` si le contrôle demande une preuve visuelle.  
**Commentaire :** La validation sera consignée après exécution réelle, avec les éventuelles erreurs rencontrées et les corrections apportées.

### T17 : prédiction d’un avis négatif

**Travail attendu :** réaliser le contrôle selon l'énoncé du TP3, conserver la sortie de commande ou le résultat dans l'application et la preuve correspondante.  
**Résultat obtenu :** Non renseigné — aucune preuve vérifiée dans ce dépôt.  
**Conformité :** [ ] À contrôler.  
**Capture :** À ajouter dans `docs/captures/` si le contrôle demande une preuve visuelle.  
**Commentaire :** La validation sera consignée après exécution réelle, avec les éventuelles erreurs rencontrées et les corrections apportées.

### T18 : requêtes invalides et codes 422

**Travail attendu :** réaliser le contrôle selon l'énoncé du TP3, conserver la sortie de commande ou le résultat dans l'application et la preuve correspondante.  
**Résultat obtenu :** Non renseigné — aucune preuve vérifiée dans ce dépôt.  
**Conformité :** [ ] À contrôler.  
**Capture :** À ajouter dans `docs/captures/` si le contrôle demande une preuve visuelle.  
**Commentaire :** La validation sera consignée après exécution réelle, avec les éventuelles erreurs rencontrées et les corrections apportées.

### T19 : intégration continue

**Travail attendu :** réaliser le contrôle selon l'énoncé du TP3, conserver la sortie de commande ou le résultat dans l'application et la preuve correspondante.  
**Résultat obtenu :** Non renseigné — aucune preuve vérifiée dans ce dépôt.  
**Conformité :** [ ] À contrôler.  
**Capture :** À ajouter dans `docs/captures/` si le contrôle demande une preuve visuelle.  
**Commentaire :** La validation sera consignée après exécution réelle, avec les éventuelles erreurs rencontrées et les corrections apportées.

### T20 : démarrage sans modèle

**Travail attendu :** réaliser le contrôle selon l'énoncé du TP3, conserver la sortie de commande ou le résultat dans l'application et la preuve correspondante.  
**Résultat obtenu :** Non renseigné — aucune preuve vérifiée dans ce dépôt.  
**Conformité :** [ ] À contrôler.  
**Capture :** À ajouter dans `docs/captures/` si le contrôle demande une preuve visuelle.  
**Commentaire :** La validation sera consignée après exécution réelle, avec les éventuelles erreurs rencontrées et les corrections apportées.

## 6. TP4 — Tests approfondis et qualité

**Statut au 26/10/2026 :** non démontré par le dépôt personnel consulté. Cette section reste un suivi de travaux à réaliser ou à publier, et non un procès-verbal de validation.

### T21 : contrôles initiaux

**Travail attendu :** réaliser le contrôle selon l'énoncé du TP4, conserver la sortie de commande ou le résultat dans l'application et la preuve correspondante.  
**Résultat obtenu :** Non renseigné — aucune preuve vérifiée dans ce dépôt.  
**Conformité :** [ ] À contrôler.  
**Capture :** À ajouter dans `docs/captures/` si le contrôle demande une preuve visuelle.  
**Commentaire :** La validation sera consignée après exécution réelle, avec les éventuelles erreurs rencontrées et les corrections apportées.

### T22 : validation du contrat d’entrée

**Travail attendu :** réaliser le contrôle selon l'énoncé du TP4, conserver la sortie de commande ou le résultat dans l'application et la preuve correspondante.  
**Résultat obtenu :** Non renseigné — aucune preuve vérifiée dans ce dépôt.  
**Conformité :** [ ] À contrôler.  
**Capture :** À ajouter dans `docs/captures/` si le contrôle demande une preuve visuelle.  
**Commentaire :** La validation sera consignée après exécution réelle, avec les éventuelles erreurs rencontrées et les corrections apportées.

### T23 : tests de propriétés

**Travail attendu :** réaliser le contrôle selon l'énoncé du TP4, conserver la sortie de commande ou le résultat dans l'application et la preuve correspondante.  
**Résultat obtenu :** Non renseigné — aucune preuve vérifiée dans ce dépôt.  
**Conformité :** [ ] À contrôler.  
**Capture :** À ajouter dans `docs/captures/` si le contrôle demande une preuve visuelle.  
**Commentaire :** La validation sera consignée après exécution réelle, avec les éventuelles erreurs rencontrées et les corrections apportées.

### T24 : seuil d’abstention

**Travail attendu :** réaliser le contrôle selon l'énoncé du TP4, conserver la sortie de commande ou le résultat dans l'application et la preuve correspondante.  
**Résultat obtenu :** Non renseigné — aucune preuve vérifiée dans ce dépôt.  
**Conformité :** [ ] À contrôler.  
**Capture :** À ajouter dans `docs/captures/` si le contrôle demande une preuve visuelle.  
**Commentaire :** La validation sera consignée après exécution réelle, avec les éventuelles erreurs rencontrées et les corrections apportées.

### T25 : jeu d’or

**Travail attendu :** réaliser le contrôle selon l'énoncé du TP4, conserver la sortie de commande ou le résultat dans l'application et la preuve correspondante.  
**Résultat obtenu :** Non renseigné — aucune preuve vérifiée dans ce dépôt.  
**Conformité :** [ ] À contrôler.  
**Capture :** À ajouter dans `docs/captures/` si le contrôle demande une preuve visuelle.  
**Commentaire :** La validation sera consignée après exécution réelle, avec les éventuelles erreurs rencontrées et les corrections apportées.

### T26 : tests d’intégration et couverture

**Travail attendu :** réaliser le contrôle selon l'énoncé du TP4, conserver la sortie de commande ou le résultat dans l'application et la preuve correspondante.  
**Résultat obtenu :** Non renseigné — aucune preuve vérifiée dans ce dépôt.  
**Conformité :** [ ] À contrôler.  
**Capture :** À ajouter dans `docs/captures/` si le contrôle demande une preuve visuelle.  
**Commentaire :** La validation sera consignée après exécution réelle, avec les éventuelles erreurs rencontrées et les corrections apportées.

### T27 : ruff, mypy, pre-commit et CI

**Travail attendu :** réaliser le contrôle selon l'énoncé du TP4, conserver la sortie de commande ou le résultat dans l'application et la preuve correspondante.  
**Résultat obtenu :** Non renseigné — aucune preuve vérifiée dans ce dépôt.  
**Conformité :** [ ] À contrôler.  
**Capture :** À ajouter dans `docs/captures/` si le contrôle demande une preuve visuelle.  
**Commentaire :** La validation sera consignée après exécution réelle, avec les éventuelles erreurs rencontrées et les corrections apportées.

## 7. TP5 — Créer l’interface Streamlit

**Statut au 26/10/2026 :** non démontré par le dépôt personnel consulté. Cette section reste un suivi de travaux à réaliser ou à publier, et non un procès-verbal de validation.

### T28 : installation du kit TP5

**Travail attendu :** réaliser le contrôle selon l'énoncé du TP5, conserver la sortie de commande ou le résultat dans l'application et la preuve correspondante.  
**Résultat obtenu :** Non renseigné — aucune preuve vérifiée dans ce dépôt.  
**Conformité :** [ ] À contrôler.  
**Capture :** À ajouter dans `docs/captures/` si le contrôle demande une preuve visuelle.  
**Commentaire :** La validation sera consignée après exécution réelle, avec les éventuelles erreurs rencontrées et les corrections apportées.

### T29 : interface connectée à l’API

**Travail attendu :** réaliser le contrôle selon l'énoncé du TP5, conserver la sortie de commande ou le résultat dans l'application et la preuve correspondante.  
**Résultat obtenu :** Non renseigné — aucune preuve vérifiée dans ce dépôt.  
**Conformité :** [ ] À contrôler.  
**Capture :** À ajouter dans `docs/captures/` si le contrôle demande une preuve visuelle.  
**Commentaire :** La validation sera consignée après exécution réelle, avec les éventuelles erreurs rencontrées et les corrections apportées.

### T30 : verdicts positifs et négatifs

**Travail attendu :** réaliser le contrôle selon l'énoncé du TP5, conserver la sortie de commande ou le résultat dans l'application et la preuve correspondante.  
**Résultat obtenu :** Non renseigné — aucune preuve vérifiée dans ce dépôt.  
**Conformité :** [ ] À contrôler.  
**Capture :** À ajouter dans `docs/captures/` si le contrôle demande une preuve visuelle.  
**Commentaire :** La validation sera consignée après exécution réelle, avec les éventuelles erreurs rencontrées et les corrections apportées.

### T31 : abstention

**Travail attendu :** réaliser le contrôle selon l'énoncé du TP5, conserver la sortie de commande ou le résultat dans l'application et la preuve correspondante.  
**Résultat obtenu :** Non renseigné — aucune preuve vérifiée dans ce dépôt.  
**Conformité :** [ ] À contrôler.  
**Capture :** À ajouter dans `docs/captures/` si le contrôle demande une preuve visuelle.  
**Commentaire :** La validation sera consignée après exécution réelle, avec les éventuelles erreurs rencontrées et les corrections apportées.

### T32 : gestion des erreurs

**Travail attendu :** réaliser le contrôle selon l'énoncé du TP5, conserver la sortie de commande ou le résultat dans l'application et la preuve correspondante.  
**Résultat obtenu :** Non renseigné — aucune preuve vérifiée dans ce dépôt.  
**Conformité :** [ ] À contrôler.  
**Capture :** À ajouter dans `docs/captures/` si le contrôle demande une preuve visuelle.  
**Commentaire :** La validation sera consignée après exécution réelle, avec les éventuelles erreurs rencontrées et les corrections apportées.

### T33 : traitement d’un CSV

**Travail attendu :** réaliser le contrôle selon l'énoncé du TP5, conserver la sortie de commande ou le résultat dans l'application et la preuve correspondante.  
**Résultat obtenu :** Non renseigné — aucune preuve vérifiée dans ce dépôt.  
**Conformité :** [ ] À contrôler.  
**Capture :** À ajouter dans `docs/captures/` si le contrôle demande une preuve visuelle.  
**Commentaire :** La validation sera consignée après exécution réelle, avec les éventuelles erreurs rencontrées et les corrections apportées.

### T34 : compte rendu, Git et CI

**Travail attendu :** réaliser le contrôle selon l'énoncé du TP5, conserver la sortie de commande ou le résultat dans l'application et la preuve correspondante.  
**Résultat obtenu :** Non renseigné — aucune preuve vérifiée dans ce dépôt.  
**Conformité :** [ ] À contrôler.  
**Capture :** À ajouter dans `docs/captures/` si le contrôle demande une preuve visuelle.  
**Commentaire :** La validation sera consignée après exécution réelle, avec les éventuelles erreurs rencontrées et les corrections apportées.

## 8. TP6 — Packager l’application

**Statut au 26/10/2026 :** non démontré par le dépôt personnel consulté. Cette section reste un suivi de travaux à réaliser ou à publier, et non un procès-verbal de validation.

### T35 : installation du kit TP6

**Travail attendu :** réaliser le contrôle selon l'énoncé du TP6, conserver la sortie de commande ou le résultat dans l'application et la preuve correspondante.  
**Résultat obtenu :** Non renseigné — aucune preuve vérifiée dans ce dépôt.  
**Conformité :** [ ] À contrôler.  
**Capture :** À ajouter dans `docs/captures/` si le contrôle demande une preuve visuelle.  
**Commentaire :** La validation sera consignée après exécution réelle, avec les éventuelles erreurs rencontrées et les corrections apportées.

### T36 : module de prédiction

**Travail attendu :** réaliser le contrôle selon l'énoncé du TP6, conserver la sortie de commande ou le résultat dans l'application et la preuve correspondante.  
**Résultat obtenu :** Non renseigné — aucune preuve vérifiée dans ce dépôt.  
**Conformité :** [ ] À contrôler.  
**Capture :** À ajouter dans `docs/captures/` si le contrôle demande une preuve visuelle.  
**Commentaire :** La validation sera consignée après exécution réelle, avec les éventuelles erreurs rencontrées et les corrections apportées.

### T37 : branchement de l’API

**Travail attendu :** réaliser le contrôle selon l'énoncé du TP6, conserver la sortie de commande ou le résultat dans l'application et la preuve correspondante.  
**Résultat obtenu :** Non renseigné — aucune preuve vérifiée dans ce dépôt.  
**Conformité :** [ ] À contrôler.  
**Capture :** À ajouter dans `docs/captures/` si le contrôle demande une preuve visuelle.  
**Commentaire :** La validation sera consignée après exécution réelle, avec les éventuelles erreurs rencontrées et les corrections apportées.

### T38 : commande sentiment

**Travail attendu :** réaliser le contrôle selon l'énoncé du TP6, conserver la sortie de commande ou le résultat dans l'application et la preuve correspondante.  
**Résultat obtenu :** Non renseigné — aucune preuve vérifiée dans ce dépôt.  
**Conformité :** [ ] À contrôler.  
**Capture :** À ajouter dans `docs/captures/` si le contrôle demande une preuve visuelle.  
**Commentaire :** La validation sera consignée après exécution réelle, avec les éventuelles erreurs rencontrées et les corrections apportées.

### T39 : fabrication de la wheel

**Travail attendu :** réaliser le contrôle selon l'énoncé du TP6, conserver la sortie de commande ou le résultat dans l'application et la preuve correspondante.  
**Résultat obtenu :** Non renseigné — aucune preuve vérifiée dans ce dépôt.  
**Conformité :** [ ] À contrôler.  
**Capture :** À ajouter dans `docs/captures/` si le contrôle demande une preuve visuelle.  
**Commentaire :** La validation sera consignée après exécution réelle, avec les éventuelles erreurs rencontrées et les corrections apportées.

### T40 : installation hors du dépôt

**Travail attendu :** réaliser le contrôle selon l'énoncé du TP6, conserver la sortie de commande ou le résultat dans l'application et la preuve correspondante.  
**Résultat obtenu :** Non renseigné — aucune preuve vérifiée dans ce dépôt.  
**Conformité :** [ ] À contrôler.  
**Capture :** À ajouter dans `docs/captures/` si le contrôle demande une preuve visuelle.  
**Commentaire :** La validation sera consignée après exécution réelle, avec les éventuelles erreurs rencontrées et les corrections apportées.

### T41 : version, tag v0.6.0 et CI

**Travail attendu :** réaliser le contrôle selon l'énoncé du TP6, conserver la sortie de commande ou le résultat dans l'application et la preuve correspondante.  
**Résultat obtenu :** Non renseigné — aucune preuve vérifiée dans ce dépôt.  
**Conformité :** [ ] À contrôler.  
**Capture :** À ajouter dans `docs/captures/` si le contrôle demande une preuve visuelle.  
**Commentaire :** La validation sera consignée après exécution réelle, avec les éventuelles erreurs rencontrées et les corrections apportées.

## 9. Bilan individuel

**Compétences mobilisées ou visées :** analyse de besoins, structuration du projet, environnement Python virtuel, gestion Git/GitHub, tests pytest, apprentissage de texte avec scikit-learn, API FastAPI, CI, contrôle qualité, interface Streamlit et distribution d'un paquet Python.

**Traçabilité :** chaque étape doit pouvoir être associée à une commande, un fichier versionné et, si demandé, une capture d'écran. Les résultats attendus du sujet ne doivent pas être présentés comme des résultats obtenus.

**Travail restant avant une remise complète TP1–TP6 :** vérifier et consigner les sorties manquantes du TP1, publier les fichiers personnels absents, réaliser ou ajouter les livrables des TP2 à TP6, joindre les captures et reporter les résultats réels des tests et de la CI.

**Référence :** dépôt personnel indiqué en première page.
