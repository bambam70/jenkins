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
