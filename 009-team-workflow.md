# Team Workflow

Voici un workflow d'équipe de Dev/DevOPS que j'aime utiliser. Il fonctionne aussi bien en remote, semi remote que sur site.

Outils :

- logiciel de chat (Slack, Mattermost…)
- gestionnaire de tickets (GitLab, GitHub, Jira…)
- gestionnaire de versions (GitLab, GitHub…)

Pratiques :

- en début de journée, poster un message sur le channel de l'équipe :
	- pour dire bonjour
	- optionnellement indiquez sa position physique :
		- En mode bureau flex ou coworking cela peut être utile pour rassembler un peu l'équipe sur un même lieu
	- indiquer le ticket sur lequel on travail
- utiliser principalement le channel le l'équipe comme un [Watercooler Channel](https://revelry.co/watercooler-channel/), pourquoi : les informations importantes doivent être échangées via le système de ticket (dans les descriptions ou commentaires)
- quelques fois, dans des situations difficiles, les commentaires des issues ne sont pas suffisants, des échanges synchrones sont nécessaires, dans ce cas :
	- si **toutes** les personnes concernées par le sujet sont "sur site" : passer en mode échange oral
	- sinon : passer en mode chat privé
		- À la fin le l'échange, mettre à jour les informations dans l'issue de manière très factuelle, courte et précise :
			- les inputs utiles (des urls, pièces jointes)
			- un "rationalize" (pourquoi ces choix)
			- la conclusion : la prise de décision, les actions concrètes
- si on travaille sur du code :
  - créer une Merge Request dès le début, avant de commencer la moindre ligne de code
  - pusher régulièrement ses avancées en mode Work In Progress
  - faire un [git squash](https://git-scm.com/book/fr/v1/Utilitaires-Git-R%C3%A9%C3%A9crire-l-historique) à la fin ou avant de demander un code review d'étape
  - essayer autant que possible de faire les MergeRequest/Commit atomic, c'est à dire, un commit doit résoudre une tâche dans son entièreté
- quand on a fini une tâche :
  - mettre à jour le ticket de la tâche avec les informations suivantes :
    - ajouter en commentaire ou dans la description les liens vers la Merge Request ou le/les commits qui résolvent le ticket
    - si le commit n'est pas suffisant pour comprendre ce qui a été fait, indiquer les informations supplémentaire en commentaire du ticket. Exemple : indiquer sur quel environnement le changement a été déployé, si il a été bien testé, par qui, quels sont les résulats du test
    - ne pas oublier de demander une review ou de fermer le ticket
- être précis dans ses messages :
 	- utiliser au maximum les urls plutôt que "d'indiquer les choses". Exemples :
		- donner l'url d'un ticket plutôt que son numéro
		- donner l'url de l'ancre au bon endroit d'une doc, plutôt que d'expliquer où dans la doc en question
		- donner l'url d'un document, plutôt que d'expliquer où se trouve le document
		- donner l'url de la conversation Slack, plutôt que de dire « c'est écrit plut haut »
- donner des feed-back rapides :
	- utiliser la réaction 👀 pour indiquer que vous êtes en train de lire une url ou un message
	- utiliser la réaction ✅ pour indiquer que vous avez pris connaissance de l'information du message
	- utiliser la réaction 🤔 pour indiquer que vous avez pris connaissance de l'information du message mais que vous ne répondez pas parce que je vous êtes encore en phase de réflexion
	- utiliser la réaction 👍 pour indiquer que vous êtes d'accord avec l'information du message ou pour féliciter une action
- il est souvent difficile de suivre les notifications des systèmes de gestions de tickets, dans ce cas :
	- indiquer sur le channel quand on prend ou qu'on travaille sur un ticket
	- ping en privé de la personne quand on a posté un message dans une issue qui demande une réponse rapide
	- demander les codes review sur le channel
- gestion des niveaux d'urgences (si quelque chose bloque beaucoup ou non) :
	- si ce n'est pas très bloquant ou urgent : mettre à jour uniquement l'issue
	- si c'est moyennement urgent : poster sur le channel
	- si c'est urgent : poster en message direct privé
- éviter les interuptions utilisant la fonctionnalité « Mettre les notifications en pause » pendant 30 minutes :
	- cela a l'avantage d'indiquer à vos contacts (via [une icône](https://get.slack.help/hc/fr-fr/articles/214908388-Diff%C3%A9rer-les-notifications-avec-le-mode-Ne-pas-d%C3%A9ranger)) que vous êtes en mode « ne pas déranger »
	- les notifications sont réellement mises en attente (elles ne sont pas perdus) pendant cette période
  - cela permet de mettre plus ou moins en pratique une [Technique Pomodoro](https://fr.wikipedia.org/wiki/Technique_Pomodoro)
