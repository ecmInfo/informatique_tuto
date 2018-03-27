+++
title = "Utiliser Pycharm (les bases)"
author = "François Brucker"

categories = [
    "ecm",
    "python",
    "pycharm",
]
tags = [
    "installation",
    "developpement",
]

weight = 1
+++



{{% toc %}}

## Introduction


Ce tuto va vous montrer les différentes étapes pour configurer son [Pycharm](https://www.jetbrains.com/pycharm/) lorsqu'on l'utilise pour la première fois.

[Pycharm](https://www.jetbrains.com/pycharm/) est l'[IDE](https://fr.wikipedia.org/wiki/Environnement_de_développement) qui sera utilisé tout au long de l'UE d'informatique à l'[ECM](https://www.centrale-marseille.fr). C'est un éditeur professionnel, il faut donc un peu de temps pour maîtriser la bête, mais une fois cet apprentissage effectué, vous ne pourrez plus vous en passer.

Ce logiciel existe sous deux formes, la version professionnelle et la version communautaire. C'est cette dernière que nous utilisons (en tant qu'étudiant, vous pouvez utiliser la version professionnelle gratuitement mas elle n'est vraiment utile que si vous faites du développement poussé en python ou que vous faites du développement web en python).



## Exécuter le programme

On suppose que vous êtes installé devant un ordinateur d'une salle machine Linux et que vous vous êtes connecté en utilisant le gestionnaire de fenêtre par défaut (si vous n'avez touché à rien, ce devrait être le cas. On choisit son gestionnaire de fenêtre sur l'écran de connexion en haut à droite).

## via le menu

PyCharm se trouve dans le menu {{< menu_code >}}Applications > Programmation > Pycharm Community Edition{{< /menu_code >}}.


{{< note warning >}}
Si c'est votre première utilisation de Pycharm : **ON SE RETIENT D'APPUYER SUR OK SANS RIEN LIRE LORSQUE LA PREMIÈRE FENÊTRE APPARAIT** (je sais, c'est dur)
{{< /note >}}
### via le terminal

Un [terminal](https://fr.wikipedia.org/wiki/Shell_Unix) est une fenêtre permettant d'exécuter des commandes. Nous allons l'utiliser ici pour exécuter Pycharm.  Sur la barre des tâches en haut à gauche de l'écran :

  1. Cliquez sur {{< menu_code >}}Applications{{< /menu_code >}} 
  2. Suivez le sous-menu {{< menu_code >}}Outils systèmes{{< /menu_code >}} 
  3. Cliquez sur {{< menu_code >}}Terminal MATE{{< /menu_code >}}  (les autres terminaux vont aussi) 
      

Une fenêtre apparaît. Vous pouvez y taper des commandes.

   
  1. Ouvrez un terminal .
  2. Dans celui-ci, tapez `pycharm.sh` puis sur la touche Entrée (on pourra utiliser la [complétion automatique](https://ensiwiki.ensimag.fr/index.php?title=Trucs_et_astuces_Unix#Compl.C3.A9tion_automatique_avec_TAB) en ne tapant que `pyc` puis en appuyant sur la touche tabulation qui complètera automatiquement en `pycharm.sh`)
  

## Configuration  

Lors de la première utilisation de Pycharm, vous aurez à choisir si vous [importez des préférences]({{< relref "#import-des-préférences-précédentes" >}}) et à configurer l'[apparence de votre éditeur]({{< relref "#apparence-de-pycharm" >}}). 

Toutes ces configurations pourront être modifiées plus tard dans l'onglet {{< menu_code >}}File > Settings...{{< /menu_code >}} du menu de PyCharm.

### Import des préférences précédentes

Si c'est la première fois que vous utilisez Pycharm où qu'une nouvelle version est disponible, la fenêtre suivante apparaît :

![importation des préférences](/img/pycharm/prefs/import_old_settings.jpg#center)


Si vous avez utilisé PyCharm précédemment, il vous proposera par défaut d'importer les préférences de l'ancienne version. Choisissez de ne rien importer puis cliquer sur {{< menu_code >}}Ok{{< /menu_code >}}.

### Apparence de Pycharm

Une nouvelle fenêtre (sauvage) apparaît qui vous permettra de configurer l'apparence de votre navigateur. J'aime bien le thème *Darcula*, c'est donc ce que j'ai choisi :

![importation des préférences](/img/pycharm/prefs/prefs.jpg#center)

Puis on peut cliquer sur {{< menu_code >}}Ok{{< /menu_code >}}. 

### Choix d'un projet

Si c'est la première fois que vous utilisez PyCharm, vous n'avez pas encore de projet actif (*ie.* le dernier projet utilisé) et c'est la fenêtre de choix du projet qui apparaît : 

![choix d'un projet](/img/pycharm/fenetre_demarrage_normal.jpg)

Vos projets sont (s'il y en a) listés à gauche de cette fenêtre (là, il n'y en a pas).

Cliquez sur {{< menu_code >}}Create new project{{< /menu_code >}}. 


## Démarrer un nouveau projet


Pour créer un nouveau projet, vous cliquez sur {{< menu_code >}}File > New Project...{{< /menu_code >}} dans un projet existant. La fenêtre suivante vou permet alors de créer un projet : 

![choix d'un projet](/img/pycharm/create_project.jpg)

 - **Location** : renseignez le nom et l'emplacement du projet
 - **Interpreter** : quelle version de python vous voulez utiliser pour ce projet.


### Nom et emplacement du projet

Essayez d'avoir un peu d'ordre dans vos projets :

 - un dossier principal où tous vos projets seront placés : ici  {{< menu_code >}}PycharmProjects {{< /menu_code >}}
 - un projet par séance : par défaut {{< menu_code >}}untitled2{{< /menu_code >}} mais il est sélectionné pour pouvoir mettre un nom de projet explicite.
 

### Interpréteur

C'est la version de python que vous utiliserez pour ce projet. Nous utiliserons **TOUJOURS** python3. Choisissez le donc. S'il n'est pas proposé par défaut, cliquez sur le triangle à droite et trouvez le dans la liste proposée (il est possible  d'[importer un interpréteur](#préférences-changer-d-interpréteur) présent sur votre ordinateur si PyCharm ne le trouve pas) A l'ECM, nous avons à notre disposition la version 3.5 de python (à l'heure où ces lignes sont tapées). Chez vous, vous aurez certainement une version (encore) plus récente.


## Créer et exécuter un fichier python

Une fois un nouveau projet créé, vous devez avoir une fenêtre du type ci-dessous qui apparaît : 

![un projet vide](/img/pycharm/files/empty_project.png)

Les différents éléments de la fenêtre sont accessible via le menu {{< menu_code >}}View > Tool Windows...{{< /menu_code >}}. Par exemple, la liste des fichiers à gauche s'appelle {{< menu_code >}}Project{{< /menu_code >}}.


### Créer

Pour créer un nouveau fichier, il faut que vous ayez sélectionné le dossier dans lequel votre fichier va être créer dans la partie {{< menu_code >}}Project{{< /menu_code >}} de la fenêtre (comme c'est le cas dans la figure ci-dessus). A partir de là vous pouvez créer un nouveau fichier dans le menu {{< menu_code >}}File > New...{{< /menu_code >}} puis en choisissant un  {{< menu_code >}}Python File{{< /menu_code >}}. Le fichier est créé dans le dossier sélectionné.

On peut l'afficher dans la fenêtre principale en double cliquant sur son nom dans la partie {{< menu_code >}}Project{{< /menu_code >}}.

Par exemple un fichier `hello.py` dont le code est 

```
print("hello world!")
```

![un projet vide](/img/pycharm/files/hello_world_file.png)

### Exécuter

Exécuter un fichier se fait *via* le menu {{< menu_code >}}Run{{< /menu_code >}}. Il y a deux commandes Run dans ce menu : {{< menu_code >}}Run nom_fichier{{< /menu_code >}} et {{< menu_code >}}Run...{{< /menu_code >}}. Le second permet de choisir le fichier à exécuter. Une fois choisi, son nom apparaîtra en haut à droite de la fenêtre, à côté du triangle vert permettant de l'exécuter. 

{{< note >}}
Il est ainsi possible de travailler sur un fichier et d'en exécuter un autre en cliquant sur le triangle vert. C'est très pratique lorsque l'on travaille sur une méthode et que l'on exécute les tests de celle-ci présents dans un autre fichier.
{{< /note >}}

## Environnement d'exécution 


Les environnement d'exécutions permettent d'exécuter des programmes ou des tests python. On les trouve soit grace à la barre de menu, item {{< menu_code >}} Run{{< /menu_code >}}, ou en haut à droite de la fenêtre (son nom puis un petit triangle vert pour exécuter l'environnement).  

Pour créer un nouvel environnement d'exécution :

  - Ouvrez la fenêtre des contextes d'exécution dans le menu {{< menu_code >}}Run > Edit configuration...{{< /menu_code >}}.
  - La fenêtre qui s'est ouverte contient tous les contextes d'exécution de votre projet. Cliquez sur le {{< menu_code >}}+{{< /menu_code >}} en haut à gauche de la fenêtre pour en créer un nouveau.
  - Choisissez {{< menu_code >}}python{{< /menu_code >}} si vous voulez exécuter du code ou {{< menu_code >}}python tests{{< /menu_code >}} pour un framework de test. Paramètrez votre environnement en choisissant le script à exécuter (on pourra également nommer son environnement).
  - Cliquez sur {{< menu_code >}}OK{{< /menu_code >}} pour créer l'environnement.

{{< note warning >}}
Dans la fenêtre de gestion des contextes, ne modifiez pas les contextes par défaut. Ce sont des templates.
{{< /note >}}

Pour plus d'informations, reportez vous à [la documentation de pycharm](https://www.jetbrains.com/help/pycharm/2016.3/working-with-run-debug-configurations.html?search=run).


## Préférences : changer d'interpréteur

Les préférences de Pycharm sont accessibles *via* le menu {{< menu_code >}}File > Settings...{{< /menu_code >}}. La fenêtre de préférences ressemble à ça : 

![un projet vide](/img/pycharm/settings/settings.jpg)

On peut quasiment tout changer, de l'apparence à l'interpréteur en passant par les raccourcis clavier.

> En haut à gauche se trouve un champ texte. Il permet de réduire les préférences à celles contenant le texte tapé (voir image ci-après). 

L'interpréteur du projet se trouve dans la partie {{< menu_code >}}Project{{< /menu_code >}} de la fenêtre des préférences.


![un projet vide](/img/pycharm/settings/interpreter.jpg)

### Créer un nouvel interpréteur

Pour créer un nouvel interpréteur à partir de la fenêtre de l'interpréteur, il suffit de cliquer sur l'engrenage dans la partie réservée à l'interpréteur : 

![un projet vide](/img/pycharm/settings/engrenage.png)

Si l'on veut ajouter un programme python déjà présent sur la machine, on choisit {{< menu_code >}}Add Local...{{< /menu_code >}}.

Une nouvelle fenêtre s'affiche : 

![ajout d'un interpréteur](/img/pycharm/settings/nouvel_interpreteur_venv.png)

Attention, par défaut `virtualenv environment` (en haut à gauche de la fenêtre) est utilisé. Dans l'absolu [c'est très bien](http://sametmax.com/les-environnement-virtuels-python-virtualenv-et-virtualenvwrapper/), mais pour nous, ca va plus nous embêter qu'autre chose (en particulier il faudrait réinstaller numpy à chaque tp...). On choisi donc `system interpréteur` et un python 3 d'installé : 

![interpréteur python](/img/pycharm/settings/interpreteur_python.png)


Dans l'image ci-dessus, mon interpréteur python3 (python3.6) était dans le dossier `/usr/local/bin` (ce qui est souvent le cas dans le monde unix ou mac)

### Installer des modules

On commence par aller trouver son interpréteur *via* le menu {{< menu_code >}}File > Settings...{{< /menu_code >}} (je l'ai trouvé en tapant `interp` dans l'onglet de recherche) : 

![python](/img/pycharm/settings/interpreteur_par_recherche.png)

Les packages installé sont listé dans la fenêtre, avec le numéro de version installé et la dernère version disponible. Pour installer le package `numpy` on commence par cliquer sur le bouton `+` en bas à gauche de la fenêtre. Un zillion de package sont disponible. On cherche numpy : 

![python](/img/pycharm/settings/package_numpy.png)

On peut ensuite cliquer sur `install package` en bas à gauche pour installer le package.

## Aide en ligne

PyCharm est un éditeur professionnel, c'est normal que la prise en main soit plus complexe qu'avec un éditeur moins performant (comme notepad++ voir Sublime Text) ou scolaire (comme Spyder). En revanche, bien l'utiliser permet d'une part des gains de productivité importants et d'autre part de coder plus agréablement. 

Le système d'aide de PyCharm est très complet et vous permet de vous familiariser mieux avec la bête. Il est disponible sur le site de l'éditeur : [aide Pycharm](https://www.jetbrains.com/help/pycharm/meet-pycharm.html) 

