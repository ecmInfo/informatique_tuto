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


## Introduction


Ce tuto va vous monter les différentes étapes pour configurer son [Pycharm](https://www.jetbrains.com/pycharm/) lorsqu'on l'utilise pour la première fois.

[Pycharm](https://www.jetbrains.com/pycharm/) est l'[IDE](https://fr.wikipedia.org/wiki/Environnement_de_développement) qui sera utilisé tout au long de l'UE d'informatique à l'[ecm](https://www.centrale-marseille.fr). C'est un éditeur professionnel, il faut donc un peu de temps pour maitriser la bête, mais une fois cet apprentissage effectué, vous ne pourrez plus vous en passer.

Ce logiciel existe sous deux formes, la version professionnelle et la version communautaire. C'est cette dernière que nous utilisons (en tant qu'étudiant, vous pouvez utilisez la version professionnelle gratuitement mas elle n'est vraiment utile que si vous faites du développement poussé en python ou que vous faites du développement web en python).


## Exécuter le programme

On suppose que vous êtes installé devant un ordinateur d'une salle machine Linux et que vous vous êtes connecté en utilisant le gestionnaire de fenêtre par défaut (si vous n'avez touché à rien, ce devrait être le cas. On choisi son gestionnaire de fenêtre sur l'écran de connexion en haut à droite).

### Un terminal

Un [terminal](https://fr.wikipedia.org/wiki/Shell_Unix) est une fenêtre permettant d'exécuter des commandes. Nous allons l'utiliser ici pour exécuter Pycharm.  Sur la barre des tâches en haut à gauche de l'écran :

  1. cliquez sur {{< menu_code >}}application{{< /menu_code >}} 
  2. suivez le sous-menu {{< menu_code >}}outils systèmes{{< /menu_code >}} 
  3. cliquez sur {{< menu_code >}}Terminal MATE{{< /menu_code >}}  (les autres terminaux vont aussi) 
      

Une fenêtre apparaît. Bous pouvez y taper des commandes.

### Commande pycharm.sh      
   
  1. Ouvrez un terminal 
  2. dans celui-ci, tapez `pycharm.sh` puis sur la touche entrée (on pourra utiliser la [complétion automatique](https://ensiwiki.ensimag.fr/index.php?title=Trucs_et_astuces_Unix#Compl.C3.A9tion_automatique_avec_TAB) en ne tapant que `pyc` puis en appuyant sur la touche tabulation qui complètera automatiquement en `pycharm.sh`)
  3. **ON SE RETIENT D'APPUYER SUR OK SANS RIEN LIRE LORSQUE LA PREMIÈRE FENÊTRE APPARAIT** (je sais, c'est dur)
  

## Configuration  

Lors de la première utilisation de Pycharm, vous aurez à choisir si vous [importez des préférences]({{< relref "#import-des-préférences-précédentes" >}}) et de configurer l'[apparence de votre éditeur]({{< relref "#apparence-de-pycharm" >}}). 

Toutes ces configurations pourront être modifiées plus tard dans l'onglet {{< menu_code >}}file > settings...{{< /menu_code >}} du menu de Pycharm.
### Import des préférences précédentes

Si c'est la première fois que vous utilisez Pycharm où qu'une nouvelle version est disponible, la fenêtre suivant apparait :

![importation des préférences](/img/pycharm/prefs/import_old_settings.jpg#center)


Si vous avez utilisé PyCharm précédemment, il vous proposera par défaut d'importer les préférences de l'ancienne version. Choisissez de ne rien importer puis cliquer sur {{< menu_code >}}Ok{{< /menu_code >}}.

### Apparence de Pycharm

Une nouvelle fenêtre (sauvage) apparait qui vous permettra de configurer l'apparence de votre navigateur. J'aime bien le thème *Darcula*, c'est donc ce que j'ai choisit :

![importation des préférences](/img/pycharm/prefs/prefs.jpg#center)

Puis on peut cliquer sur {{< menu_code >}}Ok{{< /menu_code >}}. 

### Choix d'un projet

Si c'est la première fois que vous utilisez Pycharm, vous n'avez pas encore de projet actif (*ie.* le dernier projet utilisé) et c'est la fenêtre de choix du projet qui apparaît : 

![choix d'un projet](/img/pycharm/fenetre_demarrage_normal.jpg)

Vos projets sont (s'il y en a) listés à gauche de cette fenêtre (là, il n'y en a pas).

Cliquez sur {{< menu_code >}}Create new project{{< /menu_code >}}. 


## Démarrer un nouveau projet


Pour créer un nouveau projet, vous cliquez sur {{< menu_code >}}File > new... > Project{{< /menu_code >}} dans un projet existant. La fenêtre suivant vou permet alors de créer un projet : 

![choix d'un projet](/img/pycharm/create_project.jpg)

 - la première ligne concerne le nom et l'emplacement du projet
 - la seconde ligne vous demande quel interpréteur python vous voulez utiliser.


### Nom et emplacement du projet

Essayez d'avoir un peu d'ordre dans vos projets. À chaque séance on vous demandera de créer un nouveau projet. C'est important pour ne garder que les fichiers relatif au projet courant. Si vous ne faite qu'un unique projet pour toutes les séances vous allez vous perdre et Pycharm également. 



> Ayez un répertoire commun à tous les projets, ici : `PycharmProjects`. Le porjet s'appelle pour l'instant `untitled2` mais on s'aéforcera de choisir un nom en rapport avec ce qu'on va y faire.

### Interpréteur

C'est la version de python que vous utiliserez pour ce projet.

> Nous utiliserons **TOUJOURS** python3. Choisissez le donc. A l'ecm, nous avons à notre disposition la version 3.5 de pyhton. Chez vous, vous aurez certainement une version plus récente.


## Créer et exécuter un fichier python

### Créer

### Exécuter




## Changer et importer un interpréteur


