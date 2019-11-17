# Mes recommandations pour maîtriser la dette technique au quotidien

Tout d'abord, j'invite à lire cet excellent article [« La dette technique est comme une partie de
Tetris. Tout code possède de la dette technique. C'est parfaitement normal. Vous pouvez continuer à jouer
à Tetris même avec quelques trous. »](https://damien.pobel.fr/post/dette-technique-partie-tetris/).


## Règles de bases

Voici les règles que je suis pour garder la maitrise de mes projets :

- **tout développeuur doit à tout moment pouvoir installer, exécuter et utiliser localement un projet.**<br/>
  Comment ?
    - documenter les instructions d'installation et d'exécution, faire tester par plusieurs personnes
    - quand un projet dépend d'infrastructures difficiles ou impossibler à installer, essayer de créer [des composants qui simulent ces dépendances](https://en.wikipedia.org/wiki/Mock_object)
    - faire des efforts pour avoir des données pour les tests ([fixture](https://en.wikipedia.org/wiki/Test_fixture#Software)...) et/ou de démo (sample data)
- **tout développeur (autorisé) doit pouvoir à tout moment déployer le projet (from scratch et de manière incrémentale).**<br />
  Comment ?
    - documenter la procédure de déploiment, faire tester par plusieurs personnes
    - utiliser un outil d'[Infrastructure as Code](https://fr.wikipedia.org/wiki/Infrastructure_as_Code)
    - utiliser un outil de migration de modèle de données (SQL…)
- **tout développeur doit toujours pouvoir tester localement un projet (manuellement ou automatiquement).**<br />
  Comment ?
    - documenter les instructions de test, faire tester par plusieurs personnes
    - mettre à disposition des [fixture](https://en.wikipedia.org/wiki/Test_fixture#Software) et/ou des données de démo (sample data)


## Au quotidien

Au quotidien, quand j'interviens sur un projet et que :

- je vois quelque chose d'améliorable
- je vois quelque chose difficile à comprendre
- je vois du code inconsistent avec le reste du projet
- j'ai beaucoup de difficulté à réaliser une tâche à cause de l'architecture actuelle du projet

alors j'ai deux possibilités :

1. si l'amélioration est rapide alors je l'exécute tout de suite dans une Merge Request
2. ou alors je crée une Issue avec le label « Technical Debt » pour ne pas [tondre un Yak!](https://github.com/stephane-klein/personnal-notebook/blob/draft-how-i-manage-technical-debt/003-ne-tonds-pas-de-yaks.md)


## Qu'est-ce qui n'est pas pour moi de la dette technique ?

Je ne considère pas être de la dette technique les éléments suivants :

- le choix du langage de programmation
- le choix du framework
- un choix d'architecture
- des bugs


## Qu'est-ce que je considère être de la dette technique ?

Tout ce qui m'empêche de travailler correctement sur un projet, par exemple :

- je n'arrive pas à installer l'environnement de developement du projet de manière autonome
- je n'arrive pas à utiliser (« jouer avec ») le projet localement
- je n'arrive pas à tester (manuellement ou non) une fonctionnalité du projet en dehors de son environnement de production
