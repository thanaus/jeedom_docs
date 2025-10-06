Stable
=========================

2025-07-18 10:12:23
-------------------

* Correction d'un bug sur les commandes "A la maison" & "Ailleurs" (NAPerson) et "Niveau d\'alerte maximum" (NACamera)  
`execute:: ex:'Netatmo\\Exceptions\\NAApiErrorType - 400 - bad request'`
* Compatibilité Jeedom V4.5 (core)
* Optimisation des requêtes et suppression du third-party Netatmo pour la partie Energy (Etape 1)
* Modification de la sévérité du message en cas d'erreur lors de la synchronisation des équipements
* Ajout d'erreurs de connexion (API/Web Netatmo)
  - GuzzleHttp\Exception\ServerException - 500 - Server error: 'GET https://app.netatmo.net/api/[xxx]' resulted in a '500 Internal Server Error' response: [xxx]

2024-09-27 11:20:39
-------------------

* Correction d'un bug sur la mise à jour du jeton d'authentification
* Correction d'un bug sur la mise à jour des éléments de configuration (NAMain et NHC)

2024-06-05 11:18:59
-------------------

* Optimisation des requêtes et suppression du third-party Netatmo pour la partie Weather + Aircare
* Optimisation des requêtes et suppression du third-party Netatmo pour la partie Home + Security
* Intégration du Détecteur de Monoxyde de Carbone Intelligent (NCO)

2023-07-13 09:09:18
-------------------

* Intégration du nouveau système d'authentification Netatmo (OAuth 2.0 Authorization Framework)
* Correction d'un bug sur la portée des autorisations (OAuth 2.0 Authorization Framework)
* Incohérence sur le type de batterie (Weather Station / Module additionnel (NAModule4))

2022-08-09 08:49:27
-------------------

* Intégration de la Sonnette Vidéo Intelligente (NDB)
* Correction de la validité du cookie suite au changement du workflow d'authentification depuis les serveurs Netatmo
* Modification du payload suite à un changement du workflow d'authentification depuis les serveurs Netatmo :
  - Paramètres (personnes) [NOC]  
  - Paramètres (voitures) [NOC]  
  - Paramètres (animaux) [NOC]  
  - Paramètres (autres mouvements) [NOC]  
  - Visages inconnus [NACamera]  
  - Détection de mouvement (Enregistrement) [NACamera]  
  - Détection de mouvement (Notification) [NACamera]  
  - Détection alarme [NACamera]  
  - Smart Notifications (On/Off) [NACamera]  
  - Calibration [NRV]  
  - True Temperature [NARoom]  
  - Mode de fonctionnement [NAPlug]  

2022-05-14 10:50:42
-------------------

* Passage en version minimum Jeedom 4.0.63
* Compatibilité Jeedom V4.1 (core)
* Gestion de l'erreur 419 suite à un changement du workflow d'authentification depuis les serveurs Netatmo
* Modification du sous-type (string vers numeric) pour la commande "Dernière détection" (NAPerson)
* Gestion de l'erreur 409 lors de l'activation/désactivation de la caméra (Presence et Welcome)
  - GuzzleHttp\\Exception\\ClientException - 409 - Client error: GET https://[...]/command/changestatus?status=off resulted in a 409 Conflict response: {"error":{"code":35,"message":"Already off"}} 
  - GuzzleHttp\\Exception\\ClientException - 409 - Client error: GET https://[...]/command/changestatus?status=on resulted in a 409 Conflict response: {"error":{"code":7,"message":"Already on"}} 
