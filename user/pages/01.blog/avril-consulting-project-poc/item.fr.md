---
title: 'Avril Consulting, Projet POC'
date: '14:55 08/10/2016'
taxonomy:
    category:
        - blog
    tag:
        - avril
        - project
---
 
Alors qu'es ce que l'on y fait chez avril ? Pour ma part ma première tâche était un **P**roof **O**f **C**oncept pour un client.  
 
###Le problème  
 
Laissez moi vous expliquer le cas du client, il vends beaucoup de produits en *drop shipping* ce qui veux dire qu'il ne garde aucun stock et revend simplement les produits de ses fournisseurs.  
 
Il y'a donc plusieurs fournisseurs qui proposent chaqu'un des milliers de produits et notre revendeur les vends sur une vingtaine de sites ainsi que sur des *marketplaces* comme Amazon.  
 
Traditionnellement les catalogues produits étaient maintenue dans des tableaux Excel ce qui peut vite devenir ingérable quand on manipule une grande quantité de produits de différentes sources.  
 
L'autre problème c'est la complétude d'information, il peut être très difficile de voir les informations manquantes ou dupliquées sur une feuille Excel de plusieurs milliers de ligne, on estime que la moitié de l'information produits en ligne est absente ou erronée.  
 
###La solution  
 
![](solution.jpeg?resize=150)![](b_akeneo.png?resize=150)  
 
On m'as demandé de préparer une démo qui adresse ces problèmes, un **P**roduct **I**nformation **M**anager était la réponse.  
 
Plus spécifiquement **Akeneo**, un **PIM** open source basé sur Symfony.  
 
La première tâche était l'import des fichiers Excel mis à disposition par le fournisseur, pour ça il a fallu développer un *connecteur* qui *nettoie* le csv et le transforme en un format gérable par le PIM.  
Ensuite il fallait un moyen de trier les produits pendant l'import, pour ça j'ai créer une interface dans laquelle l'utilisateur peut faire correspondre les catégories qu'il à créé avec les catégories choisi par le fournisseur.  
Après un peu de programmation back et front l'interface fonctionnait et il fallait passer à l'étape suivante : l'export.  
Comme je vous le disais le client revends sur plus de vingt sites spécialisés il faut donc un moyen d'exporter les bonnes catégories à la bonne *web shop*, un *connecteur* d'export et une autre interface de configuration plus tard le développement côté Akeneo était fini.  
 
Le client utilise **Prestashop** (un framework pour le e-commerce) pour ses web shops il a donc fallut créer un *module* pour importer dans Prestashop les données générés par Akeneo.  
 
Après mettre habitué à la structure des modules Prestashop et quelques heures de PHP et jQuery le module d'import fonctionnait comme prévu et avec ça le POC touchait à sa fin.  
Avec le temps restant j'ai exploré les différents moyens de lancer les imports et exports automatiquement à partir de tâches *cron* sur le serveur.  
 
Le moment de vérité est arrivé : la présentation au client et comme on le sait tous si il doit y avoir un bug dans le programme c'est à ce moment qu'il va pointer le bout de son nez. Heureusement pour moi tout c'est bien passé et le client était satisfait.  
 
C'était donc la première tâches qui m'as était confiée par Avril et si vous souhaitez en savoir un peu plus sur le côté technique vous pouvez télécharger la documentation technique que j'ai écrite ici :  
* [Prestashop module](AkeneoImport%20Prestashop%20Module.pdf)  
* [Akeneo bundles](Akeneo%20POC%20Bundles.pdf)  
* [Akeneo functionality](Akeneo%20POC%20fonctionnalit%C3%A9s.pdf)  