# Arduino_Buttons
Boutons UPnP basée sur une carte Arduino

<strong>Description : </strong>

Ce composant gère les événements UPnP envoyés selon le bouton pressé. Nous avons ici une carte Arduino sur laquelle 
deux boutons poussoir sotn connecté. Lorsque celui de droite est pressé un événement UPnP est lancé avec pour valeur
la chaîne de carctère "DROITE" et "GAUCHE" pour le bouton gauche.

Voici le schéma d'assemblage des boutons sur la carte Arduino :

![alt tag](https://github.com/components-upnp/Arduino_Buttons/blob/master/cablage_Arduino_Buttons.png)

<strong>Lancement de l'application : </strong>

    i - Avoir nodeJs installé sur la machine
    ii - Télécharger et décompresser l'archive du projet dans un dossier
    iii - Lancer les commandes npm install johnny-five et npm install peer-upnp depuis un terminal dans le répertoire du projet
    iv - Cabler les composants physiques sur la carte Arduino (confère la schéma ci-dessous)
    v - Brancher la carte sur la machine (port COM3 par défaut, si branchée sur un autre port, le préciser dans index.js)
    vi - Depuis l'IDE Arduinon, lancer le sketch File > Examples > Firmata > StandardFirmata
    vii - Lancer l'application avec la commande node index.js
    
<strong>Spécifications UPnP : </strong>

Ce composant offre un service UPnP dont voici la description :

  ButtonsService :
  
    1) SetTarget(String NewTargetValue) : action UPnP qui prend en entrée une chaîne de caractère et la transmet par un événement
    UPnP du nom de "Status".
    
Voici un schéma représentant le composant :

![alt tag](https://github.com/components-upnp/Arduino_Buttons/blob/master/Arduino_Buttons.png)



