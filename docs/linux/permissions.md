# Permissions

## Définition de permissions sur un fichier/dossier

=== "Syntaxe"

    ```bash
    chmod <permissions> <chemin du fichier/dossier>
    ```

=== "Exemple"

    ```bash
    chmod 666 /var/zizou
    ```

    Donne les permissions de lecture-écriture à tout les utilisateurs ``rw-rw-rw-``.

=== "Tableau de permissions"

    ```bash
    chmod OGE /var/zizou
    ```
    Ici, ``O`` correspond à l'owner du fichier. ``G`` correspond au groupe du fichier. ``E`` correspond à tout le monde.

    L'owner et le groupe sont définis via la commande ``chown`` (prochaine commande), ``chmod`` sert juste à définir les permissions.


    Ici, ``N`` est est égal à un numéro en décimal du tableau.

    |             |          | Lecture | Écriture | Exécution |
    |-------------|---------|---------|----------|-----------|
    |           7 |  ``0``  |  ``1``  |   ``1``  |   ``1``   |
    |           6 |  ``0``  |  ``1``  |   ``1``  |   ``0``   |
    |           5 |  ``0``  |  ``1``  |   ``0``  |   ``1``   |
    |           4 |  ``0``  |  ``1``  |   ``0``  |   ``0``   |
    |           0 |  ``0``  |  ``0``  |   ``0``  |   ``0``   |
    |             |         |         |          |           |
    | Format UNIX |         |  ``r``  |   ``w``  |   ``x``   |

    ```bash
    # (O) L'owner du fichier dispose du contrôle total   -> 7
    # (G) Les membres du groupent peuvent lire et écrire -> 5
    # (E) Les autres utilisateurs Linux peuvent lire     -> 4

    chmod 754 /var/zizou
    ```

## Définition de l'owner/groupe sur un fichier/dossier

=== "Syntaxe"

    ```bash
    chmod <utilisateur[:groupe]> <chemin du fichier/dossier>
    ```

=== "Exemple"

    ```bash
    chown root /var/zizou
    ```

    Donne la propriété de ``/var/zizou`` à l'utilisateur ``root``.

=== "Exemple 2"

    ```bash
    chown root:zizouclubfan /var/zizou
    ```

    Donne la propriété de ``/var/zizou`` à l'utilisateur ``root`` dans le groupe ``zizouclubfan``.
