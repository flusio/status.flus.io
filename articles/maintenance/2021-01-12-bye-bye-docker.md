---
title: Maintenance du serveur
date: 2021-01-12 17:28
status: done
---

Une maintenance du serveur est prévue ce **jeudi 14 janvier à partir de 14h00.**
Une coupure des services [flus.fr](https://flus.fr) et [flus.io](https://flus.io)
est à prévoir pour une durée de 30 à 60 minutes, éventuellement plus en cas de
problème.

L’objectif est de virer Docker du serveur pour m’en simplifier sa maintenance.
Docker est aujourd’hui utilisé pour deux services : <abbr>PHP</abbr> et la base
de donnée PostgreSQL. Il s’agit d’une opération relativement lourde et sujette
à erreurs/problèmes. Je la préparerai donc soigneusement pour limiter la
coupure au strict minimum.

_La maintenance est désormais terminée._

Ce qui a été fait hier :

1. Installation de PHP et modules nécessaires sur le serveur via les dépôts Debian
1. Configuration des sites non critiques (démo, sites de développement) avec le
   PHP des dépôts

Ce qui a été fait aujourd’hui :

1. Redirection des sites critiques vers une page de maintenance
1. Configuration des sites critiques pour utiliser le PHP des dépôts
1. Adaptation des tâches CRON
1. Suppression des fichiers liés à l’installation de PHP via Docker
1. Création d’un dump SQL de la base de données
1. Arrêt et désinstallation du PostgreSQL via Docker
1. Installation de PostreSQL via les dépôts
1. Déplacement de la base sur disque secondaire (pour profiter de plus d’espace
   disque)
1. Configuration de la base
1. Rechargement de la base pour prendre en compte les changements
1. Modification du mot de passe de la base
1. Importation du dump SQL
1. Vérification que les services arrivent à se connecter à la base de données
   et accéder aux données
1. Suppression de la redirection vers la page de maintenance
1. Désinstallation de Docker et docker-compose
