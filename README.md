# TP6 Mise en place d'une topologie

### Mise en place de la topologie

Nous avons mis en place grace à GNS3 une topologie qui ressemble enfin à quelque chose !

Tout d'abord, initialiser 2 clients 
Je me suis servi des clone de clients déjà prête grâce au TP5. (malinx le lynx)

Puis incorporer des routeur dans le logiciel Cisco pour qu'elle débouchent sur un serveur.

Nous avons une topologie qui ressemble à cela (mise en place comme dans l'exemple du sujet)

https://i.postimg.cc/50JJyJzq/Screenshot-3.png

Nous avons donc une route entre 2 clients différents non liés entre eux, qui vont communiquer directement avec un routeur et transmettre l'information de routeur en routeur jusqu'à un serveur connecté à internet et transmettre le tout jusqu'au clients.

### Pour que cela soit fonctionnel il faut donc mettre en place les IP (on suit les IP): 

On rentre dans l'interface ethernet et on modifie l'ip et son masque réseau.

Client 1 : 10.6.201.1
Client 2 : 10.6.201.11

Serveur 1 : 10.6.202.1

Ces ips ont été mises en place après avoir entré la commande conf t du terminal de GNS3(qui donne un droit maximal sur la configuration de la machine)

### Mise en place des routes (avec conf t encore une fois)

Ici il suffit de taper (dans cet ordre ci): 
ip route "adresse réseau" "masque" "passerelle"

Sur le terminal GNS3 en lien avec le routeur en question, exit le mode conf t et faire un show ip route pour vérifier que la route entrée est bonne.

___
Je ne les écris pas ici une par une mais j'ai bien rentré les mêmes routes que le tableau du TP
___

Puis pour terminé j'ai ping les machines :
- Client 1 à Client 2
- Serveur à Client 1
- Serveur à Client 2
- 
.
.
.
PS : Si jamais les TP peuvent rester sur ton github ce serait vraiment super histoire d'avoir un vrai exercice de ce type pour s'entrainer et pousser le travail plus loin à l'occasion.
