---
layout: default
title: Documentation Roborock Pro
lang: fr_FR
pluginId: roborockpro
---

# Description

Plugin permettant de piloter vos aspirateurs et laveurs de sols **Roborock** via votre
compte cloud Roborock.

Il permet la détection et l'ajout automatique des robots associés à votre compte, la
remontée de leur état (batterie, statut, progression du nettoyage, erreurs
éventuelles) ainsi que leur pilotage : démarrage, mise en pause, arrêt, retour à la
base, choix du mode de nettoyage, de la puissance d'aspiration et du niveau d'eau.

Le plugin permet également de suivre l'usure des principaux consommables du robot
(brosses, filtre, capteurs...).

Les commandes disponibles dépendent du modèle et de la génération de votre robot : voir
la section [Utilisation et commandes](#utilisation-et-commandes) pour le détail par
famille de modèles.

La connexion à votre compte se fait de façon sécurisée par e-mail et code de
confirmation : aucun mot de passe n'est demandé ni stocké par le plugin.

# Robots testés

Le plugin est conçu pour fonctionner avec l'ensemble des robots Roborock connectés au
cloud, mais les modèles suivants ont été officiellement testés :

| Robot                 | Nom interne (modèle)     |
|------------------------|--------------------------|
| Roborock Qrevo Master  | `roborock.vacuum.a117`  |
| Roborock Qrevo Curv    | `roborock.vacuum.a135`  |
| Roborock Qrevo Pro     | `roborock.vacuum.a101`  |
| Roborock S8            | `roborock.vacuum.a51`  |
| Roborock S8 Pro Ultra  | `roborock.vacuum.a70`  |
| Roborock Saros 20      | `roborock.vacuum.a288`  |
| Roborock S7 MaxV       | `roborock.vacuum.a27`  |
| Roborock Qrevo Edge 3 Pro | `roborock.vacuum.a296`  |
| Roborock Q10 X5+       | `roborock.vacuum.ss09`  |

> **Remarque**
>
> Le Roborock Qrevo Edge 3 Pro et le Saros 20 Neo sont en réalité le même robot,
> commercialisé sous deux noms différents selon les marchés (source :
> [vacuumwars.com](https://vacuumwars.com/roborocks-ifa-2026-lineup/)).

# Versions supportées

| Composant | Version                                              |
|-----------|-------------------------------------------------------|
| Jeedom    | >= 4.4.19                                             |
| Systèmes  | Smart, Luna, Atlas, Raspberry Pi, Docker, DIY          |

# Installation

Afin d'utiliser le plugin, vous devez le télécharger, l'installer et l'activer comme
tout plugin Jeedom depuis le Market.

Lors de l'activation, les dépendances nécessaires au fonctionnement du plugin sont
installées automatiquement ; cette étape peut prendre jusqu'à une minute.

# Configuration du plugin

Depuis la page de configuration du plugin, renseignez l'**adresse e-mail** de votre
compte Roborock, puis enregistrez.

Vous pouvez également modifier le port utilisé par le démon du plugin, mais il n'est
recommandé de le faire qu'en cas de conflit avec un autre service.

Une fois l'e-mail renseigné, démarrez le démon du plugin.

# Connexion et synchronisation des robots

Depuis la page d'accueil du plugin, cliquez sur le bouton **Synchroniser**.

Roborock vous envoie alors par e-mail un code de confirmation. Une fenêtre s'affiche
dans Jeedom vous invitant à saisir ce code. Une fois le code validé, les robots
associés à votre compte sont automatiquement détectés et créés en tant qu'équipements
dans Jeedom.

> **Astuce**
>
> Les connexions suivantes se font automatiquement, sans qu'il soit nécessaire de
> ressaisir un code de confirmation.

# Utilisation et commandes

Les commandes créées pour un robot dépendent de sa famille de modèle : certaines
informations et actions sont communes à tous les robots, d'autres ne sont disponibles
que sur les modèles qui les supportent réellement.

## Commun à tous les robots

- État de connexion du robot (en ligne/hors ligne)
- État courant (en charge, en nettoyage, en pause, arrêté...)
- Erreur éventuelle en cours
- Niveau de batterie
- Démarrer
- Arrêter
- Retour à la base

## Robots de génération classique (protocole V1)

C'est la famille la plus répandue (aspirateurs et laveurs Roborock connectés en
Wi-Fi/cloud classique). En plus des commandes communes :

> **Remarque**
>
> Un modèle V1 pas encore explicitement reconnu par le plugin ne dispose, en
> attendant, que des commandes communes à tous les robots.

**Informations**

- Progression du nettoyage en cours
- Suivi des consommables : brosse principale, brosse latérale, filtre, capteurs

**Actions**

- Mettre en pause
- Localiser (le robot émet un son)
- Exécuter une routine enregistrée sur le compte Roborock

**Sélections** (valeurs proposées automatiquement selon les capacités réelles du robot)

- Mode de nettoyage
- Puissance d'aspiration
- Quantité d'eau (pour les modèles avec fonction lavage)
- Nettoyage d'une pièce spécifique (liste des pièces provenant automatiquement de la
  carte enregistrée sur votre compte Roborock)

Sur les modèles disposant d'un dock (charge simple ou station complète, par ex.
Roborock S8), des informations supplémentaires sont remontées :

