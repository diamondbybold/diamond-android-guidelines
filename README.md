# diamond-android-guidelines
General guidelines for android projects





# Estrutura



## Estrutura do projecto

Os novos projectos devem seguir a estrutura dos projectos gradle em Android tal como definido no guia do utilizador para novas builds do Android (mais informações em <https://developer.android.com/studio/build/index.html>). Ao se criar um projecto via Android Studio esta estrutura já vem definida pelo projecto kickoff.

## Estrutura dos packages

Os projectos em Android devem seguir as seguintes regras nos nomes de packages:

O package principal deve ser \[site do cliente invertido\].\[nomedoprojecto\] e de seguida deve se seguir a seguinte estrutura:

-   app

-   data

    -   common

    -   repositories

-   di

-   network

    -   adapter

    -   models

        -   request

        -   response

-   ui

    -   \[feature\]

    -   widgets

-   utils

## Nomenclatura de ficheiros

### Classes

Tal como no Java normal as classes nos projectos Android devem seguir a norma UpperCamelCase (<http://en.wikipedia.org/wiki/CamelCase>).

No caso das classes que estendem componentes do Android, o nome da class deve terminam com o nome desse componente. Por exemplo: SignInActivity, SignInFragment, ImageUploaderService, ChangePasswordDialog.

### Recursos

Os nomes dos ficheiros de recursos devem se escrever em minúsculas e com underscore: exemplo: lowercase\_underscore.

### Drawables

No caso dos drawables existem três convenções a seguir: