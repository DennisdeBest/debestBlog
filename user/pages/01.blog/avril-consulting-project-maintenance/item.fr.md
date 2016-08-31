---
title: 'Avril Consulting, Maintenance de projet'
date: '14:55 08/17/2016'
taxonomy:
    category:
        - blog
    tags:
        - avril
        - maintenance
---

Une fois un projet mit en production et livré au client le travail ne s'arrête pas, une grande partie du travail d'une agence web est la *maintenance* 
 
De temps un temps un client va avoir besoin de nouvelles fonctionnalités ou trouver un *bug* qui à besoins d'être corrigé. 
Une partie de mon travail de stagiaire est de m'occuper de certaine des ces tâches. 
 
Les projets sur lesquelles j'ai pu faire de la maintenance étaient développés avec le framework *Prestshop*, la maintenance présente des challenges différent de la réalisation d'un projet de zéro. 
 
Quand on entame de la maintenance sur un nouveau projet on prie toujours que le développeur nous à laissé une bonne documentation et bien commenté son code, mais c'est rarement le cas. 
 
Le premier projet sur lequel j'ai travaillé était développé sous *Prestashop* 1.6.1, une des dernières versions. Ma tâche était de customiser le module wish list (liste de souhaits) et ajouter des fonctionnalités comme : 
* Créer une nouvelle liste depuis un *dropdown* quand on clique sur un cœur à côté d'un produit 
* remplir l'icône en forme de cœur quand on produit est ajouté à une liste et rajouter les nouvelles listes au dropdowns en *ajax* sans rechargé la page. 
 
Avec un peu de **jQuery**, **PHP** et **AJAX** dans un *override* du module de base ça c'est fait assez facilement. 
 
Avec cette prmière réussite je me suis plutôt confiant pour la suite, mais, ce n'était que de courte durée. 
En effet le deuxième projet était de nouveau sous *Prestashop* mais après avoir lancé une nouvelle *machine virtuelle* je me suis vite aperçu que le projet utilisait *Prestashop* 1.5 qui est radicalement différent de la version d'avant. 
Les demandes sur ce projet étaient :  
* Rajouter du texte à la fin du formulaire de contact 
* Ajouter une barre de recherche sur le site mobile 
* Réparer la géolocalisation 
 
La première tâche était plutôt simple mais du fait que le site n'implémentait pas le **R**esponsive **W**eb **D**esign quelques chose d'aussi triviale que de rajouter du texte cassait entièrement le *layout* de la page. 
En modifiant quelques lignes de **CSS** et quelques images ce fût chose faite en environ 3 heures. 
 
L'implémentation d'une barre de recherche sur le site mobile était plus facile que prévu et impliquait surtout de la configuration dans le *back office* et l'ajout de quelques lignes de **CSS**. 
 
La dernière tâche s'est révélé plus fourbe et touche une corde sensible chez les chef de projets, la *régression*. 
En effet la géolocalisation permet de trouver la magasin le plus proche de l'utilisateur et à toujours fonctionné sans problème puis c'est arrêté d'un coup sans raison apparente. 
Après quelques heures de recherches il s'est avéré que *chrome* était le coupable, depuis la version 50 du navigateur les requêtes de géolocalisation depuis des serveurs non sécurisées (ceux qui ne sont pas en *https*) n'était plus autorisé. 
La seule solution est donc d'obtenir un certificat **SSL** pour le serveur et migrer le site, ceci nécessite l'accord du client car ça dépasse la simple maintenance et les couts de l'opération peuvent être considérables. 
 
Mon expérience dans la maintenance applicative s'arrête à ça pour le moment. 