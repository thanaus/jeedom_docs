Stable
=========================

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

2020-06-05 11:41:24
-------------------

* Mise à jour des équipements pour les notifications Netatmo (webhook) :
  - NACamera-tag_small_move  
  - NACamera-tag_big_move  

2020-06-01 14:55:14
-------------------

* Optimisation de la mise à jour des équipements pour les notifications Netatmo (webhook) :  
  - NACamera-person  
  - NACamera-tag_open  
  - NACamera-tag_close
  - NOC-on  
  - NOC-off

2020-05-29 21:16:42
-------------------

* Association incorrecte évènement/équipement pour les notifications Netatmo (webhook) :  
  - NACamera-tag_small_move  
  - NACamera-tag_big_move  
  - NACamera-tag_open  
  - NACamera-tag_close

2020-05-21 17:02:50
-------------------

* Optimisation sur le traitement des évènements lors des notifications Netatmo (webhook)
* Mise à jour des équipements pour les notifications Netatmo (webhook) :  
  - NACamera-person  
  - NACamera-tag_small_move  
  - NACamera-tag_big_move  
  - NACamera-tag_open  
  - NACamera-tag_close

2020-05-19 22:17:41
-------------------

* Ajout de 4 commandes sur le relai (NAPlug) :  
  - 'Mode de fonctionnement (En cours)' / Type INFO  
  - 'Mode de fonctionnement' / Type ACTION-LISTE  
  - 'Jeu de température' / Type INFO  
  - 'Plage horaire' / Type INFO  
* Widget par défaut (Jeedom) pour les équipements :  
  - Détecteur de Fumée Intelligent (NSD)  
  - Sirène Intérieure Intelligente (NIS)  
  - Détecteurs d’Ouverture Intelligents pour Portes et Fenêtres (NACamDoorTag)

2020-05-16 08:53:30
-------------------

* Intégration de la Sirène Intérieure Intelligente (NIS)
* Intégration des Détecteurs d’Ouverture Intelligents pour Portes et Fenêtres (NACamDoorTag)

2020-05-06 01:04:48
-------------------

* Intégration du Détecteur de Fumée Intelligent (NSD)

2020-04-28 22:34:36
-------------------
* Compatibilité des widgets V3/V4 (Weather Station) 
