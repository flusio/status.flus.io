---
title: Articles non actualisés
date: 2019-11-29 18:00
---

Certains utilisateurs et utilisatrices pouvaient ne pas avoir leurs articles
rafraichis régulièrement. Le problème venait d’un bug lié à la vérification des
adresses courriels (le script chargé d’actualiser les articles se terminait
directement si un utilisateur n’avait pas validé son adresse).

Un patch temporaire a été proposé en amont ([référence #2694](https://github.com/FreshRSS/FreshRSS/pull/2694))
et a déjà été mis en production. Une solution plus robuste sera proposée par la
suite.
