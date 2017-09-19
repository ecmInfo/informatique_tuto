+++
title = "Les raccourcis claviers dans Pycharm"
author = "François Brucker"

categories = [
    "pycharm",
]
tags = [
    "développement"
]

weight = 4
+++


## Introduction

De nombreuses actions disponibles via un menu dans [Pycharm](https://www.jetbrains.com/pycharm/) possèdent un raccourci clavier. 

Par exemple, sous unix :

  * Commenter une ligne ou un bloc: {{< menu_code >}}Ctrl + /{{< /menu_code >}} (Utiliser le {{< menu_code >}}/{{< /menu_code >}} du pavé numérique)
  * Rechercher {{< menu_code >}}Ctrl + F{{< /menu_code >}}
  * Exécuter le fichier actuel: {{< menu_code >}}Maj + F10{{< /menu_code >}}


Nous allons montrer dans ce tuto comment les connaître et comment les modifier au besoin.


## Trouver les raccourcis

L'utilisation des raccourcis clavier est décrite dans  l'aide en ligne de Pycharm sur les [keymap](https://www.jetbrains.com/help/pycharm/keymap.html).


### Connaître un raccourci clavier

Si une commande possède un raccourci clavier, il est montré à droite de son nom : 

![commande rename](/img/pycharm/keymap/raccourci_clavier.png)

L'image ci-dessus montre la commande {{< menu_code >}}Rename{{< /menu_code >}} et son raccourci clavier {{< menu_code >}}Maj + F6{{< /menu_code >}} (cette commande est très très utile et vous l'utiliserez souvent car elle permet de renommer n'importe quoi. Le nom est modifié dans tout le fichier et dans d'autres fichiers du même projet). 

Si vous ne savez pas ce qu'est la touche Maj : [lmgtfy](http://lmgtfy.com/?q=touche+maj+clavier)

### Connaître tous les raccourcis claviers

Selon la plateforme, les raccourcis par défaut changent :
 - ![Raccourcis par défaut unix](https://resources.jetbrains.com/storage/products/pycharm/docs/PyCharm_ReferenceCard.pdf)
 - ![Raccourcis par défaut mac](https://resources.jetbrains.com/storage/products/pycharm/docs/PyCharm_ReferenceCard_mac.pdf)
 
 
 Tous les raccourcis sont disponibles dans les préférences (menu {{< menu_code >}}File > Settings...{{< /menu_code >}}) dans la partie keymap : 
 
 ![raccourcis claviers](/img/pycharm/keymap/keymap_settings.jpg)

 
### Modifier un raccourci clavier

Le raccourci clavier pour commenter automatiquement une ligne ou une partie de texte sélectionné par défaut de Pycharm n'est pas fonctionnel avec un clavier Français. 

Le raccourci concerne les commentaires : *comment* en anglais. Pour trouver rapidement les raccourcis on tape donc *comment* dans la barre de recherche de la partie {{< menu_code >}}keymap{{< /menu_code >}} de la fenêtre des paramètres : 

 ![raccourcis comments](/img/pycharm/keymap/keymap_comment.jpg)


Il y a 2 types de commentaires : commentaire d'une ligne et d'un bloc de texte. Certains langages utilisent ces deux types de commentaires (le C++ ou le Java par exemple), mais pas python puisqu'il suffit de mettre un `#` devant la ligne à commenter. Nous n'aurons à modifier que le raccourci : {{< menu_code >}}Comment with Line Comment{{< /menu_code >}}.

Dans de nombreux éditeurs, ce raccourci est sur {{< menu_code >}}CTRL + /{{< /menu_code >}} (`//` est le commentaire de ligne de nombreux langages comme le javascript, Java, C++, ...). C'est ce que pense faire Pycharm, et ceci marche avec un clavier Américain. Le clavier Français a la touche `/` comme modificateur de la touche `:`, ce qui confuse python.


 Ajoutons donc le raccourci clavier qui consiste à taper simultanément sur {{< menu_code >}}ctrl{{< /menu_code >}}, {{< menu_code >}}Maj{{< /menu_code >}} et {{< menu_code >}}:{{< /menu_code >}}, c'est à dire la combinaison : {{< menu_code >}}Ctrl + Maj + :{{< /menu_code >}} (sur mac, vous pouvez remplacer {{< menu_code >}}ctrl{{< /menu_code >}} par {{< menu_code >}}cmd{{< /menu_code >}} qui correspond mieux à l'usage courant sur cette plateforme).
 
 Après avoir double cliqué sur la ligne {{< menu_code >}}Comment with Line Comment{{< /menu_code >}} et choisi d'ajouter un raccourci clavier, effectuez la combinaison de touche puis cliquez sur {{< menu_code >}}Ok{{< /menu_code >}} (appuyer sur {{< menu_code >}}Entrée{{< /menu_code >}} change le raccourci...) : 
 
 ![raccourcis comments](/img/pycharm/keymap/keymap_shortcut.jpg)
 
Le raccourci est alors ajouté :

![raccourcis comments](/img/pycharm/keymap/keymap_result.jpg)

Testez le !

