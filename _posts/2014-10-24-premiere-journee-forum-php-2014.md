---
layout: post
title: "Forum PHP 2014 - Première journée"
date: 2014-10-24 09:00
tags: [php, event]
description: Mes retours sur cette première journée de conférences
permalink: 2014/10/24/premiere-journee-forum-php-2014
thumbnail: comment
categories: event
---

J'ai pu, cette année, me rendre au Forum PHP, organisé par l'[AFUP](http://afup.org/pages/site/) au Beffroi de Montrouge, en région Parisienne. Voici un petit résumé de cette première journée de conférences, plutôt orientées vers le [devops](https://fr.wikipedia.org/wiki/Devops) et l'industrialisation des développements.
<!-- more -->

Après une courte introduction par [Fabrice Bernhard](https://twitter.com/theodo), président de l'AFUP, je me suis rendu à la conférence "__ La mesure, ce n'est pas que pour le devops __". Présentée par Olivier Garcia et Patrick Allaert, les deux orateurs nous expliquent pourquoi, lorsqu'on propose un nouveau service sur le web, tout doit être mesuré, de la vue des pages à un simple clic sur le bouton de connexion ou sur le bouton d'annulation de souscription, nous présentant l'innévitable __ Google Analytics __, mais également __ StatsD __ qui, associé à Graphite et des interfaces comme [Grafana](http://grafana.org/) ou [Tessera](https://github.com/urbanairship/tessera), peuvent proposer un sérieux concurent au quasi monopôle de la solution du géant américain. __ A tester __ !

A suivi la conférence de Nicolas Silberman et Sébastien Angele, "__ Industrialisation des environnements de dev avec Puppet et Amazon __", ou comment faire co-exister des environnements de dev, de recette/démo, de préprod et de prod (relativement) facilement en utilisant des instances <span title="Amazon Web Services">___ AWS ___</span> associé à __ Puppet __ (avec lequel ils nous conseilleront d'utiliser Foreman), ou avec Chef, qui propose des recettes plus simples que Puppet, et s'interface bien avec des services tels que [Packer.io](https://packer.io/), qui permet de générer des images utilisables directement dans AWS. Intéressante dans le fond, je me pose tout de même quelques questions sur certaines méthodes utilisées, notamment pour __ la gestion des images/fichiers __, qui, dans l'état actuel, sont dédoublés pour chaque environnement.

Après une innévitable pause coca (il n'y avait plus de café; il faut dire qu'avec environ 300 développeurs, le café pars très vite !), Johannes Schitt nous a parlé __ qualité de code __, et des avantages inhérents à avoir un code propre, commenté (et testé ?), que ce soit pour le __ confort du développeur __ et de ses collègues ou pour la partie businness, parce qu'un code propre permet de __ diminuer les retours clients __, et donc __ augmenter le retour sur investissement __ et de mettre en place une relation de confiance avec ses partenaires. Cela permet également de ne pas être dépendant d'un seul développeur sur une application, le code étant compréhensible par n'importe qui dans l'équipe (y compris un nouvel arrivant). Il nous a parlé de [Scrutinizor](https://scrutinizer-ci.com/), un outil permettant de mesurer la qualité du code et capable de détecter des améliorations.

Et pour terminer la matinée, [Olivier Dolbeau](https://twitter.com/odolbeau) nous a parlé log en présentant le trio [ElasticSearch/Logstash/Kibana](http://www.elasticsearch.org/) ([les slides](https://speakerdeck.com/odolbeau/laisse-pas-trainer-ton-log)) pour gérer ses logs côté serveur, et [Monolog](https://github.com/Seldaek/monolog) pour le côté appli, nous rappelant que, lorsqu'on log, le contexte est __ très __ important !

(Piouf, je n'avais pas écrit d'article aussi long depuis longtemps ! On est à la moitié)

Après un bon petit sandwitch (et une petite bière, je ne vous le cacherais pas ), [Jordi Boggiano](https://twitter.com/seldaek), Lead Developper de [Composer](https://getcomposer.org), nous a donné quelques petits conseils pour mieux utiliser Composer au quotidien (privilégier l'utilisation du ~ par exemple). Conférence très agréable, et faite avec humour. Les questions ont ensuite soulevées un problème récurrent dans le monde de l'Open Source : Composer, ainsi que son service [Packagist](https://packagist.org/), sont __ totalement financés par Jordi __ ("C'est pour Bibi", pour le citer), le "forçant", pour essayer de rentrer dans ses frais, à proposer un service payant (pour utilisation commerciale), [Toran Proxy](https://toranproxy.com/). C'est l'un des __ torts de l'Open Source __ aujourd'hui, qui aura du mal à être résolu de si tôt.

A suivi [Marc Hugon](https://twitter.com/marc_hugon), qui nous a présenté l'évolution et la gestion des __ tests fonctionnels __ chez Maisons du Monde, qui ont commencé avec Selenium, de plus de plus difficile à maintenir au fur et à mesure de la complexification du site et très lourd, jusqu'à l'utilisation de __ Rubymine et Cucumber __ aujourd'hui, permettant aujourd'hui d'avoir une équipe de __ 3 testeurs parmi les 15 développeurs __ de l'équipe technique (et apparemment, ils n'ont pas le temps de chômer !). Une mise en place qui s'est faite dans la douleur, mais qui aujourd'hui permet à Maisons du Monde de réaliser __ plusieurs centaines de tests __ fonctionnels chaque jour, et de __ mettre en prod sereinement __ 2 à 3 fois par semaine.

François Dume nous a ensuite parlé [{json:api}](http://jsonapi.org/), et de comment le standard a été implémenté chez ARTE, avec une volonté d'__unifier__ les différentes API qu'ARTE fournit, et le souhait de se rapprocher de l'__Open Data__. Basé sur 2 applications Symfony, une base MongoDB, un serveur RabbitMQ et un proxy NginX associé à du LUA, j'ai trouvé l'ensemble relativement __cohérent__, mais également assez lourd, nécessitant de maintenir une __base de code importante__ (et pourquoi utiliser un Symfony pour s'occuper uniquement de l'authentification OAuth ?).

Pour terminer cette journée, de nouveau une conférence DevOps par Reynald Mandel : "Déploiement continu : un pas de plus vers le DevOps", ou comment les développeurs et les administrateurs système (ops), et même toute l'équipe tech, devrait se comporter pour __faciliter le travail de chacun__, et ainsi se rapprocher constamment du __déploiement continu__ et de l'__intégration continue__, avec un code propre, testé et passé en prod sans problème.

Voilà mon petit bilan de cette première journée. Une journée riche, qui n'est que la première de cet évènement de la communauté PHP française. En avant pour la seconde journée !
