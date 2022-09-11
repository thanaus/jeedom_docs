---
layout: default
lang: fr_FR
title: Plugin homepTalk - Changelog
description: Changelog du plugin homepTalk
---

Changelog
=========

En Beta (à venir)
--------
* Plus de compilation de openssl 1.0 dans les dependances (la lib est compatible 1.1 !) -> install des dépendances bcp plus courtes et bcp plus fiables !!!

15-02-2021
----------
* Fix TTs jeedom avec 4.2 (possible que jeedom 3 ne soit plus compatible du coup... je ne le supporte plus de toute façon)

15-10-2021
----------
* Fix images 4.2

18-01-2021
----------
* Ajout des voix dans voiceRSS

11-01-2021
----------
* Discover pour le Yamaha WX-021
* Nouvelle liste des pièces imbriquées

21-12-2020
----------
* Discover pour les Sonos Play:1 Play:3 Play:5

17-11-2020
----------
* Détection et logo Homepod Mini

14-06-2020
-------------
* FFMPEG est installé par le core, suppression de l'install de celui-ci dans les dépendances
* tag v4 das info.json

14-06-2020
-------------
* Fix double install

26-05-2020
-------------
* Compatibilité avec le plugin jeedom Jailbreak pour générer la voix sur un iPhone/iPad jailbreaké
* Installation des dépendances plus claires

06-02-2020
-------------
* Support Airplay2 Tiers : Ajout de détection Sonos One et Yamaha RX-A880 et IKEA Symfonisk
* Gestion du port d'airplay (nécessaire pour players tiers)
* Forcer la communication sur l'IPv4
* ajout avahi-browse oublié dans les dep

19-11-2019
-------------

* Fix ffmpeg à la place de avconv

14-11-2019
-------------

* Version Initiale
