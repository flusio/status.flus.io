---
title: Mise à jour de Flus
date: 2021-09-06 11:45
status: done
---

Une mise à jour de Flus est prévue pour le **jeudi 09 septembre 2021 à partir
de 9h00**. Une coupure du service app.flus.fr est à prévoir et ne devrait pas
dépasser le quart d’heure.

Habituellement les mises à jour de ce type ne nécessitent pas de coupure du
service. Cette fois-ci toutefois, plusieurs migrations délicates de la base de
données vont être appliquées. Je préfère donc le faire en étant serein sur le
fait que personne ne viendra interférer avec ces migrations.

_La maintenance est désormais terminée._

Comment ça s’est passé ? À peu près correctement, mais deux migrations ne se
sont pas exécutées immédiatement parce qu’il y avait trop de données à migrer
d’un coup. J’ai simplement migré ces données par lots plus petits et tout s’est
ensuite bien passé !
