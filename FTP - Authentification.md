## FTP – Authentication

## Contexte
- **Catégorie** : Network  
- **Challenge** : FTP – Authentication  
- **Objectif** : Analyser un fichier de capture `.pcap` afin de retrouver les identifiants FTP (`USER` et `PASS`).  
- **Compétence démontrée** : Analyse de trafic réseau avec Wireshark, utilisation de filtres, extraction d’identifiants en clair.

---

### Étapes de la résolution

## Étape 1 : Récupération du fichier
- Télécharger le fichier `ch1.pcap` depuis l’interface du challenge Root-Me.  
- Ouvrir le fichier directement dans **Wireshark**.

## Étape 2 : Filtrer le trafic FTP
- Dans la barre de filtre de Wireshark, entrer : `ftp`.
- Ce filtre permet d’afficher uniquement les paquets liés au protocole FTP.
  
## Étape 3 : Suivre le flux TCP
- Sélectionner un paquet FTP (par exemple une commande `USER` ou `PASS`).  
- Clic droit → **Follow → TCP Stream**.  
- La fenêtre du flux complet apparaît, contenant les échanges FTP en clair.

## Étape 4 : Extraction des identifiants
Dans le flux, on retrouve les informations suivantes :
  - **Nom d’utilisateur** : `cdts3500`  
  - **Mot de passe (flag)** : `cdts3500`  
