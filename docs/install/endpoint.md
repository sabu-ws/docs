!!! warning "Prérequis"

    Avant de commencer l'installation, assurez-vous d'avoir suivi les [prérequis](requirements.md#endpoint) et d'avoir effectué l'[ajout d'un endpoint]() sur le panel d'administation.  
    Vous devez être en utilisateur **root** pour pouvoir effectuer l'installation de SABU.

## Télécharger le script d'installation
Télécharger le script d'installation sur notre dépôt Github :
```
curl -sSL https://raw.githubusercontent.com/sabu-ws/endpoint/main/install.sh -o install.sh && chmod +x install.sh
```

## Lancer l'installation
Exécuter le script d'installation automatique et suivez les instructions :
```
./install.sh
```
??? abstract "Informations à renseigner lors de l'installation"

    - **Adresse IP** du serveur SABU
    - **Nom de l'endpoint** (tel que configuré dans le panel d'administration)
    - Le **token** (généré lors de l'ajout de l'endpoint sur le panel d'administration)

!!! success "Succès"

    Une fois l'installation terminée l'endpoint va redémarrer.

!!! info "Information"

    Après le redémarrage, l'endpoint doit se connecter automatiquement au serveur. (Vous pouvez vérifier le statut sur le panel d'administration)
