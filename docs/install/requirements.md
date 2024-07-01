## Server
!!! info "Information"

    Le serveur est le coeur du système SABU, il est utilisé pour plusieurs actions :

    - Gestion du système SABU via le panel d'administration
    - Liaison avec les endpoints
    - Scans des fichiers
    - Stockage des fichiers dans les espaces utilisateurs
    - Interface utilisateur cliente pour la gestion de ses fichiers et les scans depuis son ordinateur.

!!! warning "Attention"

    Le serveur étant utilisé pour les scans, allouer davantage de ressources à ce serveur permettra de gérer un plus grand nombre de scans simultanément, augmentant ainsi le nombre d'endpoints pris en charge.

    - Configuration minimale (pour tester le système) : **2 CPU / 4 Go de RAM.**  
    - Configuration recommandée : **4 CPU / 8 Go de RAM.**

### Installation de Debian
Le serveur SABU doit être installer dans un environnement Linux.  
Nous vous recommandons d'installer votre serveur sur la distribution **Debian** (Test réalisé sur Debian 12).
!!! tip "Lien"

    Téléchargement de Debian : [https://www.debian.org/download.fr.html](https://www.debian.org/download.fr.html)

### Configuration réseau
Pour le bon fonctionnement du système SABU, configurez votre serveur avec une adresse IP statique :
```
nano /etc/network/interfaces
```
Voici le modèle à respecter :
```
auto ens18
iface ens18 inet static
address X.X.X.X
netmask X.X.X.X
gateway X.X.X.X
```
!!! info "Information"

    Veuillez remplacer **ens18** par le nom de votre interface réseau.  
    Veuillez remplacer les **"X"** par votre configuration réseau.

### Ajouter un disque supplémentaire
Pour stocker les données des utilisateurs, ajoutez un disque supplémentaire dédié exclusivement à cet usage.

- 1) Ajouter le disque à votre serveur
- 2) Partitionner le disque :
```
fdisk /dev/sdb

key: n (new)
key: p (partition)
key: enter x3 (part number, first sector, last sector)

key: w (write)
```
- 3) Formatter le disque :
```
mkfs.ext4 /dev/sdb1
```
> **sdb1** : correspond à la partition de votre disque
- 4) Déclarer le disque dans le fichier fstab:
```
nano /etc/fstab
```
Ajouter cette ligne :
```
# SABU MOUNT DATA DISK
/dev/sdb1       /mnt/data   ext4    defaults        0       2
```
> **/mnt/data** : correspond au point de montage sur votre système


## Endpoint
!!! info "Information"

    Nos endpoints ont été testés sur des **Raspberry Pi 4** avec des **écrans tactiles**, vous pouvez utiliser un autre type d'équipement si vous le souhaitez.

!!! warning "Attention"

    Assurez-vous d'avoir votre équipement pleinement fonctionnel (exemple : écran tactile fonctionnel).  
    Lors de l'installation nous ne configurons pas automatiquement le matériel de ces équipements.

### Installation de Raspbian
Nos endpoints ont été testés et installés sur la distribution **Raspbian**.
!!! tip "Lien"

    Téléchargement de Raspbian : [https://www.raspberrypi.com/software/](https://www.raspberrypi.com/software/)

### Configuration réseau
Vérifiez que votre endpoint dispose d'une adresse IP et testez sa connectivité à Internet.
