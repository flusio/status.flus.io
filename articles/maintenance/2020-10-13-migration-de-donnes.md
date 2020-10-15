---
title: Migration de données
date: 2020-10-13 18:00
status: done
---

Afin de migrer des données liées aux paiements, je couperai l’accès au service
[flus.io](https://flus.io) le **jeudi 15 octobre à partir de 09h00.** La
migration devrait prendre moins de 30 minutes. Une mise à jour du service sera
effectuée en même temps.

_La maintenance est désormais terminée._

Ce qui a été fait :

1. redirection du service flus.io vers cette page de maintenance
1. mise à jour du serveur via le gestionnaire de paquets + reboot
1. mise à jour des images Docker
1. mise à jour de l'extension Flus pour flus.io
1. création d'un compte de paiement (sur flus.fr) pour chaque compte utilisateur
   de flus.io
1. mise à jour des factures pour les attacher aux comptes de paiement
   correspondants
1. suppression de la redirection vers la page de maintenance
1. vérification que tout fonctionne correctement
