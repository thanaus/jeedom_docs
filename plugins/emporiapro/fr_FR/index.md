---
layout: default
lang: fr_FR
title: Plugin Emporia Pro
description: Documentation du plugin Emporia Pro
---

Monitoring de consommation d'énergie en temps réel (Gen 2 Vue Energy Monitor)

# Présentation Emporia Pro

The Gen 2 Vue Energy Monitor est un moniteur de consommation d'énergie qui permet de surveiller la consommation électrique de votre maison en temps réel. Il mesure la consommation d'énergie en kilowattheures (kWh) et vous permet de voir la quantité d'énergie consommée par différents appareils électriques dans votre maison. Il dispose également d'une fonctionnalité de suivi de l'historique de la consommation d'énergie, vous permettant de voir l'évolution de votre consommation électrique au fil du temps.

Ce plugin permet d'interfacer ce moniteur de consommation d'énergie avec Jeedom.

# Installation et activation du plugin

Voici les étapes pour installer le plugin Emporia Pro :

1. Accédez à l'interface d'administration de votre Jeedom en ouvrant votre navigateur web.
2. Connectez-vous à votre compte Jeedom.
3. Cliquez sur "Plugins" dans le menu principal.
4. Cliquez sur "Gestion des plugins".
5. Cliquez sur "Market".
6. Recherchez le plugin Emporia Pro et cliquez dessus.
7. Cliquez sur "Installer stable/beta".

Voici les étapes pour activer le plugin Emporia Pro :

1. Cliquez sur "Plugins" dans le menu principal.
2. Cliquez sur "Gestion des plugins".
3. Recherchez le plugin Emporia Pro dans la liste des plugins installés.
4. Cliquez sur l'icône "Activer" dans la section "Etat".
5. Cliquez sur le bouton "Relancer" dans la section "Dépendances".
6. Les dépendances du plugin vont s'installer automatiquement. Ce processus peut prendre plusieurs minutes en fonction de la vitesse de votre connexion internet et de la puissance de votre Jeedom.
7. Une fois que l'installation des dépendances est terminée, vous pouvez configurer et utiliser le plugin normalement.

# Configuration du plugin

Voici les étapes pour configurer le plugin Emporia Pro :

1. Accédez à l'interface d'administration de votre Jeedom en ouvrant votre navigateur web.
2. Connectez-vous à votre compte Jeedom.
3. Cliquez sur "Plugins" dans le menu principal.
4. Cliquez sur "Gestion des plugins".
5. Recherchez le plugin Emporia Pro dans la liste des plugins installés.
6. Saisissez les informations de votre compte Emporia dans la section "Configuration". Vous aurez besoin de l'adresse email et le mot de passe.

# Configuration des équipements

Voici les étapes pour configurer les équipement :

1. Accédez à l'interface d'administration de votre Jeedom en ouvrant votre navigateur web.
2. Connectez-vous à votre compte Jeedom.
3. Cliquez sur "Plugins" dans le menu principal.
4. Cliquez sur "Energie" puis "Emporia Energy".

La page du plugin Emporia Pro dans Jeedom est divisée en deux sections principales :

- La section "Gestion"  
Cette section vous permet de configurer les paramètres de votre plugin Emporia Pro, notamment les informations d'identification de votre compte Emporia.

- La section "Mes équipements"  
Cette section répertorie tous les circuits de votre équipement Emporia.  
En cliquant sur un de vos équipements, vous arrivez sur la page de configuration de votre équipement comprenant 2 onglets.

>Dans le cas de l'équipement Emporia, ajout automatique de deux équipements :
> - le circuit électrique principal de la maison ou du bâtiment pour mesurer la consommation totale d'énergie.
> - la balance qui mesure la différence entre l'énergie électrique entrant dans le circuit principal et l'énergie électrique consommée par les circuits secondaires.

## Onglet Equipement

### Paramètres généraux

- Nom de l'équipement : c'est le nom que vous avez donné à l'équipement lors de sa création dans l'application officielle Emporia. Vous pouvez le modifier à tout moment en cliquant sur le champ de texte correspondant.
- Objet parent : il s'agit de l'objet parent auquel l'équipement est rattaché dans votre organisation d'objets. Vous pouvez modifier l'objet parent en sélectionnant un nouvel objet dans la liste déroulante.
- Catégorie : c'est la catégorie à laquelle l'équipement est rattaché dans votre organisation de catégories. Vous pouvez modifier la catégorie en sélectionnant une nouvelle catégorie.
- Options : cette section contient diverses options de configuration pour l'équipement, telles que la possibilité de désactiver temporairement l'équipement, de rendre visible le widget sur le dashboard

### Informations

- Modèle : il s'agit du modèle de l'équipement, tel que spécifié par le fabricant.
- Numéro de série : c'est un numéro unique qui identifie l'équipement.
- Firmware : il s'agit de la version du logiciel embarqué dans l'équipement. Le firmware peut être mis à jour par l'application officielle Emporira pour corriger des bugs ou ajouter des fonctionnalités.
- Numéro du circuit : il s'agit du numéro du circuit de l'équipement.
- Description : il s'agit d'un champ permettant à l'utilisateur de saisir une description personnalisée afin de faciliter l'identification et la compréhension de sa fonction ou de son utilisation.

## Onglet Commandes

Voici la liste des commandes disponibles pour un équipement Emporia Pro dans Jeedom :

- Consommation électrique (minute) : il s'agit de la consommation électrique consommée par le circuit en une minute.  
L'unité de mesure est le Watts.
- Consommation électrique (heure) : **TBD**
- Consommation électrique (jour) : **TBD**
- Consommation électrique (semaine) : **TBD**
- Consommation électrique (mois) : **TBD**
- Consommation électrique (année) : **TBD**

Voici la liste des informations disponibles pour chaque commande :

- ID : il s'agit de l'identifiant unique de la commande. Cet ID est généré automatiquement par Jeedom lors de la création de la commande.
- Nom : c'est le nom de la commande défini lors de sa création. Ce nom peut être modifié à tout moment en cliquant sur le champ de texte correspondant.
- Type : c'est le type de commande. Par exemple, une commande peut être de type "Action", "Info", "Curseur", "Liste", etc. Le type de commande détermine les options de configuration disponibles pour cette commande.
- Options : cette colonne affiche les options de configuration pour la commande, qui peuvent varier en fonction du type de commande.
- État : cette colonne affiche l'état actuel de la commande. Pour les commandes de type "Info", l'état peut être un texte ou une valeur numérique. Pour les commandes de type "Action", l'état indique si la commande a été exécutée avec succès ou non.
- Actions : cette colonne peut afficher des boutons pour exécuter des actions supplémentaires sur la commande, telles que la configuration avancée ou la suppression de la commande.