* Ajout d'erreurs de connexion (API/Web Netatmo)
  - Netatmo\Exceptions\NACurlErrorType - 28 - Operation timed out after [xxx] milliseconds with 0 out of 0 bytes received
  - GuzzleHttp\Exception\ConnectException - 0 - cURL error 7: Failed to connect to app.netatmo.net port 443: Connection timed out (see http://curl.haxx.se/libcurl/c/libcurl-errors.html)
  - GuzzleHttp\Exception\ConnectException - 0 - cURL error 35: OpenSSL SSL_connect: SSL_ERROR_SYSCALL in connection to app.netatmo.net:443 (see http://curl.haxx.se/libcurl/c/libcurl-errors.html)
* Correction d'un bug sur la gestion du webhook (suppression du fichier core/php/.htaccess)
* Suppression de 2 commandes obsolètes sur le Aircare / Capteur (NHC)
  - 'Température (tendance)' / Type INFO  
  - 'Pression (tendance)' / Type INFO

2021-01-11 16:09:46
-------------------

* Refonte de la gestion du cookie en cas d'erreur lors de la synchronisation par cron5() ou lors de l'éxécution d'une commande
* Vérification de l'intégrité de l'URL externe défini dans la configuration pour le webhook Netatmo
* Exclusion des stations météo en favoris
* Ajout d'une commande sur le détecteur d'ouveture intelligent (NACamDoorTag) :  
  - 'Batterie (Pourcentage)' / Type INFO
* Refonte de la gestion des erreurs de connexion (API/Web Netatmo)
  - Netatmo\Exceptions\NAApiErrorType - 13 - Application does not have the good scope rights
  - Netatmo\Exceptions\NAApiErrorType - 500 - Internal Server Error
  - Netatmo\Exceptions\NAApiErrorType - 502 - Bad Gateway
  - Netatmo\Exceptions\NAApiErrorType - 503 -
  - Netatmo\Exceptions\NAApiErrorType - 504 - Gateway Time-out
  - Netatmo\Exceptions\NACurlErrorType - 7 - Failed to connect to api.netatmo.com port 443: Connection refused
  - Netatmo\Exceptions\NACurlErrorType - 28 - Connection timed out after [xxx] milliseconds
  - Netatmo\Exceptions\NACurlErrorType - 28 - Resolving timed out after [xxx] milliseconds
  - Netatmo\Exceptions\NACurlErrorType - 28 - Operation timed out after [xxx] milliseconds with 0 bytes received
  - Netatmo\Exceptions\NACurlErrorType - 35 - OpenSSL SSL_connect: SSL_ERROR_SYSCALL in connection to api.netatmo.com:443
  - GuzzleHttp\\Exception\\ServerException - 500 - Server error: 'GET https://my.netatmo.com' resulted in a '500 Internal Server Error' response: [xxx]
  - GuzzleHttp\Exception\ConnectException - 0 - cURL error 7: Failed to connect to app.netatmo.net port 443: Connection refused (see http://curl.haxx.se/libcurl/c/libcurl-
  - GuzzleHttp\Exception\ClientException - 403 - Client error: `POST https://[xxx]` resulted in a `403 Forbidden` response: {"error":{"code":2,"message":"Invalid access token"}}
errors.html)
  - GuzzleHttp\Exception\TooManyRedirectsException - 0 - Will not follow more than 5 redirects

2020-11-14 17:11:42
-------------------

* Refresh automatique des widgets personnalisés sur le dashboard :
  - Weather Station / Module intérieur (NAMain)  
  - Weather Station / Module extérieur (NAModule1)  
  - Weather Station / Anémomètre (NAModule2)  
  - Weather Station / Pluviomètre (NAModule3)  
  - Weather Station / Module additionel (NAModule4)
  - Aircare / Capteur (NHC)
* Mise à jour de la commande 'Projecteur (Statut)' pour la notification Netatmo (webhook) :
  - NOC-light_mode
* Mise à jour du répertoire 3rdParty Netatmo  
[https://github.com/Netatmo/Netatmo-API-PHP](https://github.com/Netatmo/Netatmo-API-PHP)

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

2025-10-06 11:17:56
-------------------

* Correction d'un bug sur les commandes "Mode de chauffage" (NAPlug)
`execute:: ex:'Netatmo\\Exceptions\\NAApiErrorType - 400 - bad request'`

2025-09-08 14:11:44
-------------------

* Changement du nom de domaine lié à l'API Netatmo  
`we will be retiring the domain api.netatmo.net and consolidating all API traffic under the existing domain api.netatmo.com`

2025-07-25 16:24:19
-------------------

* Correction d'un bug sur les commandes "Planning" (NAPlug) et "Manual Boost" (NARoom)  
`execute:: ex:'Netatmo\\Exceptions\\NAApiErrorType - 400 - bad request'`
* Ajout du widget pour la visualisation du stream de la Caméra Intérieure ADVANCE

2025-07-21 14:23:06
-------------------

* Intégration de la Caméra Intérieure ADVANCE (NPC)

