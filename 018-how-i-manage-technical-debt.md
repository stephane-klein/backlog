# Mes recommandations pour maitriser la dette technique au quotidien

Tout d'abord, j'invite à lire cet excellent article [« La dette technique est comme une partie de
Tetris. Tout code possède de la dette technique. C'est parfaitement normal. Vous pouvez continuer à jouer
à Tetris même avec quelques trous. »](https://damien.pobel.fr/post/dette-technique-partie-tetris/).

Voici les règles que je suis pour garder la maitrise de mes projets :

- je dois toujours pouvoir installer localement un projet (quand un projet dépend d'infrastructures difficiles ou impossibler à installer, j'essaie de créer [des composants qui simulent ces dépendances](https://en.wikipedia.org/wiki/Mock_object))
- je dois pouvoir à tout moment déployer le projet
- je dois pouvoir à tout moment déployer from scratch un projet 
- je dois toujours pouvoir tester localement un projet
- je dois faire des efforts pour avoir des données pour les tests ([fixture](https://en.wikipedia.org/wiki/Test_fixture#Software)...) et/ou de démo (sample data)

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
