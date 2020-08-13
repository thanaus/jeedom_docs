Gestion de l'écosystème Netatmo en un seul plugin afin d'en faciliter la configuration et avoir ainsi une vision globale de tous ses équipements.

# Description
Netatmo est une start-up francaise spécialisé dans les objets connectés. Ses différents produits, dans la maison connectée et dans le bien être, lui ont valu différents prix (CES awards).

Il existe actuellement 4 lignes de produits :

### Weather Station
C'est une station météo comportant au minimum un module intérieur et un module extérieur. Le module intérieur permet de récupérer les informations de température, humidité, pression, CO2 et bruit. 
Le module extérieur permet de récupérer les informations de température et d'humidité. 
3 types de modules supplémentaires peuvent être associés à cette station météo : un anémomètre, un pluviomètre ainsi que 'x' modules intérieur comparable au module extérieur.

### Healthy Home Coach
C'est un module permettant d'obtenir un indice de confort calculé en fonction de la température de la pièce, l'humidité, le CO2 ainsi que l'environnement sonore.

### Thermostat
C'est un thermostat permettant de régler son chauffage en fonction de ses habitudes de vie pour ne chauffer que lorsque c'est utile. Il peut prendre aussi en compte l'isolation de la maison et la température extérieure pour anticiper le démarrage du chauffage.

### Cameras
Il s'agit de deux caméras : une caméra intérieure (Welcome) et une caméra extérieure (Presence). 
La caméra intérieure est à reconnaissance faciale et permet de vous envoyer des notifications lorsque vos enfants ou parents sont rentrés. Cette caméra de sécurité vous prévient également quand elle détecte un inconnu. 
La caméra extérieure permet de distinguer les personnes, voitures et animaux. Elle vous alerte en temps réel si quelqu'un s'attarde près de chez vous, des véhicules empruntent votre allée ou des animaux se trouvent dans votre jardin...

