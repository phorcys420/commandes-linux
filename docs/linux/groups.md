# Groupes

## Création de groupe

=== "Syntaxe"

    ```bash
    groupadd <nom du groupe>
    ```

=== "Exemple"

    ```bash
    groupadd zizouclubfan
    ```

## Supression de groupe

=== "Syntaxe"

    ```bash
    groupdel <nom du groupe>
    ```

=== "Exemple"

    ```bash
    groupdel zizouclubfan
    ```

## Ajout d'utilisateur à un groupe

=== "Exemple"

    ```bash
    usermod -aG zizouclubfan
    ```

=== "Arguments"

    | Argument | Signification |
    |----------|---------------|
    | ``a``    | Add           |
    | ``G``    | Group         |
