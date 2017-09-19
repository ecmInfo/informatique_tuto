+++
title = "Utiliser un terminal unix (les bases)"
author = "Geoffroy Desvernay, Olivier Philippe, Olivier Pagé, François Brucker"

categories = [
    "ecm",
    "unix",
]
tags = [
    "terminal",
    "environnement",
]

weight = 2
+++



{{% toc %}}

## Introduction


Ce tuto, conçu comme un petit cours, va vous montrer les bases de l'utilisation d'un terminal et des commandes unix. 


## Environnement unix à l'ecm

Lorsque vous vous connectez sur un ordinateur, vous pouvez choisir votre environnement graphique (en haut à droite). Choisissez celui par défaut. Ce n'est pas l'environnement graphique le plus joli, mais il ne consomme pas beaucoup de ressources et ses fonctionnalités suffisent.

Nous aurons principalement besoin de 3 outils disponibles dans la barre des tâches :
  * un gestionnaire de fichiers
  * un terminal
  * un navigateur web

### Gestionnaire de fichier

Cliquez sur le gros écran en haut à gauche de votre écran ou dans le menu {{< menu_code >}}Application > Accessoires > Fichiers {{< /menu_code >}}


C'est fait pour ressembler à ce que vous connaissez sous Windows. Attention cependant, il y a parfois des farces et parfois on n'arrive pas à faire ce que l'on veut. Bref, c'est bien mais ça pourrait être mieux. 


### Un terminal