# Configuration
Une fois le plugin installé, il vous faut renseigner vos informations de connections. Ces informations sont liées à votre compte Netatmo (Nom d'utilisateur, Mot de passe) et ceux fournis par Netatmo à l'activation de l'API (application).

### Activation de l'API

Pour activer l'API et ainsi récupérer les données de vos équipements, vous devez créer une application. Pour cette étape, il vous faut se connecter à l'adresse suivante :
[https://dev.netatmo.com](https://dev.netatmo.com)

Cliquez ensuite sur le menu '_CREATE YOUR APP_'. Il vous sera alors demandé de vous identifier (Email/Password). Ces informations sont liées à votre compte Netatmo que vous avez créé pour activer votre équipement.

Remplissez les champs '_Name_', '_Description_', '_Data Protection Officer name_' et '_Data Protection Officer email_'.
Il faut ensuite cocher la coche '_I accept Netatmo APIs Terms and Conditions_'
Le nom de l'application étant commun à tous les utilisateurs, il est possible qu'elle soit déjà  utilisée. Dans ce cas, le message suivant apparaitra '_Application name already used. Please choose another name._'.
Cliquez sur le bouton '_SAVE._'.

Il vous faut alors récupérer les informations '_Client id_' et '_Client secret_' de la section '_TECHNICAL PARAMETERS_'. Ces 2 champs correspondent aux champs de même nom dans la configuration du plugin.

### Configuration du plugin

La configuration du plugin est très simple et comporte 4 champs que sont le '_Client ID_', le '_Client secret_', le '_Nom d'utilisateur_' ainsi que le '_Mot de passe_'. Les deux premiers champs sont fournis par Netatmo lors de l'activation de l'API (voir section précédente) et les deux derniers champs sont ceux associés à votre compte Netatmo.
Une fois les champs renseignés dans le formulaire, il ne reste plus qu'à cliquer sur le bouton '_Sauvegarder_'.

### Synchronisation des équipements

La synchronisation des équipements est automatique en cliquant simplement sur l'icône '_Synchronisation_'.
Au bout de quelques secondes précédemment suivi du message '_Synchronisation en cours_' puis '_Synchronisation réalisé avec succès_', la page se rafraîchit et tous les équipements, quel que soit la ligne de produit, sont affichés.

La configuration de chaque équipement est standard au design de Jeedom avec un onglet '_Equipement_' correspondant aux informations spécifiques de l'équipement ainsi qu'un onglet '_Commandes_' pour afficher toutes les commandes associées à cet équipement.

# Weather Station

C'est une station météo comportant au minimum un module intérieur et un module extérieur. Le module intérieur permet de récupérer les informations de température, humidité, pression, CO2 et bruit.
Le module extérieur permet de récupérer les informations de température et d'humidité. 
3 types de modules supplémentaires peuvent être associés à cette station météo : un anémomètre, un pluviomètre ainsi que 'x' modules intérieur comparable au module extérieur.

### Module intérieur

Le module intérieur est le coeur de la station météo. Il se connecte sur une prise de courant et reçoit à intervalle régulier les données des capteurs. Ces données sont régulièrement envoyés sur le site Netatmo par l'intermédiaire de votre connexion Wifi.

La page de l'équipement permet d'afficher l'adresse MAC du module, le logiciel interne (firmware) ainsi que le signal Wifi. Voici un ordre d'échelle de la valeur du signal fourni par Netatmo :

|Wifi status | Signal quality |
| ---------- | -------------- |
|86          |Bad |
|71          |Average |
|56          |Good |

Les commandes disponibles sous Jeedom sont les suivantes :

* Température
* CO2
* Humidité
* Sonomètre
* Pression
* Température (minimum et maximum)
* Tendance (température et pression)

### Module extérieur

Le module extérieur se connecte par signal radio à la station. Il est alimenté par 2 piles 1.5V (L)R03.

La page de l'équipement permet d'afficher le numéro de série du module, le logiciel interne (firmware) ainsi que le signal radio et le pourcentage de la batterie. Voici un ordre d'échelle de la valeur du signal fourni par Netatmo :

|Radio status | Signal quality |
| ----------- | -------------- |
|90           | Low |
|60           | Highest |

Les commandes disponibles sous Jeedom sont les suivantes :

* Température
* Humidité
* Batterie
* Température (minimum et maximum)
* Tendance (température)

### Anémomètre

L'anémomètre se connecte par signal radio à la station. Il est alimenté par 2 piles 1.5V (L)R03.

La page de l'équipement permet d'afficher le numéro de série du module, le logiciel interne (firmware) ainsi que le signal radio et le pourcentage de la batterie. Voici un ordre d'échelle de la valeur du signal fourni par Netatmo :

|Radio status | Signal quality |
| ----------- | -------------- |
|90           | Low |
|60           | Highest |

Les commandes disponibles sous Jeedom sont les suivantes :

* Vent (vitesse et direction)
* Rafales (vitesse et direction)
* Batterie
* Maximum (vitesse et direction du vent)

### Pluviomètre

Le pluviomètre se connecte par signal radio à la station. Il est alimenté par 2 piles 1.5V (L)R03.

La page de l'équipement permet d'afficher le numéro de série du module, le logiciel interne (firmware) ainsi que le signal radio et le pourcentage de la batterie. Voici un ordre d'échelle de la valeur du signal fourni par Netatmo :

|Radio status | Signal quality |
| ----------- | -------------- |
|90           | Low |
|60           | Highest |

Les commandes disponibles sous Jeedom sont les suivantes :

* Pluviométrie
* Batterie
* Pluviométrie (cumul sur la dernière 1h/24h)

### Module additionnel

Le module additionnel se connecte par signal radio à la station. Il est alimenté par 2 piles 1.5V (L)R03.

La page de l'équipement permet d'afficher le numéro de série du module, le logiciel interne (firmware) ainsi que le signal radio et le pourcentage de la batterie. Voici un ordre d'échelle de la valeur du signal fourni par Netatmo :

|Radio status | Signal quality |
| ----------- | -------------- |
|90           | Low |
|60           | Highest |

Les commandes disponibles sous Jeedom sont les suivantes :

- Température
- Humidité
- CO2
- Batterie
- Température (minimum et maximum)
- Tendance (température)

# Healthy Home Coach

C'est un module permettant d'obtenir un indice de confort calculé en fonction de la température de la pièce, l'humidité, le CO2 ainsi que l'environnement sonore.

# Thermostat

C'est un thermostat permettant de régler son chauffage en fonction de ses habitudes de vie pour ne chauffer que lorsque c'est utile. Il peut prendre aussi en compte l'isolation de la maison et la température extérieure pour anticiper le démarrage du chauffage.

# Cameras

Il s'agit de deux caméras : une caméra intérieure (Welcome) et une caméra extérieure (Presence). 
La caméra intérieure est à reconnaissance faciale et permet de vous envoyer des notifications lorsque vos enfants ou parents sont rentré. Cette caméra de sécurité vous prévient également quand elle détecte un inconnu. 
La caméra extérieure permet de distinguer les personnes, voitures et animaux. Elle vous alerte en temps réel si quelqu'un s'attarde près de chez vous, des véhicules empruntent votre allée ou des animaux se trouvent dans votre jardin...

# FAQ
