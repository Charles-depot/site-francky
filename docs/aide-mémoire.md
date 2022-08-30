# Aide-mémoire simplifié Markdown pour MkDocs

Pour un rappel, voir [les bases de Markdown](https://ens-fr.gitlab.io/mkdocs/markdown-bases/)

Pour plus de possibilités, voir [Markdown pour MkDocs](https://ens-fr.gitlab.io/mkdocs/markdown-mkdocs/)

## Une image sauvegardée en local

!!! note "Markdown"
    ```markdown
    ![Un chaton](images/Chaton.JPG){width=300}

    [Source](https://commons.wikimedia.org/wiki/File:Chaton.JPG), licence _Creative Commons_
    ```

![Un chaton](images/Chaton.JPG){width=300}

[Source](https://commons.wikimedia.org/wiki/File:Chaton.JPG), licence _Creative Commons_


## Les admonitions

!!! info "Pourquoi ?"
    Elles permettent de délimiter des blocs de contenu
      avec une touche de couleur, sans créer de nouvelles
      entrées dans la table des matières.
    
    Elles structurent donc sans alourdir les onglets de navigation.

!!! note "Markdown"
    ```markdown
    !!! info "Pourquoi ?"
        Elles permettent de délimiter des blocs de contenu
            avec une touche de couleur, sans créer de nouvelles
            entrées dans la table des matières.
        
        Elles structurent donc sans alourdir les onglets de navigation.
    ```

!!! faq "Comment l'avoir enroulée, à dérouler ?"
    En remplaçant `!!!` par `???`.

    `???+` permet de l'avoir déroulée à l'ouverture de la page, et qu'elle
    puisse être ensuite enroulée.

### Les types de boites

=== "`note`"
    !!! note "Pour une note"
        `note` ou `seealso`
        ````markdown
        ```markdown
        !!! note "Pour une note"
            `note` ou `seealso`
        ```
        ````

=== "`tldr`"
    !!! tldr "Pour un résumé"
        `tldr`, `summary` ou `abstract`
        ````markdown
        ```markdown
        !!! tldr "Pour un résumé"
            `tldr`, `summary` ou `abstract`
        ```
        ````

=== "`info`"
    !!! info "Pour une information"
        `info` ou `todo`
        ````markdown
        ```markdown
        !!! info "Pour une information"
            `info` ou `todo`
        ```
        ````

=== "`tip`"
    !!! tip "Pour une astuce"
        `tip`, `hint` ou `important`
        ````markdown
        ```markdown
        !!! tip "Pour une astuce"
            `tip`, `hint` ou `important`
        ```
        ````

=== "`done`"
    !!! done "Pour une réussite"
        `done`, `check` ou `success`
        ````markdown
        ```markdown
        !!! done "Pour une réussite"
            `done`, `check` ou `success`
        ```
        ````

=== "`faq`"
    !!! faq "Pour une question"
        `faq`, `help` ou `question`
        ````markdown
        ```markdown
        !!! faq "Pour une question"
            `faq`, `help` ou `question`
        ```
        ````

=== "`warning`"
    !!! warning "Pour une difficulté"
        `warning`, `caution` ou `attention`
        ````markdown
        ```markdown
        !!! warning "Pour une difficulté"
            `warning`, `caution` ou `attention`
        ```
        ````

=== "`fail`"
    !!! fail "Pour un échec"
        `fail`, `failure` ou `missing`
        ````markdown
        ```markdown
        !!! fail "Pour un échec"
            `fail`, `failure` ou `missing`
        ```
        ````

=== "`danger`"
    !!! danger "Pour un danger"
        `danger` ou `error`
        ````markdown
        ```markdown
        !!! danger "Pour un danger"
            `danger` ou `error`
        ```
        ````

=== "`bug`"
    !!! bug "Pour un bogue"
        `bug`
        ````markdown
        ```markdown
        !!! bug "Pour un bogue"
            `bug`
        ```
        ````

=== "`example`"
    !!! example "Pour des exemples"
        `example`
        ````markdown
        ```markdown
        !!! example "Pour des exemples"
            `example`
        ```
        ````

=== "`cite`"
    !!! cite "Pour une citation"
        `cite`
        ````markdown
        ```markdown
        !!! cite "Pour une citation"
            `cite`
        ```
        ````

## Les boutons

Un lien cliquable peut être transformé en bouton en lui adjoignant un élément de CSS `{ .md-button }`

=== "Rectangle creux"
    !!! note "Markdown"
        ```markdown
        [Une console Basthon](https://console.basthon.fr/){ .md-button }
        ```
    !!! done "Rendu"
        [Une console Basthon](https://console.basthon.fr/){ .md-button }

=== "Rectangle plein"
    !!! note "Markdown"
        ```markdown
        [Une console Basthon](https://console.basthon.fr/){ .md-button .md-button--primary }
        ```
    !!! done "Rendu"
        [Une console Basthon](https://console.basthon.fr/){ .md-button .md-button--primary }

## Affichage des touches

!!! note "Markdown"

    ```markdown
    ++ctrl+alt+del++
    ```

!!! done "Rendu"
    ++ctrl+alt+del++

## Intégration de fichiers externes

Pour donner le contenu du fichier `mkdocs.yml` qui est situé dans `docs/`, on a entre :

````markdown
```yaml
--8<---​ "mkdocs.yml"
```
````

Pour un script `docs/scripts/exemple.py`

!!! note "Markdown"
    ````markdown
    ```python
    --8<--- "docs/scripts/exemple.py" <⚠ sans rien, ni espace à la fin>
    ```
    ````

!!! done "Rendu"
    ```python
    --8<--- "docs/scripts/exemple.py"
    ```

## Les panneaux coulissant (*SuperFences*)

!!! note "Entrée"

    ````markdown

    === "C"

        ```c
        #include <stdio.h>

        int main(void) {
            printf("Hello world!\n");
            return 0;
        }
        ```

    === "C++"

        ```cpp
        #include <iostream>

        int main(void) {
            std::cout << "Hello world!" << std::endl;
            return 0;
        }
        ```

    ````

!!! done "Rendu"

    === "C"

        ```c
        #include <stdio.h>

        int main(void) {
            printf("Hello world!\n");
            return 0;
        }
        ```

    === "C++"

        ```cpp
        #include <iostream>

        int main(void) {
            std::cout << "Hello world!" << std::endl;
            return 0;
        }
        ```

