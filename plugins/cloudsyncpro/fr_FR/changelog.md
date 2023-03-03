Stable
=========================

2023-03-03 19:20:37
-------------------

* Mise à jour du framework Rclone (version 1.57.0)
* Mise à jour du stockage Dropbox (authentification OAuth 2)
* Mise à jour du stockage Google Drive (authentification OAuth 2)
* Intégration du stockage Microsoft OneDrive
* Intégration du stockage pCloud
* Suppression de l'appel à une fonction obsolète (core Jeedom)  
`https://x.x.x.x/core/php/getResource.php?file=plugins/cloudsyncpro/desktop/js/cloudsyncpro.js&md5=7b33d6301ea5304b040541f419f48b21&lang=fr_FR 
Ligne 25
ReferenceError: initCheckBox is not defined`
* Suppression du caractère initial '/' du champ destination des commandes associés à un équipement de type Dropbox  
`error listing: Error in call to API function "files/list_folder": Path root is not supported for sandbox app.`  

2020-04-06 03:14:16
-------------------

* Mise à jour du fichier info.json suite à un bug du core Jeedom (remplacement du tag #language# par fr_FR)  
[https://community.jeedom.com/t/description-plugin-info-json/22513](https://community.jeedom.com/t/description-plugin-info-json/22513)
* Evolution cosmétique (largeur du champ 'Commentaire')
* Ajout du tag V4 dans la définition du plugin (info.json)

2020-02-18 03:14:15
-------------------

* Mise à jour du Market (Jeedom)

2020-01-21 19:44:13
-------------------

* Support de PHP 7.3
* Création du répertoire config si non présent lors de la sauvegarde de l'équipement  
`Unable to write configuration file /var/www/html/plugins/cloudsyncpro/core/config/rclone.conf`
* Compatibilité Jeedom V4

2019-09-24 18:04:27
-------------------

* Version initiale

Beta
=========================


