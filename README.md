# README - Script d'Installation

## Description
Ce script automatise l'installation d'un service Nginx pour le partage de dossiers, avec une configuration sécurisée garantissant la protection des données sur un système Linux. Il utilise whiptail pour fournir une interface utilisateur interactive et intuitive.

## Fonctionnalités du script
- Un utilisateur dédié pour le partage de dossier ou fichier 
- Communication en https
- Log actif sur le nginx
- Pare feu UFW
- Un cloisonnement du dossier de partage
- Nginx configuré en lecture
- Version nginx masquée
- Page d'erreur personnalisé

## Prérequis
- Linux (Debian, Ubuntu, ou toute distribution basée sur Debian)

### Installation du script :
```bash
sudo apt update
```

## Utilisation
### Exécution du script :
```bash
./script.sh
```

### Options disponibles :
1. **Install** : Lance l'installation des logiciels nécessaires.
2. **Partager un dossier ou fichier** : Permet de sélectionner un fichier ou un dossier pour le partage.

## Exemple de sélection de fichier
Lors de la sélection de l'option 2, une boîte de dialogue s'affiche demandant le chemin du fichier. L'utilisateur doit entrer le chemin absolu du fichier.

## Gestion des erreurs
- Si l'utilisateur annule une opération, le script affiche "Annulé." et se termine.
- Si aucun fichier ou chemin valide n'est fourni, une alerte est affichée.


## Auteur
**Manqui1 et flippeur**

## Licence
Ce projet est sous licence **MIT**.

