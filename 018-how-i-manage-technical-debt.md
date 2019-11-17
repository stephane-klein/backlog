# Mes recommandations pour maitriser la dette technique au quotidien

Tout d'abord, j'invite à lire cet excellent article [« La dette technique est comme une partie de
Tetris. Tout code possède de la dette technique. C'est parfaitement normal. Vous pouvez continuer à jouer
à Tetris même avec quelques trous. »](https://damien.pobel.fr/post/dette-technique-partie-tetris/).

Voici les règles que je suis pour garder la maitrise de mes projets :

- je dois toujours pouvoir installer localement un projet (quand un projet dépend d'infrastructures difficiles ou impossibler à installer, j'essaie de créer [des composants qui simulent ces dépendances](https://en.wikipedia.org/wiki/Mock_object))
- je dois toujours pouvoir tester localement un projet
- je dois faire des effort pour avoir des données pour les tests ([fixture](https://en.wikipedia.org/wiki/Test_fixture#Software)...) et/ou de démo (sample data)

Au quotidien, quand j'interviens sur un projet et que :

- je vois quelque chose d'améliorable
- je vois quelque chose difficile à comprendre
- je vois du code inconsistent avec le reste du projet 

alors j'ai deux possibilités :

1. si l'amélioration est rapide alors je l'exécute tout de suite dans une Merge Request
2. ou alors je crée une Issue avec le label « Technical Debt » pour ne pas [tondre un Yak!](https://github.com/stephane-klein/personnal-notebook/blob/draft-how-i-manage-technical-debt/003-ne-tonds-pas-de-yaks.md)