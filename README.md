## Jenkins : Normes d'utilisatation

### Introduction
Ce document présente les normes d'utilisation de Jenkins Wafa (Wafa CI).

Wafa CI est la plateforme d'intégration continue qui intégrer les changements effectué par les développeurs

Elle s'occupe de tout le processus post-commit (build, test, deploy) jusqu'à la mise en production.

### Authentification
Pour pouvoir accèder à la plateforme Wafa CI
La plateforme est interfacée avec l'annuaire entreprise des utilisateurs Active Directory,
Pour pouvoir accèder à Jenkins, l'utilisateur doit avoir l'un des rôles suivant :
- Transfo_SI 
- Prestataire
...



### Organisation des jobs

#### Nommage des Job

Les noms de jobs doivent respecter le format suivant : __domaine-application-name-role__.

- __domaine__ : Le domaine métier à qui appartient le composant concerné par le job _ex : prodOTO, sinIRD, sinAT, shared, ..._
- __application-name__ : Le nom de l'application, ou composant concerné par le job. _ex : wafaoto, rs, sird, vircheq, uaa, rbf, ..._
- __role__ : L'objectif, intention du build. _ex : pipeline, build, deploy, dbBackup, ..._

##### Examples :

- _prodOTO-api-pipeline_ : Représente la pipeline de déploiement de l'api production automobile
- _sinIRD-sird-deploy_ : Représente le job de déploiement l'application sird domaine sinistre ird
- _shared-uaa-dbBackup_ : Représente le job de back de base de données du l'application partagée uaa

### Regrouper les jobs du même domaine dans un Folder
 
Pour les équipes (domaines) qui ont plusieurs jobs, il est fortement recommendé de regrouper ces derniers dans un Folder.
Les Folders permettent de mieux organiser les jobs, réutiliser la gestion de droits et de partager un ensemble credentials réservés au domaine.

Les folders sont gérés par les équipes de développement :
* Création et mise à jour du folder
* Création, Configuration, Lancement des Jobs
* Gestion de la sécurité
* Gestion des identifiants globaux

### Sécurité des jobs


### Les identifiants

### Ecriture des pipelines

### Agents disponibles


https://jenkins.io/doc/book/pipeline/pipeline-best-practices/
https://dzone.com/articles/top-10-best-practices-for-jenkins-pipeline
https://dzone.com/articles/how-to-use-the-jenkins-declarative-pipeline?fromrel=true
https://fr.godaddy.com/engineering/2018/06/05/cicd-best-practices/
https://www.digitalocean.com/community/tutorials/an-introduction-to-ci-cd-best-practices
https://docs.huihoo.com/jenkins/enterprise/14/user-guide-14.5/folder-sect-usage.html
https://wiki.jenkins.io/display/JENKINS/Jenkins+Best+Practices
