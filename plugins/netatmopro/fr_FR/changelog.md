Stable
=========================

2020-06-06 17:32:06
-------------------

* Intégration du Détecteur de Fumée Intelligent (NSD)
* Intégration de la Sirène Intérieure Intelligente (NIS)
* Intégration des Détecteurs d’Ouverture Intelligents pour Portes et Fenêtres (NACamDoorTag)
* Compatibilité des widgets V3/V4 (Weather Station) 
* Ajout de 4 commandes sur le relai (NAPlug) :  
  - 'Mode de fonctionnement (En cours)' / Type INFO  
  - 'Mode de fonctionnement' / Type ACTION-LISTE  
  - 'Jeu de température' / Type INFO  
  - 'Plage horaire' / Type INFO  
* Widget par défaut (Jeedom) pour les équipements :  
  - Détecteur de Fumée Intelligent (NSD)  
  - Sirène Intérieure Intelligente (NIS)  
  - Détecteurs d’Ouverture Intelligents pour Portes et Fenêtres (NACamDoorTag)
* Optimisation sur le traitement des évènements lors des notifications Netatmo (webhook)
* Mise à jour des équipements pour les notifications Netatmo (webhook) :  
  - NACamera-person  
  - NACamera-tag_open  
  - NACamera-tag_close
  - NACamera-tag_small_move  
  - NACamera-tag_big_move    
  - NOC-on  
  - NOC-off

2020-04-24 14:56:58
-------------------

* Compatibilité Jeedom V4 (core)
* Mise à jour du widget au design V4 Jeedom :  
  - Weather Station / Module intérieur (NAMain)  
  - Weather Station / Module extérieur (NAModule1)  
  - Weather Station / Anémomètre (NAModule2)  
  - Weather Station / Pluviomètre (NAModule3)  
  - Weather Station / Module additionel (NAModule4)
* Ajout du tag V4 dans la définition du plugin (info.json)
* Mise à jour du fichier info.json suite à un bug du core Jeedom (remplacement du tag #language# par fr_FR)  
[https://community.jeedom.com/t/description-plugin-info-json/22513](https://community.jeedom.com/t/description-plugin-info-json/22513)
* Optimisation du code CSS (Weather Station / Module intérieur (NAMain))
* Image manquante (wind2kts.svg) sur le dashboard (widget anémomètre)  
`Console: Failed to load resource: the server responded with a status of 404 (Not Found)`
* Incohérence sur le type de batterie (Weather Station / Anémomètre (NAModule2))

Beta
=========================

2020-09-21 16:46:49
-------------------

* Mise à jour de la commande 'Projecteur (Statut)' pour la notification Netatmo (webhook) :
  - NOC-light_mode

2020-06-11 10:58:32
-------------------

* Mise à jour du répertoire 3rdParty Netatmo  
[https://github.com/Netatmo/Netatmo-API-PHP](https://github.com/Netatmo/Netatmo-API-PHP)

2020-06-07 11:25:01
-------------------

* Refresh automatique des widgets personnalisés sur le dashboard :
  - Weather Station / Module intérieur (NAMain)  
  - Weather Station / Module extérieur (NAModule1)  
  - Weather Station / Anémomètre (NAModule2)  
  - Weather Station / Pluviomètre (NAModule3)  
  - Weather Station / Module additionel (NAModule4)
  - Aircare / Capteur (NHC)
