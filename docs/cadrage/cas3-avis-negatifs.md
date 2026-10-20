# Fiche de cadrage : Priorisation des avis négatifs

> Remplir chaque rubrique en une à trois phrases. Les rubriques marquées (obligatoire) sont vérifiées par `pytest`.

## Besoin en une phrase (obligatoire)

Classer les avis clients négatifs d'un site e-commerce par priorité afin que l'équipe du service client traite d'abord les problèmes les plus urgents ou récurrents.

## Utilisateur final (obligatoire)

L'équipe du service client et le responsable qualité utilisent la liste priorisée pour identifier rapidement les problèmes de livraison, de paiement, de produit ou de sécurité nécessitant une intervention.

## Approche retenue (obligatoire)

Cocher une seule case :

- [ ] Règles métier
- [x] Machine learning
- [ ] RAG
- [ ] Modèle génératif seul

## Justification (obligatoire, citer au moins deux critères de la grille : (a) données étiquetées, (b) vérifiabilité, (c) coût par requête, (d) conséquence d'une erreur)

(a) Un historique d'avis étiquetés par catégorie et niveau d'urgence peut servir à entraîner et évaluer un classifieur. (c) Un modèle de classification peut traiter un grand volume d'avis à faible coût par requête, tandis que (d) les avis mal classés doivent rester vérifiables et pouvoir être remontés par un employé.

## Données nécessaires et leur origine (obligatoire)

Il faut un historique d'avis clients, leurs notes éventuelles, la date, les catégories de problème et des étiquettes de priorité validées par le service client. Les données doivent être minimisées et anonymisées avant leur utilisation pour l'entraînement et les tests.

## Métrique de succès et seuil d'acceptation (obligatoire)

Sur un jeu de test annoté indépendamment, la précision parmi les 20 avis classés comme les plus urgents doit atteindre au moins 0,80 et le rappel de la catégorie « priorité élevée » au moins 0,85. Les seuils sont confirmés avec l'équipe métier avant la mise en service.

## Conséquence d'une erreur et validation humaine prévue (obligatoire)

Un avis urgent mal classé peut retarder la résolution d'un problème important, tandis qu'un faux positif consomme du temps de traitement. Un employé valide les priorités élevées et peut corriger le classement pour améliorer les données d'évaluation.

## Risques éthiques ou de confidentialité (obligatoire)

Les avis peuvent contenir des noms, coordonnées ou informations sensibles. Il faut anonymiser ces éléments, limiter l'accès aux données, surveiller les biais entre catégories de clients et ne pas traiter automatiquement le classement comme une décision définitive.

## Approche écartée et pourquoi (facultatif)

Les règles seules peuvent manquer des formulations variées et des problèmes nouveaux exprimés dans les avis. Un modèle génératif seul est moins adapté à un classement répétable à grande échelle et doit être évalué avant tout usage.
