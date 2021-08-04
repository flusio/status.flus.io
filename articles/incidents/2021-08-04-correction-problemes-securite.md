---
title: Correction de 2 problèmes de sécurité
date: 2021-08-04 18:07
---

Au début du mois de juillet, 2 problèmes de sécurité m’ont été remontés.

Le premier concernait le mécanisme de réinitialisation de mot de passe. Si un
attaquant réussissait à obtenir un lien de réinitialisation (sans l’utiliser)
et que l’utilisateur ciblé modifiait lui-même son mot de passe, le lien de
réinitialisation restait valide. L’attaquant pouvait ainsi reprendre le
contrôle du compte. Le risque était plutôt faible puisque cela signifiait que
l’attaquant avait pris, au préalable, le contrôle de la boîte email de
l’utilisateur. Aussi, le lien expirait automatiquement au bout d’une heure ce
qui limitait d’autant plus le risque. **Le lien de réinitialisation est
désormais automatiquement rendu invalide suite au changement du mot de passe ou
de l’email de l’utilisateur. De plus, l’utilisateur est également déconnecté de
ses autres appareils pour s’assurer qu’un attaquant ne conserve pas lui-même
une session ouverte.**

[Accéder au commit de correction](https://github.com/flusio/flusio/commit/06c7602ae8c8c31d3859edc291ca0c1503fa20ed)

Le second problème de sécurité concernait la possibilité pour un attaquant
d’intégrer Flus à un site externe via un mécanisme d’[`iframe`](https://developer.mozilla.org/fr/docs/Web/HTML/Element/iframe).
Cela pouvait permettre à l’attaquant de se faire passer pour Flus tout en
ajoutant du code malveillant par-dessus (i.e. attaque par [détournement de
clic](https://fr.wikipedia.org/wiki/D%C3%A9tournement_de_clic)). J’ai considéré
le risque comme étant plutôt faible. De plus, Flus étant un logiciel libre, il
est toujours possible d’en créer une copie conforme. **J’ai tout de même fait
en sorte d’interdire les intégrations par `iframe`.**

[Accéder au commit de correction](https://github.com/flusio/flusio/commit/25165cac4014a175fdfa575d178714327adadff6)

Ces deux problèmes présentant des risques faibles, j’ai décidé de repousser
leur correction à la fin de mes vacances et de ne pas publier d’article à part
entière sur le [carnet](https://flus.fr/carnet).

Je remercie Rishabh Pardeshi pour me les avoir remontés.
