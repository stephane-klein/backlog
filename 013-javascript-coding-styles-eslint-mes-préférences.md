# Javascript Coding Style, ESLint, mes préférences

Voici un extrait de la configuration [ESLint](https://eslint.org/) que j'utilise :

```
{
    ...
    "extends": [
        "eslint:recommended",
        "plugin:react/recommended",
        "plugin:jest/recommended"
    ],
    ...
    "rules": {
        "indent": [
            "error",
            4
        ],
        "semi": [
            "error",
            "always"
        ],
        "space-before-function-paren": [
            "error",
            {
                "anonymous": "always",
                "named": "never",
                "asyncArrow": "always"
            }
        ]
    }
}
```

## À propos de StandardJS

Je connais le projet [StandardJS](https://standardjs.com/), j'aime l'idée de fédérer un maximum de
développeurs Javascript autour d'une même configuration de coding style.<br />
Je viens du monde Python où presque tous les projets suivent le coding style défini par la
[PEP 8](https://www.python.org/dev/peps/pep-0008/) et j'aime cela 🙂.

Cependant, il y a certaines de règles définies par StandardJS qui me rendent la lecture du
Javascript difficile ou tout du moins, désagréable.

En attendant de changer d'avis, voici les règles ESLint que j'utilise.

## Indentation

```
    "rules": {
        "indent": [
            "error",
            4
        ],
```

## Utilisation des Semicolons

```
        "semi": [
            "error",
            "always"
        ],
```

## Pas d'espace entre le nom de la fonction et la paranthèse

```
        "space-before-function-paren": [
            "error",
            {
                "anonymous": "always",
                "named": "never",
                "asyncArrow": "always"
            }
        ]
```

Documentation : [« Require or disallow a space before function parenthesis (space-before-function-paren) »](https://eslint.org/docs/rules/space-before-function-paren) 