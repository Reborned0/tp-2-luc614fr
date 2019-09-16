
# Exercice 1. Variables d’environnement



1- <b>_. Dans quels dossiers bash trouve-t-il les commandes tapées par l’utilisateur ?_</b>

on tappe la commande `printenv PATH` et on a ce chemin comme résultat `/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin
:/bin:/usr/games:/usr/local/games:/snap/bin`

2- <b>_.Quelle variable d’environnement permet à la commande cd tapée sans argument de vous ramener dans
votre répertoire personnel ?_</b>

la variable d'environnement est la suivante : `$HOME`

3- <b> Explicitez le rôle des variables LANG, PWD, OLDPWD, SHELL et _.</b>

la variable d’environnement LANG détermine la langue que les logiciels utilisent pour communiquer avec l’utilisateur
la variable d'environnement PWD contient le répertoire de travail courant de l'interpréteur de commande.
la variable d'environnement OLDPWD contient le chemin absolu vers le répertoire courant précédent
la variable d'environnement SHELL indique l'interpréteur shell utilisé par défaut, ici c'est /bin/bash 
la variable d'enbvironnement _ indique dans quel répertoire se situe dans la commande utilisé précedemment

4- <b> _Créez une variable locale MY_VAR (le contenu n’a pas d’importance). Vérifiez que la variable existe_ </b>

`MY_VAR= ; printenv MY_VAR
echo $MY_VAR`

5- <b> _Tapez ensuite la commande bash. Que fait-elle ? La variable MY_VAR existe-t-elle ? Expliquez. A la fin
de cette question, tapez la commande exit pour revenir dans votre session initiale._ </b>

Elle ouvre un nouveau niveau sur le shell. La variable MY_VAR n'existe pas car c'est une variable locale 

6- <b> _Transformez MY_VAR en une variable d’environnement et recommencez la question précédente. Expliquez._ </b>

`export MY_VAR="abc"` puis `printenv MY_VAR` et je vois abc qui apparait 

7- <b> _Créer la variable d’environnement NOMS ayant pour contenu vos noms de binômes séparés par un espace.
Afficher la valeur de NOMS pour vérifier que l’affectation est correcte._ </b>

`export NOMS="lucas franck"`  L'affectation est bien correcte après vérification 


8- <b> _Ecrivez une commande qui affiche ”Bonjour à vous deux, binôme1 binôme2 !” (où binôme1 et binôme2
sont vos deux noms) en utilisant la variable NOMS._ </b>

`echo "Bonjour à vous deux, $NOMS"` 

9- <b> _Quelle différence y a-t-il entre donner une valeur vide à une variable et l’utilisation de la commande
unset ?_ </b>

La variable qui a une valeure vide est toujours utilisable tandis que l'utilisation de la commande unset sur une variable la supprime et la rend inutilisable 

10.  <b> _Utilisez la commande echo pour écrire exactement la phrase : $HOME = chemin (où chemin est votre
dossier personnel d’après bash)_ </b>

`echo "\$HOME = $HOME"`

# Programmation Bash


# Exercice 2. Contrôle de mot de passe


