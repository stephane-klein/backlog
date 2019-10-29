# Comment j'utilise Storybook pour créer des apps React ou des Sites statiques

[Voici le Scafolding](https://github.com/stephane-klein/storybook-reactjs-scaffolding) que j'utilise pour mes [Storybook](https://storybook.js.org/) avec ReactJS.

## Quel est mon utilisation de Storybook ?

Je l'utilise pour développer :

- des applications ReactJS
- des sites statiques (par exemple, basé sur [Gatsby](https://www.gatsbyjs.org/))

## Comment je l'utilise ?

- Je crée une [story](https://storybook.js.org/docs/basics/writing-stories/) :
  - par composant React
  - par page de l'application ou du site

## Quels sont les avantages ?

L'utilisation de Storybook permet au développeur :

- au niveau des pages :
  - d'avoir une aperçu rapide et exhaustive de toutes les pages du projet
  - d'accéder directement aux pages sans avoir à se connecter à un compte utiliseur
  - d'accéder aux pages sans avoir besoin de lancer un service backend
  - de créer des pages qui ne sont pas encore activées dans l'application
  - de créer plusieurs version d'une même page pour faire des propositions ou préparer une future version
  - vérifier le bon rendu de la page en fonction des différentes tailles d'écrans (avec [l'addon-viewport](https://github.com/storybookjs/storybook/tree/master/addons/viewport))
  - switcher rapidement d'une langue à une autre (avec [l'addon-i18next](https://github.com/fynncfchen/storybook-addon-i18next#readme))
  - mocker les call d'API GraphQL (avec [l'addon apollo-storybook-react](https://github.com/abhiaiyer91/apollo-storybook-decorator))
- au niveau des composants :
  - d'avoir un environement pour préparer, développer ses composants
  - d'avoir la liste des composants disponible et des exemples d'utilisation

Storybook est pour moi un excellent outil pour faire du développement itératif.

Pour aller plus loin : [Storybook Driven Development](https://medium.com/nulogy/storybook-driven-development-a3c517276c07)
