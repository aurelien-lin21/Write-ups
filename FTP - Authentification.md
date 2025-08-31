# Root-Me Write-Up : FTP - Authentification

Récemment, j’ai résolu le challenge **FTP – Authentification** sur [Root-Me](https://www.root-me.org/fr/Challenges/Reseau/FTP-Authentification).  
Objectif : analyser une capture réseau pour extraire un mot de passe transmis via FTP.


## Étapes de la résolution

1. **Ouverture du fichier dans Wireshark**
   J’ai ouvert le fichier `.pcap` fourni dans Wireshark.

2. **Filtrage du protocole FTP**
   J’ai appliqué le filtre : ftp
