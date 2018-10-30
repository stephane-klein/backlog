# Utilité et contenu d'un README

## Quelles sont les questions auxquelles doit répondre le README d'un projet ?

Quand j'arrive sur un projet logiciel, je me pose les questions suivantes :

- Sous une forme succincte, quelle est la fonction du projet ?
- Pourquoi ce projet a-t-il été créé (son contexte, la problématique rencontrée) ?
- Quelles sont les solutions alternatives à ce projet ? Quelles sont les forces et faiblesses de ce projet par rapport aux alternatives ? (optionnel : limité aux librairies, outils…)
- Comment lancer une démo rapidement ? (pour mieux comprendre l'usage du projet)
- Sous une forme succincte, quels sont les briques téchnologiques du projet ? ([software stack](https://en.wikipedia.org/wiki/Solution_stack))
- Comment compiler le projet ? (optionnel : limité aux langages compilés ou à la génération d'images Docker)
- Comment lancer les tests unitaires et fonctionnels ?
- Où est le dashboard du système de CI ([Intégration Continue](https://en.wikipedia.org/wiki/Continuous_integration) des tests) ?
- Comment déployer ce projet ?
- Quel est le workflow de développement du projet ?
- Quels sont les trucs et astuces à savoir pour contribuer au code source du projet ?
- Comment contacter les développeurs ?


Pour un projet interne à une société, je me pose des questions supplémentaires :

- Qui a besoin de ce projet ? Dans quel contexte ?
- Comment et où est déployé ce projet ?
- Où sont les environnements de test, staging... ?
- Où est le dashboard du système de CD ([Déploiement Continue](https://en.wikipedia.org/wiki/Continuous_delivery)) ?
- Qui est le [Product Owner](https://en.wikipedia.org/wiki/Scrum_(software_development)#Product_owner) du projet ? Quels sont les membres du projets ?

J'espère trouver réponse à toutes ces questions dans le fichier README du projet.


## Exemple de template de README

J'ai publié sur GitHub le projet [harobed/README-skeleton](https://github.com/harobed/README-skeleton) qui contient un exemple de README.
