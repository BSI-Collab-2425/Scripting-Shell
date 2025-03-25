# README - Script d'installation

## Description
Ce script automatise l'installation d'un service Nginx pour le partage de dossiers, avec une configuration sécurisée garantissant la protection des données sur un système Linux. Il utilise whiptail pour fournir une interface utilisateur interactive et intuitive.

## Fonctionnalités du script
- Un utilisateur dédié pour le partage de dossier ou fichier 
- Communication en https
- Log actif sur le nginx
- Pare-feu UFW
- Un cloisonnement du dossier de partage
- Nginx configuré en lecture
- Version nginx masquée
- Page d'erreur personnalisé

## Prérequis
- Linux (Debian, Ubuntu, ou toute distribution basée sur Debian)

### Installation du script :
```bash
sudo cp nginx-install-script.deb /var/cache/apt/archives/
sudo chown _apt /var/cache/apt/archives/nginx-install-script.deb
sudo apt install -y /var/cache/apt/archives/nginx-install-script.deb
```

## Utilisation
### Exécution du script :
```bash
sudo nginx-install-script
```

### Options disponibles :
1. **Installer Nginx** : Lance l'installation de Nginx
2. **Configurer Nginx** : Configure Nginx, crée un utilisateur dédié à Nginx et crée des règles de filtrage
3. **Partager un dossier ou fichier** : Permet de sélectionner un fichier ou un dossier pour le partage.
4. **Supprimer la configuration** : Supprime la configuration de nginx
5. **Désinstaller Nginx** : Désinstallation Nginx

## Exemple de sélection de fichier
Lors de la sélection de l'option 3, une boîte de dialogue s'affiche demandant à l'utilisateur s'il souhaite sélectionner un fichier ou dossier. Ensuite l'utilisateur sélectionne le chemin du fichier. Si le fichier fait partie de la liste des fichiers interdits, un message d'erreur apparaîtra.

## Gestion des erreurs
- Si l'utilisateur annule une opération, le script affiche "Annulé." Et se termine.
- Si aucun fichier ou chemin valide n'est fourni, une alerte est affichée.

## Documentation  
Une page de manuel est disponible pour plus d’informations sur l’utilisation du script :  
```bash
man nginx-install-script
```

## Auteur
**Manqui1 et Fl1pp3r**

## Licence
Ce projet est sous licence **MIT**.

