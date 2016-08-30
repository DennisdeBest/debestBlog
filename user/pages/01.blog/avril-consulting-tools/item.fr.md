---
title: 'Avril Consulting, Les outils'
date: '14:55 07/28/2016'
taxonomy:
    category:
        - blog
    tag:
        - avril
        - tools
---

>It's best to have your tools with you. If you don't, you're apt to find something you didn't expect and get discouraged.  
><cite>Stephen King</cite>  
  
Avoir les bons outils c'est la moitié du travail, ceci est autant vraie pour la construction d'une maison que d'un logiciel ou un site web. 
  
Jetons un œil à la boîte d'outils du développeur.  
  
###Version Control  
  
![](git.png)  
  
Le contrôle de version est quelque chose de très chère à tous les développeurs. 
Il permet de suivre toutes les modifications sur le code et de revenir à n'importe quel *commit* (sauvegarde) en un seul clique. 
L'autre gros avantage c'est quand on travail en équipe, en effet en utilisant un *répositoire* git chaque développeur se crée une copie du code pour travailler dessus et peut se créer ainsi des *branches* sans que le fait que quelqu'un d'autre modifie le même code viennent perturber le travail. 
Une fois que le développeur à fini de travailler sur son côté du code il peut *merger* sa branche sur le code en commun, on évite ainsi tout les maux de têtes liées aux conflits qui peuvent apparaître quand plusieurs personnes modifient le même code. 
Les outils de versioning que nous utilisons (et la grande majorité des développeurs) c'est **GIT** et le *répositoires* (projets) sont stockés sur un serveur *gitlab* privé. 
  
**Gitlab** est une page web qui propose une interface pour la gestion du versioning. Il permet de voir facilement les différentes branches, commits, merge et contient tous les outils pour une gestion de version privé et sécurisé. 
  
##IDE's  
  
![](phpstorm.png)  
  
*I*ntegrated *d*evelopment *e*nvironments, ces outils viennent dans pleins de déclinaisons mais dans l'ensemble sont là pour répondre à une même problématique, regrouper dans un logiciel toutes les différents fonctionnalités dont un développeur peut avoir besoin pour écrire son code. Lequel choisir est une questions de préférences personnel, d'habitude et de coût. Quelques IDE pour le développement web :   
* **Sublime Text**, plus qu'un simple éditeur de texte il permet par exemple de faire de l'auto complétion de texte, du coloriage syntaxique dépendant du langage. Gratuit pour une utilisation personnel, il est présent sur le pc de beaucoup de développeurs. 
* **Atom**, un IDE très léger développé par *github*, il y a beaucoup de plugins de disponible pour pouvoir le configurer en fonction du type de projet. 
* **Adobe dreamweaver**, on en a déjà parlé dans un autre post, c'est un IDE très lourd mais qui vient avec pas mal de fonctionnalités comme la connexion au serveurs FTP, un éditeur WYSIWYG. Facile à prendre en main pour un débutant mais trop lourd et pas assez configurable pour du travail plus poussé. 
* **PHP Storm**, mon ide préféré, il à tout ce dont on a besoins, connexions au serveurs, intégration *git* et *xdebug*, un terminal, la coloration syntaxique et j'en passe. Il y a également pas mal de plugins de disponibles pour les fonctionnalités spécifiques dont on peut avoir besoin, comme par exemple l'auto complétion pour les projets *symfony*. 
  
## Communication  
  
![](slack_logo_wide.png)  
  
Aujourd'hui tout le monde à une adresse e-mail mais depuis que le premier mail à été envoyé par Ray Tomlinson à lui même en 1971, la communication par internet à beaucoup évolué. Au bureau nous utilisons **Slack**, un outils très pratique de chat qui permet de faire des canaux par sujet ou projet et d'y inviter les gens concernés, il permet également le partage de documents. 
  
##La gestion de projets 
  
![](logo.png)  
  
Dans le dernier post je vous ai parlé du fameux *SCRUM board* sur lequels sont disposé les tâches de la journée et biensûr ces tâches doivent venir de quelque part dans notre cas c'est 
**Redmine**.  
**Redmine** est un outil de gestion de projet en ligne qui permet au gestionnaire de projet de créer des *tickets* (tâches) et de les assigner aux différentes personne de l'équipe. 
Chaque tâches peux avoir une estimation de temps et une fois la tâche fini on peut comparer le temps estimé avec le temps que la tâche à réelement pris et sur l'échelle d'un projet cela permet de voir la rentabilité facilement. 
  
##Environments  
  
![](Vagrant.png)  
  
A ne pas confondre avec les IDEs l'environnement c'est le paysage sur lequel notre application va tourner. 
Traditionnellement chaque développeur installait sur sa machine un outil comme **LAMP**, qui signifie **L**inux, **A**pache (le serveur web le plus courant avec 50% des sites qui tournent dessus), **M**ySQL (serveur de base de données très courant également) et **P**HP (langage de programmation web très populaire et puissant). 
Le problème avec cette manière d'opérer c'est la compatibilité, en effet quand on travail à plusieurs sur un projet il est important de tous avoir les mêmes versions des logiciels voir même les mêmes que sur le serveur sur lequel l'application va être déployé. 
Pour contourner ce problème nous utilisons des *machines virtuelles* (un ordinateur virtuel à l'intérieur du système opérateur). 
Pour s'assurer que c'est machines virtuelles aient bien le même *paysage* nous utilisons **Vagrant** en combinaison avec **Ansible** pour créer rapidement et de manière constante des machines virtuelles. 
  
Voici donc les principaux outils dont on se sert pour développer des applications web au sein d'avril, si vous en utilisez d'autres n'hésitez pas à laissez un commentaire ;).  
  
  
 
  