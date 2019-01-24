# Mon carnet de voyage Bazel

## Genèse du voyage

Vers le [12 janvier](https://twitter.com/klein_stephane/status/1084077842227494913), suis à une discussion avec mon collègue [Albert](https://twitter.com/albttx) au sujet de [CMake](https://fr.wikipedia.org/wiki/CMake) je me suis lancé dans la [tonte d'un nouveau Yak!](https://github.com/harobed/personnal-notebook/blob/master/003-ne-tonds-pas-de-yaks.md) 🤭 : l'étude et l'écriture d'un [POC de Bazel](https://github.com/harobed/poc-bazel-with-golang-and-python) dans un contexte Golang, Python, Docker et monorepos / multirepos.

Voici mon rapport personnel avec [Bazel](https://en.wikipedia.org/wiki/Bazel_(software)) avant le 12 janvier :

- je connais de nom Bazel depuis mi 2017
- je n'ai aucune idée de : son contexte d'utilisation, de son principe de fonctionnement… rien du tout
- quand je regarde le contenu des fichiers [BUILD](https://github.com/kubernetes/kubernetes/blob/master/build/BUILD) dans le projet Kubernetes, cela me fait peur
- mi 2018, dans le contexte d'un projet en monorepos, avec plusieurs services en Go, l'idée d'utiliser Bazel me traverse l'esprit. J'explore un peu la piste en lisant un peu la documentation, quelques articles : j'y comprends rien, cela me semble énorme, complexe, cela me fait peur, j'arrive à la conclusion que c'est overkill, j'abandonne l'idée.

Suite à la discussion au sujet de CMake, j'ai fait des recherches :

- étude de la syntax CMake
- lecture de Threads sur Hacker News et Reddit

Suite à cette étude, voici mon sentiment :

- je lis que l'outil CMake, la syntax… n'est pas très agréable à utilise
- je lis que c'est "vieux", dépassé
- beaucoup de commentaires expliquent que la "réponse" est Bazel
- dans un Thread sur HackerNews, je suis tombé sur un commentaire à propos de [please.build](https://please.build/). Je ne sais pas pourquoi, mais il m'a fait moins peur que Bazel, j'ai compris des concepts. C'est un projet codé en Go, je me suis dit, cela doit être rapide à tester

Résultat :  [je me suis lancé dans un de Please.build POC](https://twitter.com/klein_stephane/status/1084077842227494913).

## Conclusion de mon POC de Please

J'ai réussi très rapidement à faire tomber en marche mon POC de [Please](https://please.build/).

Cette expérience m'a permise de :

- démystifier ces types d'outils de build
- de comprendre les concepts

Problèmes rencontrés avec Please :

- j'ai très vite compris que c'était un solo projet
- qu'il y avait très peu d'utilisateurs et donc de ressources disponibles
- je suis tombé sur des limitations et j'ai vu que Bazel n'avait pas ces limitation et qu'il était bien plus complet

Suite au POC réussi de Please, au fait que les concepts et que le langage de Bazel est le même que Please, je me suis lancé dans un POC de Bazel.


## La grande famille des outils de compilations

Rédaction à venir…
