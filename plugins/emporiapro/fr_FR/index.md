---
layout: default
lang: fr_FR
title: Plugin Emporia Pro
description: Documentation du plugin Emporia Pro
---

Ce plugin permet de récupérer la consommation d'eau (compteur communicant) depuis le site "Veolia & moi - Eau"

Configuration du plugin 
=======================

Après installation du plugin, il vous suffit de l’activer. Il faut ensuite rentrer les informations de votre compte Veolia.

-   **Adresse email** : Indiquez l'adresse email de votre compte Veolia
-   **Mot de passe** : Indiquez le mot de passe de votre compte Veolia

Configuration des équipements 
=============================

La configuration des équipements Veolia est accessible à partir du menu plugins puis Energie. Vous retrouvez ici :

-   un bouton pour la synchronisation de vos équipements depuis votre compte Veolia

-   un bouton pour afficher la configuration du plugin

-   la liste de vos équipements Veolia

Equipement
==========

En cliquant sur un de vos équipements, vous arrivez sur la page de configuration de votre équipement comprenant 2 onglets: Equipement et
Commandes.

Onglet Equipement
-----------------

-   **Paramètres généraux / Nom de l’équipement** : nom de votre équipement

-   **Paramètres généraux / Objet parent** : indique l’objet parent auquel appartient l’équipement

-   **Paramètres généraux / Catégorie** : catégorie (couleur) de l'équipement sur le dashboard

-   **Paramètres généraux / Options / Activer** : permet de rendre votre équipement actif

-   **Paramètres généraux / Options / Visible** : le rend visible sur le dashboard

-   **Paramètres spécifiques** : (none)

-   **Informations / Description** : permet d'écrire une description sur l'équipement

Onglet Commandes
----------------

Il existe 3 commandes que vous pouvez renommer, afficher ou non sur le dashboard et les réorganiser.

-   **Consommation du jour** : consommation du jour (litres)

-   **Consommation facturée** : volume facturée (m<sup>3</sup>)

-   **Index** : consommation cumulée (litres)


Astuces & FAQ
=============

**-> Quelle est la fréquence de synchronisation des données ?**

>Lors de l'activation du plugin, une cron spécifique au plugin est ajoutée au moteur de tâches de Jeedom. La synchronisation des données s'effectue une fois par jour et correspond à l'heure d'activation du plugin modulo 5 minutes.
