---
title: Serveur hors-service
date: 2021-05-18 17:20
---

Mise à jour de 18h15 : finalement, il s’agissait simplement du système de
fichiers du disque qui était corrompu. J’ai pu résoudre le problème grâce à la
commande `fsck`. Le problème est donc résolu.

---

Mise à jour de 17h55 : il semblerait que le disque n’ait pas totalement
disparu… seulement le partitionnement du disque (ce qui n’est pas beaucoup
mieux). J’ai contacté le support de Hetzner pour en savoir plus. S’il s’avère
que j’ai effectivement perdu les données du disque, la dernière sauvegarde date
de 14h25 (un moindre mal).

---

Les services [flus.fr](https://flus.fr) et [flus.io](https://flus.io) sont
hors-service depuis environ 17h. Il semblerait que le disque dur sur
lequel se trouve les données de la base de données ne soit plus accessible par
le serveur. La raison exacte est encore inconnue. Je suis en train d’investiguer
pour en savoir plus.
