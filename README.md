# DEVOPS CONCEPTS

## METHODES CLASSIQUES ET METHODE AGILE

Avant le concept devops, les développements étaient réalisés en mode cascade.

Les phases de ce développement suivent rigoureusement un ordre spécifique, à savoir:
- La définition des exigences
- La Conception de l'architecture matérielle définie dans le cahier de charge
- La réalisation des exigences spécifiées en amont
- La validation après les differents tests  
- Le déployement et la maintenance applicatif.


![556px-Modèle_en_cascade_générique_avec_livrables](https://user-images.githubusercontent.com/48319188/114306813-59cd2a80-9add-11eb-8e6b-934221322756.png)

source:  [wikipedia: modèle en cascade](https://www.google.com/url?sa=i&url=https%3A%2F%2Ffr.wikipedia.org%2Fwiki%2FMod%25C3%25A8le_en_cascade&psig=AOvVaw1O0CEeTdwCPtRHgVGOU1rd&ust=1618237479392000&source=images&cd=vfe&ved=2ahUKEwjj6Z7CsvbvAhXHAGMBHd_6DRMQr4kDegUIARDJAQ)

Cette méthode faisait que la mise en service des exigences mettait assez de temps. De plus, les demandes de changement par le client final au cours du développement ont un impact négatif sur le délai de livraison. 

Pour pallier ce problème, le mode **agile** à pris de l'ampleur. Il est le plus utilisé dans les differentes compagnies car le client est impliqué dans le processus de développement des exigences. Ce mode, est plus flexible aux changements grâce sa collaboration avec l'utilisateur final c'est-à-dire le client.

L'idée de ce mode, est que le deploiement des fonctionnalités se fait par sprint de manière régulier, en développement des features au fur et à mésure afin de donner au client une certaine visibilité. Cela permet au client d'avoir une application fonctionnelle en peu de temps, qu'il va tester et faire son feed back pour les fonctionnalités suivantes qui seront délivrées dans le prochain lot.

Conclusion: L'idée majeure du mode agile en comparaison au mode en cascade c'est de mettre regulièrement en production des applications par lot de fonctionnalité.

## DEV ET OPS ( en guerre)

Le **DEV** se charge de développer les fonctionnalités selon les exigences du clients en produisant plusieurs versions de l'application par deploiement.

L'**OPS** (les administrateurs IT)lui son rôle est de s'assurer de la stabilité des applications avant de les pousser en production.

Très souvent, il y a une incompréhension des _DEVS_ et des _OPS_ sur certaines exigences avant la mise en production des fonctionnalités de l'application à déployer.
(Exple : problème de version de package et de logiciel, conflit de port, absence de test des differentes fonctions, les critères de sécurité... )

C'est pour faire face à ces incompréhensions que le mouvement **DEvOps** voit le jour.

## DevOPS ( reconcilier)

Ce mode de travail va permettre une meilleure collaboration entre les Développeurs et les Opérateurs, les Opérateurs seront consultés à chaque étape du développement pour qu'ils puissent donner leurs avis sur certains choix des développeurs.

![images](https://user-images.githubusercontent.com/48319188/114310981-2abeb500-9aed-11eb-826d-99daa35aa4ac.png)

###  ETAPES DU DEVOPS

#### Planification

C'est une étape d'analyse des besoins, cette phase d'analyse doit se faire avec les Opérateurs. 

#### Réalisation 
Cette phase inclut 
- la conception logicielle
- Le design de l'appli
- Le développement de code ( tests unitaires inclus)

#### Versionnage
Dans cette phase on va plutot gérer les différentes versions de l'application

#### Assemblage ou package

L'idée de cette étape et de faire l'ensemble des tâches requis en vue de la version finale de l'application, la release.
Dev-> staging (preprod)->prod


#### Test en continue
Cette phase comprend des tests continus, qu'ils soient manuels ou automatisés, et vise à assurer une qualité de code optimale.

#### Deploiement (Release)

C'est l'étape de la mise en production de l'application, dans cette étape nous avons la livraison d'une fonctionnalité de l'application.
Cette étape comprend aussi les plans d'actions en cas d'indisponiblité de l'application.

#### Opérationnalisation ( Configuration ou exploitation)

Cette étape comprend l'ensemble du processus de configuration, de gestion de l'application en production.

#### surveillance ( Monitoring ou Supervision)

Dans cette partie on s'assure de la disponibilité de l'application et sa performance. On collecte les informations sur l'expérience des utilisateurs, les métriques sur les performances de l'application en production,...

### AVANTAGES DU DEVOPS

- Deploiement régulier de nouvelle fonctionnalité
- Reduction du nombre de burg lors des mises en production
- Augmentation de l'efficacité
- Meilleure utilisation des ressources
- Automatisation accrue pour réduire le nombre d'erreur humaine
- 
##  PRATIQUES DEVOPS

### Collaboration

Pour tirer profit de cette méthode il va falloir une bonne collaboration entre le développeur et l'administrateur, cette collaboration passe par une communication afin de s'assurer de l'avancement ou de la disponibilité de l'application

### Automatisation

Le but de l'automatisation est de 
- Réduire l'erreur humaine
- Permettre la reproductibilité sur tous les serveurs
- Réduire la charge de travail pour se concentrer sur d'autres fonctionnalités ( Productivité)
- Permettre le self-service

### Intégration continue( CI)
C'est la phase de planification et de codage.
Dans cette étape après développement, le code est poussé sur le serveur de subversion (par exple Gitlab) ce dernier sera compilé et intégré pour validation. Les erreurs pourront être vérifiées et une alerte sera transmise pour signaler d'éventuels problèmes.

outils utilisés: 
- Intégration de code : Git
- Intégration automatique: Jenkins, Gitlab ci


source: [netapp](https://www.netapp.com/fr/devops-solutions/what-is-devops/)
