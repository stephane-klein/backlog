# Keep it simple, stupid le plus longtemps possible

Depuis quelques années, j'utilise les mots suivants pour décrire mon mindset de développement :

> « Je suis au maximum le principe KISS ([Keep it simple, stupid](https://fr.wikipedia.org/wiki/Principe_KISS)), j'écris le code le plus direct possible
> et quand j'ai trop de "douleur" alors je refactor mon code et j'y ajoute le minimum de sophistication indispensable »

<p align="center"> 
<img src="https://camo.githubusercontent.com/0607e034aee88cce40b832367d44265e01b42654/68747470733a2f2f7777772e6f736e6577732e636f6d2f696d616765732f636f6d6963732f7774666d2e6a7067">
</p>

Ici j'utilise le mot "douleur" dans le sens de ["a pain point"](https://hn.algolia.com/?dateRange=all&page=0&prefix=false&query=pain%20point&sort=byPopularity&type=story) en anglais : quelque chose de casse-pieds, pénibilité, grosse difficulté...

## Partie 1 : la quête du code "parfait"

Pendant la plus grande première partie de ma vie de développeur, j'ai essayé d'écrire le code le plus "propre" possible.

Cela passait par :

- Découper le code en petites fonctions
- Éviter toute duplication de code (mon plus grand combat était le [copy-and-paste programming](https://en.wikipedia.org/wiki/Copy-and-paste_programming), j'ai embêté beaucoup de monde avec cela)
- Organiser le plus logiquement possible l'arborescence des dossiers
- Créer le maximum de classes (programmation objet) avec le maximum de niveau d'héritage (à l'époque c'était cool de faire de l'héritage)
- Utiliser les [Design Patterns](https://en.wikipedia.org/wiki/Design_Patterns) (j'ai aussi creusé la [programmation orientée aspect](https://fr.wikipedia.org/wiki/Programmation_orient%C3%A9e_aspect)...)
- [Don't repeat yourself](https://en.wikipedia.org/wiki/Don%27t_repeat_yourself)
- Découper mon projet en de petits projets ou librairies réutilisables
- Multiplier le nombres de repositories (Git...)
- Écrire du code pérenne dans le temps
- J'essayais d'écrire tout de suite le code dans sa version finale, devoir intervenir à nouveau sur du code était pour moi un échec, la preuve d'un mauvais choix de design.

En résumé, un beau code était pour moi un code "intelligent" avec beaucoup de sophistication.

## Partie 2 : la prise de conscience, le "trop de tout"

Il y a un peu moins de dix ans, j'ai commencé à prendre le chemin inverse, quand j'ai réalisé que je passais mon temps à chercher le code "parfait".

- je me suis rendu compte que je passais énormément de temps à découper mon code en petites fonctions, ce qui impliquait :
    - se creuser la tête pour trouver des noms à ces fonctions
    - de savoir où les placer, dans quels fichiers, dans quels sous dossiers, trouver des noms logiques à ces fichiers et ces dossiers
    - de réorganiser encore et encore le découpage, le naming au fur et à mesure de l'évolution de l'application
- je me suis rendu compte qu'à force d'éviter la duplication de code :
    - que j'avais un code de plus en plus difficile à comprendre
    - qu'il fallait énormément de temps pour une nouvelle personne pour intervenir sur mon code
- j'ai accepté (par expérience) que le code était jetable et que ce n'était pas un échec s'il avait été utile pendant une certaine durée

Mon but était-il de faire du code ou de créer un produit rapidement tout en étant de qualité d'un point de vue fonctionnel ?

### Qu'est-ce qui m'a aidé à prendre ce recul ?

#### Des échecs

De 2007 à 2013 j'ai poursuivi la quête du [Don't repeat yourself](https://en.wikipedia.org/wiki/Don%27t_repeat_yourself), de [« la balle d'argent »](https://fr.wikipedia.org/wiki/Pas_de_balle_en_argent) !

Influencé par [Ruby On Rails](https://fr.wikipedia.org/wiki/Ruby_on_Rails), [Django](https://fr.wikipedia.org/wiki/Django_(framework)),
mon rêve pour améliorer ma productivité était de générer automatiquement les applications à partir du modèle de données et des informations de paramétrages des UX.

Ce fut un échec, un [Yak!](https://github.com/stephane-klein/personnal-notebook/blob/master/003-ne-tonds-pas-de-yaks.md) perpétuel !

Je passais la majorité de mon temps à :

- étudier, comprendre les Framework, sélectionner le "meilleur"
- embrasser toujours plus de complexité en écrivant des extensions, des plugins pour traiter mes cas particuliers
- modifier mes projets pour suivre la monté en version des frameworks
- trouver des solutions pour contourner les bugs des frameworks

Je me suis trouvé de plus en plus dans des situations où je passais par exemple plus d'une semaine pour modifier un cas particulier d'un simple champ select html,
chose qui m'aurait pris 30min sans framework, sans toutes les couches de magies.

À cela s'ajoute en équipe, les heures et les heures de [trolls](https://fr.wikipedia.org/wiki/Troll_(Internet)) de choix de framework.<br />
Chaque développeur a ses préférences, pour tel ou tel framework et tout cela est parfaitement argumentable, car ils ont tous des forces et faiblesses.

C'est suite à cette expérience que j'ai très peur de bâtir une application sur des solutions comme [React Admin](https://github.com/marmelab/react-admin), [Forest Admin](https://www.forestadmin.com/) si je sais que je vais devoir les adapter (solutions qui peuvent être très bien pour faire un [POC](https://fr.wikipedia.org/wiki/Preuve_de_concept) ou un [MVP](https://fr.wikipedia.org/wiki/Produit_minimum_viable)), j'ai très peur de tomber dans un énorme [Yak!](https://github.com/stephane-klein/personnal-notebook/blob/master/003-ne-tonds-pas-de-yaks.md).

#### Des personnes

Des rencontres, par exemples :

- [Mathieu Lecarme](https://twitter.com/athoune) qui m'a dit une fois « j'ai besoin d'intervenir sur ..., je constate que c'est de l'horlogerie fine, j'ai besoin d'aide », je me suis dit que j'avais codé quelque chose de bien trop compliqué
- Je me souviens de la quête vers le minimaliste dans le code de [David Larlet](https://larlet.fr/david/blog/)
    - Est-ce qu'il est possible d'enlever des couches dans la stack ?
- [Philippe Lafoucrière](https://twitter.com/plafoucriere) qui m'a poussé vers du minimalisme, de grosse remise en question en contribuant au code source de Gemnasium
    - Est-ce que mon ORM me fait vraiment gagner du temps ?
    - Est-ce que je peux me passer de cette librairie ?

Ces deux dernières personnes m'ont poussé à réfléchir si je pouvais supprimer des couches, enlever des choses.

> Il semble que la perfection soit atteinte non quand il n'y a plus rien à ajouter, mais quand il n'y a plus rien à retrancher. -- [Antoine de Saint-Exupéry](https://fr.wikiquote.org/wiki/Perfection)

#### L'influence culturelle de technos

Depuis 15 ans, je suis très influencé par [les 19 principes du Zen de Python](https://fr.wikipedia.org/wiki/Zen_de_Python), tout particulièrement :

> - Préfère :
>    - l'explicite à l'implicite,
>    - le déroulé à l'imbriqué,
> - Prends en compte la lisibilité.
> - Mais, à la pureté, privilégie l'aspect pratique.
> - Face à l'ambiguïté, à deviner ne te laisse pas aller.

Les choix minimalistes avec peu de sophistication du langage [Go](https://en.wikipedia.org/wiki/Go_(programming_language)) a conforté la direction [KISS](https://fr.wikipedia.org/wiki/Principe_KISS).

## Partie 3 : prise de décision, le code direct, du code « stupide »

Depuis quelques années, j'essaie d'écrire un code le plus direct possible.

Mon objectif : diminuer au maximum ma [charge cognitive](https://fr.wikipedia.org/wiki/Charge_cognitive).

J'essaie d'ajouter, une librairie, un service ou une couche d'abstraction uniquement si c'est nécessaire fonctionnellement ou si j'ai beaucoup de "douleur" avec la solution actuelle.

J'essaie de garder un code le plus flat possible ([The art of avoiding nested code](https://www.thepythoncorner.com/2017/12/the-art-of-avoiding-nested-code/), [Flat is better than nested](https://medium.com/@ankushchoubey/clean-code-1-flat-is-better-than-nested-leave-when-not-okay-c09ba74090ef), [Avoid Indirection in Code for human readability](http://matthewrocklin.com/blog/work/2019/06/23/avoid-indirection))

J'essaie de découper mon code uniquement si j'ai trop de "douleur" ou si cela apporte de la valeur fonctionnelle, exemple :

- je crée une fonction si j'ai besoin de la tester dans un test unitaire, ce qui fini par être le cas si j'ai trop de difficulté sur une section de code
- je crée une fonction pour éviter de la duplication en suivant la règle [« Rule of three »](https://en.wikipedia.org/wiki/Rule_of_three_(computer_programming))

## Annexes

### Ressources

- [YAGNI](https://en.wikipedia.org/wiki/You_aren%27t_gonna_need_it) (You aren't gonna need it)
- [Overengineering](https://en.wikipedia.org/wiki/Overengineering)
- [KISS principle](https://en.wikipedia.org/wiki/KISS_principle)
- [Don't repeat yourself](https://en.wikipedia.org/wiki/Don%27t_repeat_yourself)
- [Duplicate code](https://en.wikipedia.org/wiki/Duplicate_code)
- [Code reuse](https://en.wikipedia.org/wiki/Code_reuse)
- [Database normalization](https://en.wikipedia.org/wiki/Database_normalization)
- [Rule of three (computer programming)](https://en.wikipedia.org/wiki/Rule_of_three_(computer_programming))
- [Separation of concerns](https://en.wikipedia.org/wiki/Separation_of_concerns)
- [Single source of truth](https://en.wikipedia.org/wiki/Single_source_of_truth)
- [On Coding, Ego and Attention](https://josebrowne.com/on-coding-ego-and-attention/)
- [Duplication is far cheaper than the wrong abstraction](https://news.ycombinator.com/item?id=23739596)
