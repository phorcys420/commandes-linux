# Montage de volumes

``/dev/sdX`` est un disque logique ou virtuel.

``X`` signifie la lettre correspondant à l'ordre d'apparition (ex: ``/dev/sda`` est le premier disque, ``/dev/sdb`` le deuxième, etc).

``/dev/sdX1`` est la partition n°1 du disque ``/dev/sdX``

## Lister les appareils (disques) disponibles

=== "Commande"

    ```bash
    lsblk
    ```

=== "Commande n°2"

    ```bash
    blkid
    ```

## Monter une partition

=== "Syntaxe"

    ```bash
    mount <partition> <chemin du dossier>
    ```

=== "Exemple"

    ```bash
    mount /dev/sdb1 /mnt
    ```

    `/mnt` est un dossier vide présent à la racine d'un système Linux prévu à cet effet.

## Formater une partition déja existante

=== "Syntaxe"

    ```bash
    mkfs.<système de fichiers> <partition>
    ```

=== "Exemple"

    ```bash
    mkfs.vfat /dev/sdc1
    ```

=== "Paquets à installer"

    | Système de fichiers        | Paquet Debian                         | Préinstallé? |
    |----------------------------|---------------------------------------|--------------|
    | ``ext2``/``ext3``/``ext4`` | ``e2fsprogs``                         | Oui          |
    | ``hfs``/``hfsplus``        | ``hfsprogs``                          | Non          |
    | ``fat``/``vfat``           | ``dosfstools``                        | Non          |
    | ``exfat``                  | ``exfat-utils`` **OU** ``exfatprogs`` | Non          |
    | ``ntfs``                   | ``ntfs-3g``                           | Non          |