- État du dock, erreur du dock

Sur les modèles dont le dock est une station complète avec auto-vidage et/ou lavage
automatique (par ex. Roborock Qrevo Curv), des informations supplémentaires encore sont
remontées :

- État du réservoir d'eau sale, état du réservoir d'eau propre
- État du sac à poussière du dock
- Suivi du bac de nettoyage (consommable additionnel)

## Robots Q10 (protocole B01, ex. Roborock Q10 X5+)

Ces robots utilisent un protocole de communication différent des modèles classiques ;
seul un socle de fonctionnalités de base est actuellement supporté. En plus des
commandes communes :

**Informations**

- Progression du nettoyage en cours
- Suivi des consommables : brosse principale, brosse latérale, filtre, capteurs

**Actions**

- Mettre en pause
- Reprendre (action distincte du démarrage, propre à ce protocole)

**Sélections** (valeurs fixes propres à ce modèle)

- Mode de nettoyage
- Puissance d'aspiration
- Quantité d'eau

Non disponibles pour l'instant sur cette famille : nettoyage d'une pièce spécifique,
localisation, exécution de routines, informations détaillées du dock (état/erreur du
dock, réservoirs d'eau).

## Autres robots B01 (Q7 et suivants)

La détection de ces modèles est en place, mais leur pilotage n'est pas encore
implémenté : toute commande envoyée à ce type de robot échoue avec un message
explicite indiquant que la série n'est pas encore supportée.

# Fréquence de mise à jour

Le plugin combine les notifications en temps réel envoyées par le robot avec des
rafraîchissements périodiques automatiques, afin de garantir que les informations
affichées restent fiables et à jour :

- un rafraîchissement rapide (toutes les 10 secondes) pendant un nettoyage en cours,
- un rafraîchissement général (toutes les 30 secondes) le reste du temps,
- une reconnexion complète au canal d'information du robot (MQTT) toutes les heures,
  pour assurer la stabilité de la remontée des données sur la durée.

# Dépannage

Si une commande envoyée à un robot échoue (par exemple si celui-ci est occupé ou hors
ligne), une alerte s'affiche dans Jeedom en indiquant le robot concerné.

# Changelog

[Voir le changelog](./changelog)

# Support

Si vous avez un problème, commencez par lire les derniers sujets en rapport avec le
plugin sur [community]({{site.forum}}/tag/plugin-{{page.pluginId}}).

Si malgré tout vous ne trouvez pas de réponse à votre question, n'hésitez pas à créer
un nouveau sujet en n'oubliant pas de mettre le tag du plugin
([plugin-{{page.pluginId}}]({{site.forum}}/tag/plugin-{{page.pluginId}})).

Il faudra au minimum fournir :

- une capture d'écran de la page santé Jeedom
- une capture d'écran de la page de configuration du plugin
- les logs disponibles du plugin, en niveau *INFO*, collés dans un `Texte préformaté`
  (bouton `</>` sur community), pas de fichiers !
- selon les cas, une capture d'écran de l'erreur rencontrée
