# Cycle de vie des Repos Git

## Les Repository « POC »

- Pour quel usage ? Dans quel but ?
  - **Pour explorer** la mise en oeuvre d'une librairie, un framework
  - Pour explorer une architecture d'organisation
  - ...
- Niveau de maturité ? 
  - Aucun, **c'est un bac à sable**
  - Le projet peut fonctionner ou non, ce n'est pas important
- Où ?
  - Dans le **GitHub perso** du développeur (example: https://github.com/harobed/poc-swarm-sentry)
  - Dans GitLab, dans namespace des repos perso du développeur (example: `https://gitlab.com/stephane-klein/my-poc`)
- Critères de qualités ?
  - README : optionnel, à écrire au fur et à mesure de la progression du projet
  - Commit message : pas important
- Partage ?<br />
  Même si le projet est en Work In Progress, non exploitable, ces expérimentations peuvent être utiles à d'autre développeur.   


## Les repository « Nursery » / « Pouponnière »

- Pour quel usage ? Dans quel but ?
  - Pour des composants, des services en cours de préparation
  - Le but est d'itérer du draft à un niveau de maturité qui sera accepté dans le repository « Team / Corporate »
- Niveau de maturité ? 
  - Plus avancé que le POC mais pas encore prêt pour une mise en production
  - Le projet peut être parfois cassé
- Où ?
  - Dans GitLab, dans un namespace spécifique, `POC` ou `nursery`
- Critères de qualités ?
  - Les commits peuvent se faire directement dans la branche `master`
  - Commit message : pas important
- Partage ?
  - Public avec le reste de l'équipe, pour rendre transparent l'avancé du projet

Migration d'un projet « Nursery » vers « Team / Corporate » ? une simple copie de fichiers, l'historique Git est mis à la poubelle.


## Les repository « Team / Corporate »

- Pour quel usage ? Dans quel but ?
  - C'est le code qui est en production
- Où ?
  - Dans le namespace public de la team ou de la société
  - Et/ou dans le [monorepos](https://gomonorepo.org/) de l'équipe ou de la société
- Niveau de maturité ?
  - Les branches `master` et `develop` doivent être sable
- Critères de qualités :
  - Documenté, présence des sections :
    - « Getting started »
    - « Setup Development Kit »
    - « Project Overview »
    - « Deployments »
  - Branche `master` et `develop` protégées
  - Toute modification doit passer par des Merge Request et Code Review 
  - GitLab-CI de configuré
  - Déploiement continue
  - Pérennité : partage du savoir, chaque partie du projet doivent être maitrisé par plusieurs personnes de l'équipe