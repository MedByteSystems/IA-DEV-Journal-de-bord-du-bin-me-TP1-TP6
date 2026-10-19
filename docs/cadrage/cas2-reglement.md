# Fiche de cadrage : Questions sur le règlement intérieur

> Remplir chaque rubrique en une à trois phrases. Les rubriques marquées (obligatoire) sont vérifiées par `pytest`.

## Besoin en une phrase (obligatoire)

Développer un assistant qui répond aux questions des étudiants sur le règlement intérieur en s'appuyant sur les documents officiels et en indiquant les sources utilisées.

## Utilisateur final (obligatoire)

Les étudiants utilisent l'assistant pour retrouver rapidement les règles concernant les absences, les retards, les examens et la discipline, sans devoir parcourir tous les documents.

## Approche retenue (obligatoire)

Cocher une seule case :

- [ ] Règles métier
- [ ] Machine learning
- [x] RAG
- [ ] Modèle génératif seul

## Justification (obligatoire, citer au moins deux critères de la grille : (a) données étiquetées, (b) vérifiabilité, (c) coût par requête, (d) conséquence d'une erreur)

(b) Les réponses doivent être vérifiables dans les articles du règlement ; le RAG permet de retrouver les passages pertinents et de les citer. (d) Une réponse erronée sur les absences ou les sanctions peut induire un étudiant en erreur : les cas ambigus doivent être signalés et confirmés par l'administration.

## Données nécessaires et leur origine (obligatoire)

Le système utilise le règlement intérieur officiel à jour, ses annexes et les documents institutionnels autorisés, fournis par l'école. Un jeu de questions de test avec des réponses validées et les références aux articles permet d'évaluer l'assistant.

## Métrique de succès et seuil d'acceptation (obligatoire)

Sur un jeu d'au moins 50 questions validées, au moins 90 % des réponses doivent être correctes et accompagnées d'une source pertinente. Chaque réponse factuelle doit citer un passage identifiable du document officiel.

## Conséquence d'une erreur et validation humaine prévue (obligatoire)

Une réponse incorrecte peut conduire un étudiant à mal comprendre une règle ou une procédure. Si les documents ne permettent pas de répondre clairement, l'assistant doit le signaler et orienter l'étudiant vers l'administration.

## Risques éthiques ou de confidentialité (obligatoire)

Les questions peuvent contenir des informations personnelles concernant les étudiants. Il faut limiter les données collectées, contrôler les accès, éviter de conserver inutilement les conversations et protéger les documents internes non destinés aux étudiants.

## Approche écartée et pourquoi (facultatif)

Le modèle génératif seul est écarté, car il peut inventer une règle ou répondre sans source vérifiable. Le RAG limite ce risque en reliant les réponses aux documents officiels, sans garantir l'absence totale d'erreurs.
