# Fiche de cadrage : Ordonnances incomplètes en pharmacie

> Remplir chaque rubrique en une à trois phrases. Les rubriques marquées (obligatoire) sont vérifiées par `pytest`.

## Besoin en une phrase (obligatoire)

Détecter les ordonnances auxquelles il manque un ou plusieurs champs obligatoires afin d'aider le pharmacien à repérer les informations à vérifier avant toute délivrance.

## Utilisateur final (obligatoire)

Le pharmacien ou le préparateur en pharmacie utilise le système pour repérer les informations manquantes et contrôler chaque ordonnance avant de prendre une décision de délivrance.

## Approche retenue (obligatoire)

Cocher une seule case :

- [x] Règles métier
- [ ] Machine learning
- [ ] RAG
- [ ] Modèle génératif seul

## Justification (obligatoire, citer au moins deux critères de la grille : (a) données étiquetées, (b) vérifiabilité, (c) coût par requête, (d) conséquence d'une erreur)

(b) Les champs requis et les règles de validation doivent être explicitement définis et vérifiables par le pharmacien. (d) Une ordonnance incomplète considérée à tort comme valide peut présenter un risque pour le patient ; des règles explicites et une validation humaine sont donc préférables.

## Données nécessaires et leur origine (obligatoire)

Il faut une liste des champs requis, des règles de validation et des exemples fictifs d'ordonnances complètes ou incomplètes. Ces éléments sont établis à partir des procédures validées par la pharmacie, sans utiliser de données personnelles réelles pour les tests du TP.

## Métrique de succès et seuil d'acceptation (obligatoire)

Sur un jeu de test fictif validé par un professionnel, le rappel des ordonnances incomplètes signalées doit atteindre au moins 0,98. Le système doit aussi indiquer correctement le ou les champs manquants pour chaque ordonnance testée.

## Conséquence d'une erreur et validation humaine prévue (obligatoire)

Une ordonnance incomplète non détectée pourrait être considérée à tort comme valide. Le pharmacien examine les champs signalés et conserve la responsabilité de la décision finale avant toute délivrance.

## Risques éthiques ou de confidentialité (obligatoire)

Les ordonnances peuvent contenir des données de santé sensibles. Les essais utilisent des données fictives ; tout usage éventuel de données réelles doit respecter la confidentialité et limiter les accès aux personnes autorisées.

## Approche écartée et pourquoi (facultatif)

Le machine learning est écarté en première intention, car les champs obligatoires peuvent être contrôlés par des règles explicites sans nécessiter un grand jeu de données étiquetées.