Un [terminal](https://fr.wikipedia.org/wiki/Shell_Unix) est une fenêtre permettant d'exécuter des commandes. Nous allons l'utiliser ici pour exécuter des commandes unix.  Sur la barre des tâches en haut à gauche de l'écran :

  1. Cliquez sur {{< menu_code >}}Applications{{< /menu_code >}} 
  2. Suivez le sous-menu {{< menu_code >}}Outils systèmes{{< /menu_code >}} 
  3. Cliquez sur {{< menu_code >}}Terminal MATE{{< /menu_code >}}  (les autres terminaux vont aussi) 

Le terminal permet d'interagir de façon plus fine et plus poussée que l'explorateur de fichier et la barre des tâches. Il est commun à tout le monde unix (unix, linux, mac, ...). On pourra souvent utiliser la [complétion automatique](https://ensiwiki.ensimag.fr/index.php?title=Trucs_et_astuces_Unix#Compl.C3.A9tion_automatique_avec_TAB) lorsque l'on tape des commandes, cela permet d'aller bien plus vite.


### Navigateur web

Dans {{< menu_code >}}Applications > Internet {{< /menu_code >}} : Firefox ou Chrome (qui s'appelle ici Chromium).


## Ressources internet

  - le [cours de Laurent Tichits](http://www.dil.univ-mrs.fr/%7Etichit/unix/index.html)  de Laurent Tichit, en particulier son [aide mémoire](http://www.dil.univ-mrs.fr/%7Etichit/unix/AideMemoire.pdf)
  - le [cours de l'ISIMA](http://fc.isima.fr/~loic/unixc.php). Une bonne introduction aux commandes en général.
  - le site [des tuteurs à l'ENS](http://www.tuteurs.ens.fr/unix/) plein de resources. Didactique.

## Fichiers

Dans le monde unix, tout est fichier, des commandes à vos rapports en pdf en passant par les hauts parleurs de votre ordinateur (`/dev/audio`).

Comme unix est multi-utilisateur, chaque fichier ou dossier (qui est un fichier particulier) que vous possédez a des droits d'utilisations. Cet [article](http://www.tuteurs.ens.fr/unix/droits.html) expose en détails leur gestion.

### Les droits


Il existe trois catégories de droits :

  - ceux liés à l'utilisateur (''**u**ser''),
  - ceux liés à son (ou ses) groupes (''**g**roup''),
  - ceux des autres utilisateurs (''**o**ther'').

Et trois possibilités :

  - lire (''**r**ead'') son contenu,
  - écrire (''**w**rite'') ou effacer,
  - exécuter (''e**x**ecute''). Si le fichier est un programme on peut l'exécuter et si c'est un dossier on peut y accéder.

On peut connaitre les droits d'un dossier ou d'un fichier en :

  * accédant à la partie {{< menu_code >}}Propriétés... > Permissions{{< /menu_code >}} en cliquant droit sur un élément du gestionnaire de fichiers
  * en utilisant l'argument '-l' de la commande 'ls'.


#### Quels sont vos droits ?

  - En utilisant un gestionnaire de fichiers, regardez les permissions de votre dossier `html` par exemple, ou bien du fichier `index.html` placé dans le dossier `html` de votre voisin (les dossiers de toute la promo se trouvent dans le dossier père de votre dossier principal)
  - Testez les commandes `whoami` et `groups` dans un terminal. A quoi servent-elles ?

#### Changeons les droits ! 

Créez un dossier que vous nommerez `dropbox`, choisissez une image de l'internet et sauvegardez-la dans le repertoire créé. 

  - **Je te vois**. Par défaut, votre voisin peut cliquer sur l'image pour la voir. Testez le.
  - **Je ne te vois plus**. Modifiez les droits pour que seul vous puissiez voir l'image.

#### Ligne de commande 

La page d'Ubuntu sur la [ligne de commande](https://doc.ubuntu-fr.org/tutoriel/console_ligne_de_commande) vous donne les deux instructions unix permettant de :

  - lire les fichiers d'un dossier : [ls](https://doc.ubuntu-fr.org/tutoriel/console_ligne_de_commande#ls)
  - vous déplacer de dossier en dossier : [cd](https://doc.ubuntu-fr.org/tutoriel/console_ligne_de_commande#cd)

Utilisez cette documentation pour voir les droits (argument `-l`) des fichiers de votre dossier principal (dont le raccourci est `~`. Pour vous déplacer dans votre dossier principal, tapez juste la commande `cd` puis Entrée.)

Vous êtes maintenant parés à refaire ce que vous avez fait précédemment en utilisant uniquement le terminal et les commandes `ls` et `cd` (si si, c'est possible).

### Fichiers visibles de l'internet 


Vous pouvez mettre à disposition de l'internet des fichiers (attention à ce que vous faites...). Vous pouvez voir les fichiers que vous mettez à disposition là : http://monlogin.perso.centrale-marseille.fr/visible/

 Il faut bien sûr changer **monlogin** en **votre login**.

Le dossier visible de l'internet est dans le dossier : `html/visible`. Pour rendre un fichier non téléchargeable il faut modifier les droits pour **o**ther (le rendre non lisible).


>Attention, ce qui est visible de l'internet est visible du monde entier ! 


#### A faire

Testez cette fonctionnalité en mettant deux images dans votre visible, une visible de tout le monde, et une uniquement visible pour vous.

Tout marche-t-il correctement ?


### Compression et décompression de fichiers

Il est d'usage de transmettre les dossiers ou les fichiers volumineux en les compressant. Dans le monde unix, deux formats sont communément utilisés :

  - le format *zip* (permet de compresser tout un dossier)
  - le format *tar.gz* (on commence par utiliser l'utilitaire tar qui rassemble tout en un seul fichier, que l'on compresse ensuite)


#### A faire

  - En utilisant le gestionnaire de fichiers, compressez le répertoire `dropbox` de la partie précédente des deux façons (cliquez droit sur le dossier puis {{< menu_code >}}Créer une archive{{< /menu_code >}}). Placez ces deux fichiers sur votre visible.
  - Récupérez ces deux fichiers depuis le visible de votre voisin et décompressez les dans un dossier `temp` que vous aurez créé dans votre répertoire racine (votre maison).
  - Refaire tout ça en utilisant les lignes de commandes :
    - commandes `zip` (lisez le [manuel](https://doc.ubuntu-fr.org/man) de la commande en tapant `man zip` pour comprendre pourquoi il faut utiliser l'argument -r) et `unzip`
    - commandes `tar czvf` et `tar xzvf` (que signifient les arguments ?)

### Fichiers exécutables


#### Un exemple

Copiez-collez la ligne suivante dans un terminal. Puis appuyez sur la touche entrée.

```
echo 'echo coucou `whoami` !' > salut.sh
```


Vous venez de créer un fichier nommé  `salut.sh` dans le repertoire courant. Vérifiez-le (en utilisant la commande `ls`).

Ce fichier est un script qui peut être exécuté. 

  - Commencez par voir l'intérieur du fichier (vous pourrez par exemple utiliser la commande `cat salut.sh` dans un terminal, ou afficher le contenu du fichier en utilisant le gestionnaire de fichiers) 
  - Permettez à tout le monde de l'exécuter en changeant ses droits,
  - Exécutez le fichier en tapant la commande `./salut.sh` (qui va exécuter le fichier nommé `salut.sh` présent dans le répertoire courant `./`).
  - Méditez sur le résultat obtenu.

#### Les chemins d'accès

Dans le monde unix, rien n'est magique. Tout ce qui est tapé dans un émulateur de terminal est un fichier placé dans un dossier. La commande `cat` de tout à l'heure est un fichier par exemple. Pour savoir où est ce fichier, on pourra utiliser la commande `which`. 

Si vous tapez `which cat` puis la touche entrée, on vous indiquera où est placé la commande `cat`. 

> Question : Où est placée la commande `which` ? 

Seule une petite quantité de dossiers est scannée pour savoir s'il contient une commande. Ces dossiers sont visible dans la variable `PATH`. Tapez `echo $PATH`  pour connaître ces répertoires.

>Vous remarquerez que votre répertoire n'y apparaît pas. C'est pourquoi il a fallu taper `./salut.sh` pour exécuter le fichier `salut.sh` et pas juste `salut.sh`. 


#### A faire 

Trouvez où est placé le fichier `python3` et `pycharm.sh` que vous utiliserez en informatique.



Dans votre répertoire `dropbox`, exécutez le code suivant : 

```
echo 'print("Salut les 1A !")' > salut.py
```

Vous venez de créer un fichier `salut.py` qui sera exécutable par le programme (fichier) `python3`.


>Il existe des éditeurs pour terminal performant et plus ou moins user friendly comme `pico`, `nedit` ou encore  l'inusable `vim` (attention, lisez le manuel avant de vous en servir...)


Si vous êtes dans le répertoire `dropbox` la commande : 

```
python3 salut.py
```

Doit fonctionner. Que fait-elle ?

Placez-vous maintenant dans votre répertoire racine. Retapez la commande précédente. Il doit y avoir une erreur. Pourquoi ?



## Processus

Une introduction est disponible dans cet [article](http://www.tuteurs.ens.fr/unix/processus.html).


Nous allons créer, voir et et détruire un processus. Pour cela il va vous falloir deux fenêtres terminal.

  - Dans le premier terminal tapez `xeyes`
  - Dans le second tapez `top` qui montre l'usage de tous les processus.
  - Lorsque vous ne bougez pas la souris la fenêtre xeyes ne fait rien et elle disparait de l'écran `top`. En revanche lorsque vous bougez la souris les yeux bougent et utilise du temps cpu. Le processus xeyes doit apparaître dans la fenêtre top.

Chaque processus a un numéro appelé *PID* (c'est la première colonne du top). On peut détruire un processus en utilisant la commande `kill`. 

  - Trouvez le numéro *PID* du processus xeyes
  - Utilisez un troisième terminal pour taper la commande `kill numero`
 
   
## Connexions

Que l'on veuille se connecter à un autre ordinateur de la même salle de TP, sur un centre de calcul ou sur le serveur web de son site sur les chats, on utilise ssh :

{{< youtube lLyjnuWVqMk>}}

De manière générale, pour se connecter à une machine distante, il faut connaître :

  - son nom
  - le login avec lequel on veut se connecter

Par défaut, les machines des salles ne sont pas accessibles de l'extérieur de l'école (et si elles sont éteintes...). Pour les élèves, la machine ouverte depuis l'extérieur est `sas1.centrale-marseille.fr`.

Connaître sa machine :

  - la commande `hostname` vous donne son nom
  - la commande `dnsdomainname` vous donne son domaine
  - le nom complet est nom.domaine, mais à l'intérieur d'un domaine, on peut se connecter en utilisant uniquement son nom via la commande `ssh`.


### À faire

Connectez vous sur la machine de votre voisin : 
  - Trouvez son nom sur la machine puis utilisez la commande ''ssh'' pour vous y connecter : ''ssh nom_machine'' (il faudra être d'accord puis taper votre mot de passe)
  - Vérifiez que votre voisin est également connecté en utilisant la commande `users`.
  - Déconnectez-vous en tapant `exit` (ou appuyez sur les touches {{< menu_code >}}application > CTRL + D {{< /menu_code >}}).


Essayez maintenant de vous connecter à la machine `sas1.centrale-marseille.fr`. 

### Lancer des processus

Si vous vous connectez sur une machine de l'école, votre compte et vos fichiers doivent être présents de la même manière que si vous vous connectez normalement. Vous pouvez faire tout ce que vous feriez normalement en utilisant le **terminal**. 

Attention cependant, même si vous exécutez des processus en *background*, ils vont s'arrêter lorsque vous vous déconnectez (si vous ne voulez pas rester connecter, on utilisera des commandes comme `screen`, `nohup` ou `batch` dont l'usage dépasse le cadre de ce tutoriel).
 
> Si vous lancez des processus coûteux en temps de calcul, une règle de bonne conduite est d'utiliser la commande `nice` pour laisser de la place et du temps processeur aux autres personnes.


Connectez-vous sur la machine de votre voisin avec l'argument `-Y`. Cet argument vous permet de lancer des fenêtres sur votre propre écran. Testez le avec la commande `xeyes`.

Vous pouvez également ouvrir des fenêtres sur l'écran de votre voisin (avec sa permission) :
  - Connectez vous sur la machine de votre voisin sans utiliser l'argument -Y.
  - Dîtes que vous voulez afficher des choses sur son écran. Ceci se fait en modifiant la variable d'environnement d'affichage : `export DISPLAY=:0.0`.
  - Tapez `xeyes` et constatez que votre connexion n'est pas autorisée.
  - Votre voisin doit autoriser les connexions en tapant `xhost +`.
  - Retapez `xeyes`.
