Synchronisation fichiers vers des services de stockage en ligne (Dropbox, Google Cloud Storage, Nextcloud) mais aussi système de fichier local, serveurs (S)FTP

Présentation Cloudsyncpro
=========================
Dans le domaine de la synchronisation de fichiers, il existe un outil multiplateforme et largement utilisé : rsync.
On trouve aussi nombre d'outils qui se reposent sur rsync pour la gestion de la synchronisation, qui n'est qu'une de leurs multiples fonctionnalités.
C'est notamment le cas de Rclone, qui est un dérivé créé par Nick Craig-Wood. Open source, son code est disponible sous licence MIT et diffusé via GitHub. Sa fonctionnalité principale est d'accéder à des services de stockage en ligne mais il faut par contre être un adepte de la ligne de commande.

Ce plugin permet d'interfacer cet outil avec Jeedom et simplifier la configuration des services de stockage en ligne.

Installation et activation du plugin
====================================

Le plugin Cloudsyncpro doit être installé via le market Jeedom.

![cloudsyncpro](../images/c79bc8a975d6c3d2d6b358fecf424364.png) ![cloudsyncpro](../images/0756e6d2ebb078ad6d6218eb7f877ab8.png)

Une fois le plugin installé, il suffit de l’activer en cliquant sur "Activer".

![cloudsyncpro](../images/e49685947a96b7b166fb675155eac787.png)

Installation des dépendances
----------------------------

Les dépendances sont installées automatiquement par Jeedom dans les 5 min. Elles seront également réinstallées lors d'une mise à jour du plugin si besoin.

![cloudsyncpro](../images/ab08acd6c64a40354c8d3ddc80421ab2.png)

Mise à jour manuelle des dépendances
------------------------------------

Pour mettre à jour manuellement les dépendances, il faut cliquer sur "Relancer".

![cloudsyncpro](../images/df83599d06ecebbea359557b5efb4dde.png)

Configuration des équipements
=============================

Onglet Equipement
-----------------

-   **Nom de l’équipement** : Nom de votre service de stockage

-   **Objet parent** : Indique l’objet parent auquel appartient l’équipement

-   **Activer** : Permet de rendre votre équipement actif

-   **Visible** : Rend votre équipement visible sur le dashboard

-   **Commentaire** : Champ de texte libre

-   **Type de stockage** : Type de votre service de stockage

![cloudsyncpro](../images/1b27a7acbb02749f2dc1777ab5ca1686.png)

Onglet Commandes
----------------

Services de stockage
====================

FTP
---

File Transfer Protocol (protocole de transfert de fichier), ou FTP, est un protocole de communication destiné au partage de fichiers sur un réseau TCP/IP.

SFTP
----

SSH File Transfer Protocol (protocole de transfert de fichier), ou SFTP, est un protocole de communication fonctionnant au-dessus de SSH pour transférer et gérer des fichiers à distance.

Dropbox
-------

Dropbox est un service de stockage et de partage de copies de fichiers locaux en ligne proposé par Dropbox, Inc., entreprise localisée à San Francisco, en Californie.

Google Drive
------------

Google Drive ou Google Disque au Québec, est un service de stockage et de partage de fichiers dans le cloud lancé par la société Google.

Nextcloud
---------

Nextcloud est un logiciel libre, de site d'hébergement de fichiers, et un fork du logiciel ownCloud. À l'origine accessible via WebDAV, n'importe quel navigateur web, ou des clients spécialisés, son architecture ouverte a permis de voir ses fonctionnalités s'étendre depuis ses origines.

FAQ
===
