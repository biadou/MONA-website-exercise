---
on:
  workflow_dispatch:

permissions:
  contents: read
  issues: read

safe-outputs:
  create-pull-request:
    title-prefix: "[agentic-update] "

tools:
  github:
---

# Flux de travail : Mise à jour automatique du site GitHub Info de Mona

## Objectif
Mettre à jour le contenu du site web "GitHub Info de Mona" en analysant les notes internes ainsi que les nouveautés récentes publiées sur le blog officiel GitHub et le journal des modifications (Changelog).

## Sources à consulter
1. Les notes de Mona situées dans le dépôt.
2. Les actualités récentes du Blog GitHub.
3. Les dernières annonces du Journal des modifications GitHub (Changelog).

## Fichiers autorisés à la modification
- Fichiers contenus dans le dossier du site web (ex: `index.html`, `site/`, ou `docs/`).
- Interdiction de modifier les fichiers de configuration système ou les workflows CI/CD.

## Consignes d'exécution
1. Analyser les trois sources de données pour identifier les nouveautés clés concernant le site de Mona.
2. Rédiger les mises à jour textuelles pertinentes et les appliquer aux fichiers du site.
3. Créer automatiquement une Pull Request vers la branche `main`.
4. Inclure dans la description de la Pull Request :
   - Un résumé structuré des modifications apportées.
   - La liste explicite des sources consultées.
   - Les raisons des choix d'édition.