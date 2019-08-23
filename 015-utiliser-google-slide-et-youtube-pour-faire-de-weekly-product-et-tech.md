# Utiliser Google Slide et YouTube pour faire des Weekly Product et Tech itérativement

Présentation de l'utilisation des Google Slide et YouTube dans Workflow de développement que je suis actuellement (chez [Spacefill](https://www.spacefill.fr)).

En début de cycle de développement (Sprint d'une ou deux semaines), par exemple la semaine 34 :

- Création de deux nouveaux documents Google Slide (librement accessible, partage global) :
  - « Product Weekly 34 »
  - « Tech Weekly 34 »

Pendant tout le long du sprint :

- [Tout commence par une issue GitLab](https://about.gitlab.com/handbook/communication/#everything-starts-with-a-merge-request)
- Dès que l'on commence à travailler sur l'issue ➡️créer une [Merge Request dès le début](https://about.gitlab.com/2016/10/25/gitlab-workflow-an-overview/), avant de commencer la moindre ligne de code
- Cycle de vie d'une Merge Request :
  - Sélectionner un [template de Merge Request](https://docs.gitlab.com/ee/user/project/description_templates.html) (voir exemple plus bas)
  - Itérer sur le code :
    - Commit / Push réguliérement (je pousse à chaque fois que j'ai quelque chose supplémentaire qui fonctionne, en pratique environ tous les 1/4 d'heure)
  - Dès que j'arrive à un résultat satisfaisant :
    - Je déploie en [Review App](https://docs.gitlab.com/ee/ci/review_apps/)
    - Je prépare correctement les Fixtures dans la Review App pour que la démo soit pertinente
    - Je crée un petit Screencast (assez brut, pas de perte de temps) de la feature que je publie en privé sur YouTube
    - Je crée de nouvelle Slide dans « Product Weekly 34 »
  - Je fais une demande de feature Review (contient le lien vers la Review App + le lien vers la Vidéo YouTube)
    - 🔄 cycle d'itération de feedback / correction au niveau de la feature
  - Je Squash et et je Rebase de code
  - J'écris un commit message qui respecte [How to Write a Git Commit Message](https://github.com/harobed/CONTRIBUTE-skeleton/blob/master/CONTRIBUTE.md#git-workflow)
  - Je fais une demande de Code Review
    - 🔄 cycle d'itération de feedback / correction au niveau du code
  - Je vérifie que tous ce qui est dans la checklist (qui vient du template) en description de la Merge Request est fait
  - Je fais une dernière verification avant application du Merge vers la branche `develop`

En fin de Sprint :

- Présentation à tout le monde des avancés produits via le Google Slide « Product Weekly 34 »
  - Partage des slides dans un channel Slack
- Présentation à l'équipe Tech (ouvert au autre personnes si elles sont curieuses) des sujets de discussions Tech via le Google Slide « Tech Weekly 34 »
  - Partage des slides dans un channel Slack

## Avantage de cette pratique ?

- La création du Screencast de demande de feature review dans le Review App force le développeur à bien finir et présenter son travail
- La check list présente dans le template Merge Request pousse à la rigueur
- La création des slides de présentation au moment de la demande de feature review :
  - rend le travail de reporting plus itératif, plus court et donc moins fastidieux
  - tout le monde participe (il n'y a pas qu'une seule personne qui s'occupe du travail de reporting)
  - cette pratique évite la redondance de reporting
- Les présentations de la Product Weekly avec tous les petits Screencasts fait son Waouh Effect 🤗

## Example de template de Merge Request

- [ ] La MR a été Squash et Rebase ?
- [ ] Git commit message respecte [How to Write a Git Commit Message](https://github.com/harobed/CONTRIBUTE-skeleton/blob/master/CONTRIBUTE.md#git-workflow)
- [ ] Testé dans la review App ?
- [ ] Screencast / Screenshot ?
- [ ] Ajouté dans les Slides de la Weekly Product ou Weekly Tech ? 
- [ ] Migration testées avec les données de prod ?
