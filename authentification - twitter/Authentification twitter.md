# Authentification twitter

## Contexte

- **Catégorie** : Réseau  
- **Challenge** : Twitter Authentication  
- **Objectif** : Analyser un fichier `.pcap` afin de retrouver le mot de passe d'une session Twitter.  
- **Compétence démontrée** : Analyse de flux TCP avec Wireshark, décodage base64, récupération de credentials.

---

## Étapes de la résolution

### Étape 1 : Récupération du fichier

Le challenge fournit un fichier `.pcap` contenant une session Twitter. Une fois téléchargé, je l'ai ouvert directement dans **Wireshark**.

### Étape 2 : Suivi du flux TCP

En examinant la capture, on remarque qu’il n’y a **qu’un seul paquet**.  
J’ai utilisé **Follow → TCP Stream** sur ce paquet pour visualiser l’intégralité de la session.

![Capture suivi du flux TCP](twitter_tcp_stream.png)

### Étape 3 : Repérage de l’en-tête Authorization

Dans le flux TCP, on repère un en-tête `Authorization` : **Basic dXNlcnRlc3Q6cGFzc3dvcmQ=**
Cet en-tête utilise la technique **Basic Authorization**, et la chaîne semble encodée en base64.

### Étape 4 : Décodage du token en base64

J’ai copié la valeur encodée et l’ai décodée en utilisant un outil en ligne ou la commande suivante :

```bash
echo "dXNlcnRlc3Q6cGFzc3dvcmQ=" | base64 --decode
```

### Étape 5 : Extraction du mot de passe

Le mot de passe extrait est :
