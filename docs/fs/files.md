# Opérations de fichier

## Fichiers

### Création de fichier

=== "Syntaxe"

    ```bash
    touch <fichier>
    ```

=== "Exemple"

    ```bash
    touch /var/zizou.txt
    ```

### Modification de fichier

=== "Syntaxe"

    ```bash
    nano <fichier>
    ```

=== "Exemple"

    ```bash
    nano /etc/passwd
    ```

---

## Dossiers

### Création de dossier

=== "Syntaxe"

    ```bash
    mkdir <chemin du dossier>
    ```

=== "Exemple"

    ```bash
    mkdir zizou
    ```

### Changement de dossier actuel

=== "Syntaxe"

    ```bash
    cd <nom du dossier>
    ```

=== "Exemple"

    ```bash
    cd /mnt
    ```

---

## Dossiers/fichiers

### Suppression de fichier/dossier

=== "Syntaxe"

    ```bash
    rm <paramètres> <chemin>
    ```

=== "Suppression de fichier"

    ```bash
    rm /var/zizou.txt
    ```

=== "Suppression de dossier"

    ```bash
    rm -rf /var/zizou
    ```

    | Argument | Signification | Comportement                                                                         |
    |----------|---------------|--------------------------------------------------------------------------------------|
    | ``r``    | Recursive     | Supprime aussi les sous-dossiers.                                                    |
    | ``f``    | Force         | Ne demande pas une confirmation de suppression pour chaque élément (fichier/dossier) |
