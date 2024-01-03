# jenkins

TOUS SAVOIR SUR JENKINS

Définition : 

Il s'agit d'un ordonnanceur ou scheduler qui permet de programmer, tester, vérifier et enchainer des tests.
Il est utilisé en intégration continue (CI/CD), permettant de faire tourner des tâches (jobs) de manière intélligente.
Il permet aussi de créer des pipeline permettant de faire du build, du run et de test

Installation : 

sur Windows : elle se fait directement sur le site jenkins.io en choisissant la plateforme que vous utiliser
sur Linux : elle se fait de la manière suivante : 

  > wget -q -O -http://pkg.jenkins-ci.org/debian/jenkins-ci.org.key | sudo apt-key add -

  > sudo sh -c 'echo deb http://pkg.jenkins-ci.org/debian binary/ > /etc/apt/sources.list.d/jenkins.list'

  > sudo apt-get update

  > sudo apt-get install jenkins

NB : la clé d'activation de jenkins se trouve dans le fichier 

  > Pour Linux /var/jenkins_home/secrets/initialAdminPassword

  > Pour Windows C:\ProgramData\Jenkins\.jenkins\secrets\initialAdminPassword

Configuration :

la première configuration consiste à résoudre l'alerte présente au niveau du tableau de bord de jenkins.
Pour cela, il suffit de se rendre dans "Manage jenkins" (administrer jenkins) ....

Ensuite, on fait une configuration du système dans laquelle on peut redéfinir le repertoire home :

  - sur windows, il s'agit du repertoire C:\ProgramData\Jenkins\.jenkins
  - sur Linux, il s'agit du repertoire /var/jenkins_home

On peut configurer dans le même onglet, le nombre de lanceur (exécuteur) de jobs; cela permet à jenkins de paralléliser et de gérer plusieurs jobs à la fois.

On peut également se connecter à un serveur github, avec la gestion des crédentials (login et mot de passe) ainsi que plein d'autres fonctionnalité.

Dans la section "security" (configurer la sécurité globale), on a la gestion du contrôle d'accès c'est à dire comment se connecter à jenkins (base de données, LDAP, ...), les autorisations; la gestion des formats de texte pour mieux personnaliser le tableau de bord jenkins; la gestion des ports sur lesquels les agents jenkins font des échanges valable lorsqu'on à plusieurs jenkins qui travaillent ensemble et par defaut on à le port 50000; la gestion des tokens et des ports à utiliser pour le SSH.

Dans jenkins, on la gestion des users et de rôles qui permettent de différencier les groupes d'utilisateurs ainsi que les différentes tâches à réaliser sur ces profils:

  - il faut créer des utilisateurs selon les besoins de l'entité (exemple: dev, ops)
  
  - ajouter le rôle "Rôle-baser Authorization strategy" au niveau de la gestion des plugins
