# Contributing Guidelines

Merci de contribuer au projet 2048 !

## Workflow
- Ne pas pousser directement sur `main`.
- Créer une nouvelle branche pour chaque modification.
- Faire une Pull Request vers `main` et attendre l’approbation.

## Tests
- S'assurer que les tests passent (`mvn test`) avant de proposer une PR.

## Qualité & CI
- Le pipeline CI doit être vert avant le merge.
- Le code doit compiler (`mvn package`).

## Sécurité
- Ne pas committer de secrets.
- Dependabot et CodeQL doivent rester activés.
