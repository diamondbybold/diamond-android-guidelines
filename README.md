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

**Convenção de nomenclatura geral**

Tabela - Nomenclatura de drawables

| Tipo de Asset      | Prefixo       | Exemplo                  |
| :----------------- | ------------- | ------------------------ |
| Action bar/Toolbar | ab_/tb_       | ab_stacked.9.png         |
| Button             | btn_          | btn_send_pressed.9.png   |
| Dialog             | dialog_       | dialog_top.9.png         |
| Divider            | divider_      | divider_horizontal.9.png |
| Icon               | ic_           | ic_star.png              |
| Menu               | menu_         | menu_submenu_bg.9.png    |
| Notification       | notification_ | notification_bg.9.png    |
| Tabs               | tab_          | tab_pressed.9.png        |

**Convenção de nomenclatura de icons**

Tabela - Nomenclatura de Icons

| Tipo de Asset            | Prefixo         | Exemplo                  |
| :----------------------- | --------------- | ------------------------ |
| Icons                    | ic_             | ic_star.png              |
| Icons do Launcher        | ic_launcher_    | ic_launcher_calendar.png |
| Icons de menu ou Toolbar | ic_menu_        | ic_menu_archive.png      |
| Icon barra de Status     | ic_stat_notify_ | ic_stat_notify_msg.png   |
| Icons de Tabs            | ic_tab_         | ic_tab_recent.png        |
| Icons de Dialogs         | ic_dialog_      | ic_dialog_info.png       |

**Convenção de nomenclatura de selectors**

Tabela - Nomenclatura de selectors

| Estado   | Sufixo    | Exemplo                  |
| :------- | --------- | ------------------------ |
| Normal   | _normal   | btn_order_normal.9.png   |
| Pressed  | _pressed  | btn_order_pressed.9.png  |
| Focused  | _focused  | btn_order_focused.9.png  |
| Disabled | _disabled | btn_order_disabled.9.png |
| Selected | _selected | btn_order_selected.9.png |

### Layouts

Os nomes dos ficheiros de layouts devem corresponder ao nome dos componentes Android que pretendem representar, mas movendo o componente mais alto para o principio. Por exemplo, se estivermos a criar um Layout para a actividade SignInActivity, o nome do ficheiro de layout deve ser activity_sign_in.xml.

Um caso ligeiramente diferente é quando criamos um layout para ser injectado num Adapter, por exemplo para popular uma RecyclerView. Neste caso o nome do layout deve iniciar com item_.

Note-se ainda que há casos em que as regras acima não se aplicam. Por exemplo, quando criamos layouts que tem o intuito de ser incluídos noutros layouts. Neste caso usa-se o prefixo partial_.

Tabela - Nomenclatura de Layouts

| Componente       | Classe               | Exemplo                    |
| :--------------- | -------------------- | -------------------------- |
| Activity         | UserProfileActivity  | activity_user_profile.xml  |
| Fragment         | SignUpFragment       | fragment_sign_up.xml       |
| Dialog           | ChangePasswordDialog | dialog_change_password.xml |
| AdapterView item | \---                 | item_person.xml            |
| Layout parcial   | \---                 | partial_stats_bar.xml      |