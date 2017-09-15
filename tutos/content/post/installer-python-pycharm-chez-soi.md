+++
title = "Installer python3 et Pycharm chez soi"
author = "François Brucker"

categories = [
    "python",
    "pycharm",
]
tags = [
    "environnement"
]

weight = 3
+++


## Introduction

Tuto vous montrant comment installer chez vous le duo [python3](https://www.python.org/) et [Pycharm](https://www.jetbrains.com/pycharm/).


## Python3

Pour chaque installation, notez où le programme python3 se trouve, Vous en aurez besoin pour le choix d'un interpréteur lors de la configuration de Pycharm.

### mac

Pour l'installation de nombreux logiciels utiles en informatique, plutôt que de les installer à la main, on peu utiliser : [brew](https://brew.sh) qui s'utilise en ligne de commande ({{< menu_code >}}Application > Utilitaires > Terminal{{< /menu_code >}}. Je vous conseille d'en faire un lien sur le doc, vous allez en avoir besoin si vous faite un peu d'informatique).

Une fois brew installé pour python3, la commande `brew install python3` dans un terminal vous insalle tout python. Le programme est dans `/usr/local/bin/python3`. 

{{< youtube p4gz9Y78ECs>}}
### windows 

L'installeur [scoop](http://scoop.sh) vous permet d'installer python sans douleur et tout un tas d'autres utilitaires (comme git, Java, etc) sous windows. 

{{< youtube oLEkF7ctXOU>}}

Par défaut les programmes sont installé dans le dossier `appdata/local` de votre dossier principal. Pour voir le dossier `appdata` dans un explorateur de fichier, il est nécessaire de cocher la case [show hidden files](http://www.windows10themes.net/guides/how-to-view-the-appdata-folder-in-windows-10/). Naviguez ensuite vers l'exécutable `python`.



Sinon, vous pouvez aussi utiliser le package  [winpython](http://winpython.github.io).

### linux

Souvent installé par défaut. Ce [tutoriel](https://www.digitalocean.com/community/tutorials/how-to-install-python-3-and-set-up-a-local-programming-environment-on-ubuntu-16-04) vous montre une méthode en utilisant le packageur par défaut de linux.


## Pycharm

Il existe deux versions de [Pycharm](https://www.jetbrains.com/pycharm/) : Community et Professionnal. La version Community, gratuite, convient parfaitement lorsque l'on veut développer de petites applications ou algorithmes ce qui est notre cas. Vous pouvez la télécharger en cliquant sur le bouton {{< menu_code >}}Download{{< /menu_code >}}. Vous serez redirigé vers les version de votre système : linux, mac ou Windows.

Une fois le logiciel installé, il faudra le [paramètrer]({{< relref "/post/utilisation-pycharm-bases.md#configuration" >}}). 

