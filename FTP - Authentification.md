## FTP – Authentication

## Contexte
- **Enseigne** : Network  
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
  
